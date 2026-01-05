Berikutnya kita mulai dengan **file kedua** secara **rapih, mendalam, dan terstruktur**:

---

```markdown
# 📘 01_Arsitektur_Teknis_WhatsApp_End-to-End.md
## End-to-End Technical Architecture — WhatsApp Integration
*Version: 1.0 | Last Updated: 2026-01-05*

---

## 🎯 Tujuan Dokumen

Dokumen ini menjelaskan **arsitektur teknis komprehensif** untuk integrasi WhatsApp Cloud API ke dalam sistem *Lawyers-Hub*, termasuk:

✅ Komponen arsitektur  
✅ Alur data & event  
✅ Boundary logic  
✅ Syarat non-functional (security, scalability, reliability)  
✅ Prinsip desain yang aman untuk konteks hukum

Dokumen ini menjadi **referensi utama tim engineering & security** dalam merancang layanan WhatsApp yang production-ready.

---

## 📌 Ringkasan Arsitektur

**Pendekatan utama:**
- WhatsApp sebagai *transport layer* (tidak menyimpan business logic)
- Sistem internal *Lawyers-Hub* sebagai *system of record*
- AI hanya untuk **klasifikasi/estimasi** (read-only)
- Semua keputusan hukum dan billing diputuskan manusia

High-Level Architecture:

```

WhatsApp Cloud API
│
▼
Webhook Gateway
│
▼
Message Ingestor & Normalizer
│
▼
Event Bus / Queue System
│
▼
Core Domain Services
│
├─ Intake Service
├─ Messaging Service
├─ Billing & Time Tracking
├─ AI Assist Service (read-only)
└─ Audit & Logging

```

Outbound Path:

```

Lawyer Dashboard
│
▼
Template Validator
│
▼
Outbound Messaging Service
│
▼
WhatsApp Send API

````

---

## 🔐 4. Data Residency, Multi-tenancy & Scalability

### 📍 4.1 Data Residency (Kepatuhan PDP)
- **Primary Storage:** Semua data NormalizedMessage dan PII (Hashed) harus disimpan di server yang berlokasi di **Indonesia** untuk mematuhi UU PDP.
- **Temporary Storage:** Payload raw di Gateway disimpan maksimal 7 hari untuk keperluan debugging, terenkripsi (AES-256).
- **AI Processing:** Jika menggunakan provider AI eksternal, pastikan data yang dikirim sudah di-sanitize (PII masking).

### 🏢 4.2 Multi-tenancy & Isolation
- **Tenant Scoping:** Setiap request ke WhatsApp API dan penyimpanan data harus menyertakan `tenantId`.
- **Isolation Level:** Data antar tenant harus terpisah secara logis (Row-Level Security) atau fisik (Separate Databases) untuk mencegah kebocoran informasi antar firma hukum.
- **WABA Mapping:** Pemetaan antara WhatsApp Business Account (WABA) dan `tenantId` dikelola di layanan konfigurasi pusat.

### 📈 4.3 Scalability & Performance
- **Horizontal Scaling:** Webhook Gateway harus stateless agar bisa di-scale secara horizontal di belakang Load Balancer.
- **Throughput Management:** Gunakan Redis-based queue (BullMQ) untuk mengelola spike traffic dari WhatsApp.
- **Idempotency:** Implementasikan `Idempotency Key` (Message ID) di semua layer (Gateway, Normalizer, Domain) untuk mencegah pemrosesan ganda.
- **SLA:** Target respon webhook < 200ms untuk menghindari retry otomatis dari Meta.
- **Circuit Breaker:** Implementasikan pattern Circuit Breaker pada outbound path untuk mencegah cascading failure saat WhatsApp API mengalami gangguan.

---

## 📅 8. Implementation Roadmap (Phased)

### Phase 1: Foundation (Week 1-2)
- Webhook Gateway setup (Signature verification, Dedup).
- Message Normalizer (Basic schema, Hashing).
- Multi-tenant config service.

### Phase 2: Core Workflows (Week 3-4)
- Event Bus integration (BullMQ).
- Intake Pre-Case State Machine.
- Outbound Messaging (Template validation).

### Phase 3: AI & Security (Week 5-6)
- AI Assist (Classification, PII Masking).
- Media Service (Virus scan, Secure storage).
- Audit Trail & Immutable Logging.

### Phase 4: Observability & Scaling (Week 7-8)
- Centralized Monitoring (Prometheus/Grafana).
- Distributed Tracing (Jaeger/Zipkin).
- Load Testing & HA Validation.

---

## 📂 5. Media Handling Architecture

Untuk menangani dokumen hukum, gambar, dan media lainnya:
1. **Inbound Media:** Gateway menerima media URL dari Meta -> Worker mengunduh media -> Simpan ke Private Cloud Storage (S3/GCS) dengan enkripsi -> Simpan `contentRef` di database.
2. **Security Scan:** Semua media yang diunduh wajib melalui proses virus/malware scanning sebelum dapat diakses oleh user.
3. **Lifecycle Policy:** Dokumen yang tidak lagi aktif dalam perkara (misal: intake yang tidak lanjut) harus dihapus otomatis setelah periode retensi tertentu (misal: 30 hari).

---

## 🧱 Komponen Utama & Tanggung Jawab

### 1) WhatsApp Cloud API
**Peran:**
- Menyediakan kanal komunikasi resmi
- Mengirim/terima pesan template dan non-template

**Aturan:**
☑️ Hanya template yang disetujui boleh dikirim  
☑️ Delivery & read receipts masuk sebagai event

---

### 2) Webhook Gateway
**Fungsi utama:**
- Verifikasi signature Meta
- Sanitasi payload
- Deduplikasi event
- Forward event ke Normalizer

**Harus dipenuhi:**
- Signature HMAC check  
- Idempotent request handling  
- Throttle & rate limiting  
- Logging level debug/trace

**Output:**
```ts
WebhookEvent {
  eventId: UUID
  provider: "whatsapp"
  rawPayloadRef: EncryptedStorageRef
  receivedAt: timestamp
}
````

---

### 3) Message Ingestor & Normalizer

**Fungsi:**

* Parsing event
* Normalisasi ke internal format
* Extract metadata (sender_hash, type)

**Normalized Message Schema:**

```ts
NormalizedMessage {
  id: UUID
  tenantId: string
  channel: "whatsapp"
  direction: "inbound" | "outbound"
  senderHash: string
  messageType: "text" | "document" | "template"
  contentRef: string?
  timestamp: DateTime
}
```

---

## 🛡️ 6. High Availability (HA) & Disaster Recovery (DR)

Untuk menjamin layanan tetap berjalan di lingkungan hukum yang kritis:
- **Multi-AZ Deployment:** Deploy layanan Gateway dan Normalizer di minimal dua Availability Zone (AZ).
- **Database Replication:** Gunakan Read Replicas untuk Messaging Store dan Failover otomatis untuk Core DB.
- **Queue Persistence:** Pastikan Redis/BullMQ dikonfigurasi dengan AOF (Append Only File) untuk mencegah kehilangan pesan saat restart.
- **RTO/RPO:** Target RTO (Recovery Time Objective) < 4 jam dan RPO (Recovery Point Objective) < 15 menit.

## 🔑 7. Secret & Key Management

- **Tenant Secrets:** API Key WhatsApp (Phone Number ID, WABA ID, Access Token) disimpan di **Secret Manager** (Vault/AWS Secret Manager) dengan enkripsi per-tenant.
- **Encryption Keys:** Key untuk enkripsi media dan PII di-rotate secara periodik setiap 90 hari.
- **Zero Trust:** Komunikasi antar microservice (misal: Gateway ke Normalizer) wajib menggunakan mTLS atau API Key internal yang divalidate.

---**Aturan:**
☑️ No storage of raw phone number
☑️ Document metadata saja — isi file referensi

---

### 4) Event Bus / Queue

**Mengapa perlu:**

* Memastikan reliability
* Mendukung retry, DLQ
* Menghilangkan blocking di webhook

**Arsitektur:**

```
MessageReceived
OutboundRequested
IntakeUpdated
TimeEntrySuggested
```

Queue technology: e.g. **BullMQ, SQS, Kafka** (tergantung skala)

---

### 5) Core Domain Services

#### a) Intake Service

* Manages Pre-Case sessions
* Handles consent & question tree
* Persists structured intake data

#### b) Messaging Service

* Normalized message store
* Associates WA message → session
* Outbound scheduling

#### c) Billing & Time Tracking

* Time suggestion (AI assisted)
* Human approval
* Invoice draft generation

#### d) AI Assist Service

**Role terbatas:**

* Classify intent
* Klasifikasi urgensi
* Estimasi kompleksitas
* Suggest time estimate
  **Tidak boleh:** auto respond atau keputusan hukum

#### e) Audit & Logging

* Append-only logs
* Immutable
* Track who/when/why

---

## 🔐 Keamanan & Compliance

### A. Data Protection (PDP)

* No plaintext phone number
* Hashed identifier (HMAC)
* Content references encrypted
* Minimal retention sesuai policy

### B. Access Control

* Scoped API tokens per tenant
* Role-based access untuk actions
* Audit trail untuk semua write

### C. Immutable Logging

* Tidak boleh update/delete
* Kalau perlu koreksi → record separat

---

## 🧠 Prinsip Perilaku Sistem

| Concern            | Rule                    |
| ------------------ | ----------------------- |
| AI Role            | Read-only; assist only  |
| Legal Advice       | Only by human (lawyer)  |
| Billing            | Must be lawyer approved |
| WhatsApp Templates | Pre-approved            |
| Consent            | Explicit required       |
| Logging            | Immutable, traceable    |

---

## ⚙️ Alur Data (Skenario Nyata)

### Inbound

1. WA event masuk → Webhook
2. Gateway verifikasi → forward
3. Ingestor normalisasi → Event Bus
4. Intake service proses → AI classify (read-only)
5. Notifikasi ke UI

### Outbound

1. Lawyer triggers outbound
2. Template validator checks
3. Messaging schedules via Event Bus
4. Outbound service calls WA API
5. Log & notify status

---

## 📈 NFR (Non-Functional Requirements)

| Category      | Target                        |
| ------------- | ----------------------------- |
| Latency       | < 500ms processing per event  |
| Scalability   | Auto scale event consumers    |
| Availability  | ≥ 99.9% SLA                   |
| Observability | Structured logs + metrics     |
| Security      | Zero plaintext sensitive data |

---

## 🧪 Testing Considerations

* Unit tests for normalization & gateway
* Integration tests with WhatsApp sandbox
* Contract tests for event schema
* Load tests for spike scenarios
* Security tests for signature & rate limits

---

## 📦 Teknologi yang Direkomendasikan

| Layer           | Rekomendasi             |
| --------------- | ----------------------- |
| Webhook Gateway | Node.js / Fastify       |
| Queue           | BullMQ / Redis / SQS    |
| Normalizer      | TypeScript              |
| AI Assist       | internal microservice   |
| Logging         | Elastic / Loki / Splunk |
| Metrics         | Prometheus / Grafana    |

---

## 📌 Kesimpulan

Arsitektur ini dibangun dengan prinsip:
✅ Separation of Concerns
✅ Auditability
✅ Security by Design
✅ Ethics & Compliance

Setiap komponen punya boundary yang jelas, sehingga ketika diimplementasikan, **tidak ada business logic yang bocor ke kanal transport (WhatsApp)** dan **AI tidak pernah mengambil keputusan hukum**.

---

## 📎 Referensi Cepat

* Meta WhatsApp Cloud API docs
* Event Driven Architecture best practices
* Indonesian PDP guidelines
* Legal ethics standards

---

```

---

Jika format ini sesuai, saya siap lanjut ke **file berikutnya**, yaitu:
➡️ `02_Diagram_Sequence_Inbound_Outbound.md`

Tunggu arahan Anda (atau cukup bilang “lanjut”).
```

Berikut **lanjutan dokumen** secara **rapih, mendalam, dan siap pakai**:

---

```markdown
# 📘 04_Message_Ingestor_and_Normalization.md  
## Message Ingestor & Normalization | WhatsApp Integration  
*Version: 1.0 | Last Updated: 2026-01-05*

---

## 🎯 Tujuan Dokumen

Dokumen ini menjelaskan secara komprehensif:

✔ Bagaimana **event masuk dari WhatsApp** diproses  
✔ Bagaimana payload dinormalisasi jadi format internal Lawyers-Hub  
✔ Komponen apa saja yang terlibat  
✔ Aturan keamanan, penyimpanan, dan retensi  
✔ Edge case & strategi error handling

Flow ini berada di **antara Webhook Gateway** dan **Core Domain (Event Bus → Services)**.

---

## 📌 Terminologi Inti

| Istilah | Definisi |
|---------|----------|
| Raw Event | Payload asli dari WhatsApp Cloud API |
| Normalizer | Komponen yang memetakan raw event → bentuk internal |
| Normalized Message | Output yang konsisten untuk downstream services |
| ContentRef | Referensi ke konten media (file id/URL) |
| SenderHash | Identitas tersamarkan (hashed phone) |

---

## 🧱 Arsitektur — Scope

```

Webhook Gateway
↓ (WebhookEvent)
Message Ingestor & Normalizer
↓ (NormalizedMessage)
Event Bus / Queue
↓
Core Domain Services

````

**Inti:**
- Normalizer tidak mengandung *business logic*
- Semua event memiliki *audit trail*
- Tidak ada storage raw sensitive data secara clear

---

## 🧠 1️⃣ Goals Normalization

1. **Konsistensi antar event**
   - WhatsApp Cloud API punya banyak tipe event
   - Kita perlu format yang cocok diproses domain

2. **Security & Privacy**
   - Tidak menyimpan phone asli
   - Media/reference disimpan aman

3. **Idempotency downstream**
   - Output harus bisa retry tanpa efek ganda

---

## 📍 2️⃣ Normalized Message — Schema

### 🧱 2.1 Struktur Utama

```ts
NormalizedMessage {
  id: UUID
  tenantId: string // Pemetaan WABA_ID -> Tenant dikelola di Service Configuration
  eventType: NormalizedEventType
  priority: "high" | "normal" | "low" // Prioritas pesan (e.g. OTP = High)
  channel: "whatsapp"
  direction: "inbound" | "outbound" | "status_update"
  senderHash: string
  recipientHash: string?
  messageType: MessageType
  content: ContentMetadata
  timestamp: DateTime
  rawRef: string // Pointer ke encrypted raw payload (AES-256)
  metadata: {
    language?: string 
    waMessageId: string 
    isPrivileged: boolean // Penanda rahasia jabatan advokat
    [key: string]: any
  }
}
```

---

### 🧱 2.1.2 Tenant Lookup & Isolation
- **Mechanism:** Ingestor melakukan query ke **Tenant Configuration Service** (dengan cache Redis) menggunakan `WABA_ID` dari payload WhatsApp.
- **Security:** Jika `tenantId` tidak ditemukan, event dihentikan (dropped) dan dicatat sebagai security event.
- **Isolation:** Data hasil normalisasi harus disimpan dengan `tenantId` sebagai kunci partisi (Row-Level Security) untuk menjamin isolasi data antar firma hukum.

### 🧱 2.1.5 Media Normalization & Virus Scan
Untuk pesan berupa gambar atau dokumen:
1. **Download:** Ingestor mendownload media dari URL sementara WhatsApp.
2. **Virus Scan:** Media dikirim ke **Virus Scan Service** (misal: ClamAV) sebelum disimpan.
3. **Secure Storage:** Simpan media di internal storage (S3/GCS) dengan enkripsi at-rest menggunakan kunci enkripsi spesifik per-tenant.
4. **Reference:** Simpan UUID storage ke dalam field `content.mediaId`.
5. **Lifecycle:** Media di internal storage mengikuti kebijakan retensi firma hukum (misal: 5 tahun sesuai standar dokumen hukum).

---

### 🧱 2.2 NormalizedEventType

Enumerasi:

```
enum NormalizedEventType {
  inbound_text
  inbound_document
  inbound_media
  status_update
  template_response
  unknown
}
```

---

### 🧱 2.3 MessageType

```
enum MessageType {
  text
  document
  image
  video
  template
  unknown
}
```

---

### 🧱 2.4 ContentMetadata

```ts
ContentMetadata {
  textBody?: string
  mediaId?: string
  mediaMimeType?: string
  templateName?: string
  templateVars?: string[]
}
```

📌 **Catatan:**

* `textBody` hanya untuk pesan teks
* `mediaId` direferensikan → di-fetch & disimpan di storage ter-encrypted (opsional, tergantung kebutuhan retention)

---

## 📍 3️⃣ Normalization Rules

### ✅ Rule #1 — WhatsApp Raw → Internal Fields

| Raw Field (WA)                                 | Internal Field            |
| ---------------------------------------------- | ------------------------- |
| `entry[].id` (WABA ID)                         | tenantId (via lookup)     |
| `entry[].changes[].value.messages[].from`      | senderHash                |
| `entry[].changes[].value.messages[].text.body` | content.textBody          |
| `entry[].changes[].value.messages[].type`      | messageType               |
| `entry[].changes[].value.statuses[].status`    | eventType = status_update |

### 🛡️ Rule #1.5 — Privacy & Masking
- **Hashing:** Nomor telepon asal (`from`) wajib di-hash menggunakan HMAC-SHA256 sebelum masuk ke `senderHash`.
- **Anonymization for AI:** Jika pesan diteruskan ke AI Assist, `textBody` harus melalui filter PII Masking (menghapus nama asli, alamat, dll) dan disimpan dalam field metadata terpisah (misal: `content.maskedText`).

---

### ⚠️ Rule #2 — Template Identifiers

Jika raw event adalah template response:

* `templateName` = WA template identifier
* `templateVars` = variabel teks

---

### 📌 Rule #3 — Media / Document

Jika ada file:

* WA memberikan `id`
* Normalizer:

  1. simpan `mediaId`
  2. push task untuk fetch media & simpan ke encrypted storage
  3. update ContentMetadata dengan pointer storage

---

## 🧩 4️⃣ Direction Handling

### 🟢 Inbound

* text → inbound_text
* document/image/video → inbound_media / inbound_document
* template responses → template_response

### 🔵 Outbound Status

* delivered
* read
* failed
  Masuk ke eventType = `status_update`

---

## 📍 5️⃣ Sender / Recipient Hashing

### 🛠 Hashing Method

Gunakan:

```
sha256_hmac(phoneNumber, platformSecret)
```

**Hasil**:

* konsisten across components
* tidak bisa dibalik jadi phone asli

---

## 🧪 6️⃣ Idempotency Key

Key generasi:

```
"idempotencyKey" = event.messageId || event.statusId
```

Jika downstream sudah memproses idempotencyKey:

* skip
* ack cepat

---

## ⚠️ 7️⃣ Missing / Unsupported Fields

Jika encounter field yang tak dikenal:

* `NormalizedEventType = unknown`
* log warning level
* dispatch ke DeadLetterQueue (DLQ)

---

## 📊 8️⃣ Error Semantics & Handling

| Error Code | Category | Description | Handling Action |
|------------|----------|-------------|-----------------|
| `ERR_AUTH_SIG` | Security | Signature verification failed | Drop + Log Critical Alert |
| `ERR_TENANT_NOT_FOUND` | Security | WABA_ID not mapped to any tenant | Drop + Audit Log |
| `ERR_MALFORMED_JSON` | Payload | WhatsApp sent invalid JSON | Log + DLQ |
| `ERR_MEDIA_FETCH` | Infrastructure | Failed to download media from Meta | Retry (Exponential Backoff) |
| `ERR_VIRUS_DETECTED` | Security | Media contains malware/virus | Quarantine + Notify Lawyer |
| `ERR_PII_SCRUB` | Privacy | Failed to mask sensitive data | Log + DLQ (manual review) |
| `ERR_HASH_FAIL` | Privacy | Failed to hash phone number | Log Critical + Stop Processing |

---

## 🗳️ 9️⃣ Retention & Purging

### Minimum retention policy

* `rawRef`: 90 hari
* `NormalizedMessage`: 365 hari (audit)

Opsional:

* shorter retention jika tenant request purge (compliance)

---

## 📍 10️⃣ Performance & Throughput

**Target:**

* 99.9% ack < 200ms
* decoupled processing
* horizontal scale normalizer workers

---

## 🧠 11️⃣ Observability & Metrics

KPI penting:

* inbound events/sec
* normalize errors count
* unknown event ratio
* DLQ events

Monitoring:

* logs structured (JSON)
* metrics prom exported

---

## 🧪 12️⃣ Contract Testing (Essential)

Kontrak schema:

* raw WA webhook → NormalizedMessage
* Must include:

  * required fields
  * hashed sender
  * timestamp
  * eventType

Test scenarios:

* text message
* document
* template
* status update
* duplicate event

---

## 📌 13️⃣ Summary

**Message Ingestor & Normalization** adalah lapisan yang menjamin:
✔ Konsistensi data seluruh event inbound
✔ Privacy (hashing & encrypted storage)
✔ Idempotent processing
✔ Clean contract ke downstream services

Ini adalah dasar yang kuat untuk:

* Intake workflows
* AI Assist classification
* Billing & audit trails

---

## 📎 Referensi

* WhatsApp Cloud API Payload Structure
* Event Driven Architecture Patterns
* Secure hashing practices

```

---

Silakan cek format **dan konfirmasi**.  
Kalau sudah pas, saya akan lanjut ke:

➡️ **05_Event_Bus_and_Async_Workflow.md**

Tinggal jawab **lanjut**.
::contentReference[oaicite:0]{index=0}
```

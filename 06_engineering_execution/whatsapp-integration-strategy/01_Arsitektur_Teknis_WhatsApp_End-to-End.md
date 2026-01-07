# Arsitektur Teknis WhatsApp End-to-End

## 1. High-Level Architecture

Integrasi ini menggunakan **WhatsApp Cloud API** (hosted by Meta) untuk
mengurangi _maintenance overhead_ infrastruktur on-premise, dengan fokus pada
keamanan dan skalabilitas.

```mermaid
graph LR
    User((User/Client)) <-->|WhatsApp App (E2EE)| Meta[Meta Cloud API]
    Meta <-->|Webhook / HTTPS (TLS 1.3)| GW[Lawyers Hub WA Gateway\n(NestJS)]
    GW <-->|AMQP| MQ[Message Queue\n(RabbitMQ/Redis)]
    MQ <-->|Event| Core[Core Service]
    Core <-->|Context| AI[CopilotKit AI]
    Core <-->|Persist| DB[(PostgreSQL)]
    Lawyer((Lawyer)) <-->|Web Dashboard| Core
```

## 2. Komponen Utama

### 2.1 WhatsApp Cloud API

- **Role**: Interface utama pengiriman/penerimaan pesan.
- **Hosting**: Meta Infrastructure (US/EU).
- **Auth**: System User Access Token (Permanent/Rotating).
- **Compliance**: Meta bertindak sebagai Data Processor (GDPR).

### 2.2 WA Gateway Service (NestJS)

- **Role**: Entry point untuk Webhook.
- **API Version**: WhatsApp Business API **v22.0** (Update 2026).
- **Responsibility**:
  - Validasi Signature (`X-Hub-Signature-256`).
  - Deduplikasi pesan (berdasarkan `wamid`).
  - Media download & re-upload ke **S3 Private Bucket** menggunakan
    `MediaService`.
  - Publish event ke Message Queue.

### 2.3 Message Queue (Event Bus)

- **Role**: Decoupling antara penerimaan pesan (cepat) dan pemrosesan bisnis
  (kompleks).
- **Topics**:
  - `wa.message.incoming`
  - `wa.message.outgoing`
  - `wa.status.update` (Sent, Delivered, Read)

### 2.4 Core Service & AI Orchestrator

- **Role**: Business logic, Case mapping, AI processing.
- **Logic**:
  - Mapping `phone_number` ke `Client Entity`.
  - Deteksi sesi aktif (24h window).
  - Routing ke AI Assistant atau Human Lawyer.

## 3. Strategi Keamanan (Security & Compliance)

### 3.1 Webhook Security

- Semua request dari Meta **WAJIB** divalidasi menggunakan `App Secret` untuk
  memastikan integritas dan otentikasi pengirim.
- Rate limiting pada endpoint webhook untuk mencegah DDoS.

### 3.2 Data Privacy (UU PDP / GDPR)

- **Encryption at Rest**:
  - Pesan disimpan di DB dengan enkripsi kolom (misal: AES-256) untuk data
    sensitif.
  - Kunci enkripsi dirotasi secara berkala.
- **PII Handling**:
  - Nomor telepon dan nama disamarkan (masked) di log sistem aplikasi (e.g.,
    `+62812***`).
- **Media Handling**:
  - File dokumen/gambar tidak disimpan di server publik.
  - Menggunakan _Presigned URL_ dengan masa berlaku terbatas (misal: 15 menit)
    untuk akses lawyer via dashboard.
  - Media di server Meta akan dihapus otomatis setelah 30 hari (policy Meta),
    kita harus mendownloadnya segera saat webhook masuk.

## 4. Scalability Strategy

- **Stateless Gateway**: Service gateway dapat di-scale horizontal (Kubernetes
  ReplicaSet) untuk menangani lonjakan trafik.
- **Async Processing**: Pemrosesan berat (OCR dokumen, AI analysis) dilakukan
  oleh worker terpisah via Queue, tidak memblokir HTTP response ke Meta.

Berikut **isi dokumen lanjutan: `05_Event_Bus_and_Async_Workflow.md`**, secara **rapih, mendalam, dan siap untuk dokumentasi + implementasi** dengan konteks integrasi WhatsApp di *Lawyers-Hub*.

---

```markdown
# 📘 05_Event_Bus_and_Async_Workflow.md  
## Event Bus & Asynchronous Workflow — WhatsApp Integration  
*Version: 1.0 | Last Updated: 2026-01-05*

---

## 🎯 Tujuan Dokumen

Dokumen ini menjelaskan secara terperinci **arsitektur event bus / asynchronous workflow** untuk memproses event WhatsApp di *Lawyers-Hub*, termasuk:

✔ Alasan penggunaan message queue  
✔ Skema event yang distandarisasi  
✔ Pola “consumer + publisher”  
✔ Strategi retry & dead-letter  
✔ Observability metrics  
✔ Integration dengan core domain

Asynchronous workflow ini membantu:
- merespon webhook dengan **200 OK dalam <200ms**  
- menghindari blocking processing  
- mengatasi **duplicate events** secara efektif  
- menjaga stabilitas saat beban tinggi

Referensi praktik asynchronous webhook integration yang efektif untuk WhatsApp menunjukkan pentingnya *queue-based processing*, karena webhook harus **mengakui cepat dan memproses payload di luar request cycle** untuk menghindari retry dan duplikasi dari provider. :contentReference[oaicite:0]{index=0}

---

## 📌 1️⃣ Motivasi Asynchronous Architecture

### 💡 Kenapa asynchronous?

- **Webhook harus cepat ack (200 OK)** supaya Meta/WhatsApp tidak retry berkali-kali. :contentReference[oaicite:1]{index=1}  
- **Procese logic domain yang kompleks** (intake/AI assist) butuh waktu yang lebih lama → tidak cocok dilakukan langsung di webhook handler.  
- **Skalabilitas** & fault tolerance lebih baik dengan queue. :contentReference[oaicite:2]{index=2}

> “Proses webhook secara asynchronous ... - simpan event dulu, lalu proses event nanti.” :contentReference[oaicite:3]{index=3}

---

## 📍 2️⃣ Event Bus — Pilihan Arsitektur

Implementasi utama:
- **Broker:** **Redis + BullMQ** (untuk Node.js/TypeScript stack).
- **Workers / Consumers:** Layanan mikro yang terpisah, membaca event dari BullMQ queues.

### 🧱 Queue Configuration & Partitioning
| Parameter | Value | Reason |
|-----------|-------|--------|
| `attempts` | 5 | Mengatasi network hiccups sementara |
| `backoff` | Exponential (delay: 1000ms) | Menghindari overloading provider saat error |
| `concurrency` | 10-50 per worker | Mencegah overload ke DB/AI API |
| `removeOnComplete` | true (or store 1000 last) | Menghemat memori Redis |
| `priority` | High (1) to Low (10) | OTP > Status Update > Inbound |

### 🏢 3. Multi-tenant Partitioning
Untuk menjaga isolasi dan performa antar tenant:
- **Tenant-specific Queues:** Setiap tenant besar (Firma Hukum besar) mendapatkan queue terpisah untuk mencegah *noisy neighbor effect*.
- **Priority Queues:** Gunakan sub-queue untuk pesan dengan prioritas tinggi (e.g., OTP, Emergency Legal Aid).
- **Poison Message Handling:** Jika pesan gagal diproses > 3 kali karena logic error (bukan transient), tandai sebagai "Poison" dan pindahkan ke DLQ dengan anotasi error detail.

---

## 🔒 4. Consumer Resilience & Idempotency

### 🔌 Circuit Breaker Integration
Jika downstream service (misal: WhatsApp API atau AI Provider) sedang mengalami gangguan:
- **Pause Queue:** Worker dapat mendeteksi status "Open" pada Circuit Breaker dan melakukan `pause()` pada antrean untuk mencegah kegagalan massal dan membuang-buang jatah retry.
- **Auto-Resume:** Setelah Circuit Breaker kembali ke status "Closed", worker melanjutkan (`resume()`) pemrosesan.

### 🆔 Consumer-Level Idempotency
Meskipun Gateway melakukan deduplikasi, worker **WAJIB** melakukan pengecekan idempotensi ulang sebelum mengeksekusi business logic:
1. Gunakan `waMessageId` sebagai kunci unik di database bisnis.
2. Jika record dengan ID tersebut sudah ada, anggap sukses dan abaikan (no-op).
3. Ini krusial untuk menangani kasus di mana worker mati tepat setelah memproses data tapi sebelum mengirim acknowledgement ke broker (Redis).

### 🧱 Komponen

```

Webhook Gateway (enqueue)  →  Event Bus / Message Queue
├─ Consumer: Intake Service
├─ Consumer: Normalizer / Parser
├─ Consumer: AI Assist (read only)
└─ Consumer: Messaging Service

````

🧠 Pola ini memastikan **decoupling** antara penerimaan event dan pemrosesan yang memerlukan sumber daya lebih besar. :contentReference[oaicite:4]{index=4}

---

## 📌 3️⃣ Event Types & Schema

Berikut jenis event yang diproduksi oleh **Message Ingestor / Normalizer**:

### ✅ Standard event contract

```ts
type EventType =
  "MessageReceived"
  | "IntakeUpdated"
  | "OutboundRequested"
  | "TimeEntrySuggested"
  | "OutboundStatusUpdate";
````

### 🧱 Event payload structure

```ts
{
  eventType: string;
  eventId: string;
  normalizedMessage?: NormalizedMessage;
  metadata?: Record<string, any>;
  timestamp: string;
}
```

---

## 🧠 4️⃣ Workflow Patterns

### 🔄 Inbound Flow (async)

```plaintext
Webhook Gateway -> enqueue(Event: MessageReceived)
   ↓ ack 200 OK
Queue Worker -> process(MessageReceived)
   ↓
Normalizer/Intake Service
   ↓
emit Event: IntakeUpdated
```

Ini memisahkan **acknowledgement** dari **business processing**.

---

## 🔁 5️⃣ Retry & Dead-Letter Strategy

### 📌 Retry Policy

Jika consumer gagal memproses event:

* retry dengan **exponential backoff**
* tambah **jitter** untuk mencegah *retry storm*
  (mis. 5s, 15s, 1m, 5m, 30m) ([Technori][1])

### 🛑 Dead-Letter Queue (DLQ)

* Jika event gagal beberapa kali
* Pindahkan ke DLQ
* Notifikasi admin/operator

---

## 🧪 6️⃣ Hybrid Processing (Sync + Async)

Untuk event ringan (mis. status update sederhana):

* bisa diproses secara **hybrid**:

  * langsung diteruskan ke consumer internal
  * tetap lewat queue, tapi prioritas tinggi

Contoh:

```
status_update (delivered/read) → immediate handler
message_received (complex) → async
```

Ini sesuai praktik webhook yang direkomendasikan agar tidak memblok panggilan utama. ([docs.360dialog.com][2])

---

## 🔍 7️⃣ Observability

### � 7.1 Monitoring BullMQ (Prometheus/Grafana)
Pantau metrik berikut untuk mendeteksi bottleneck:
- `bullmq_queue_waiting`: Jumlah job yang menunggu (antrean menumpuk).
- `bullmq_queue_active`: Jumlah job yang sedang diproses.
- `bullmq_job_duration_ms`: Waktu yang dibutuhkan untuk memproses satu job.
- `bullmq_job_failed_total`: Akumulasi kegagalan job per-queue/per-tenant.

### ⏱ 7.2 Job Timeout & Cancellation
- **Job Timeout:** Set `timeout: 30000` (30 detik) untuk job AI classification. Jika lewat batas, batalkan dan log sebagai timeout error.
- **Stalled Job Handling:** Pastikan `lockDuration` diatur dengan benar agar job yang worker-nya mati mendadak dapat diambil kembali oleh worker lain.

---### 📌 Logging

* structured logs
* trace id per event
* timestamp & tenant id

---

## 📈 8️⃣ Scaling & Performance

* Worker dapat **horizontal scale** berdasarkan queue depth
* Throttling internal untuk mencegah overload downstream services
* Backpressure handling

---

## 🧠 9️⃣ Integration with Downstream Services

Contoh alur:

```
MessageReceived
   → Intake Service
      → update PreCaseSession
      → emit IntakeUpdated
         → lawyer UI polling / push
```

Setiap service subscriber di Event Bus membaca hanya event yang relevan.

---

## 🔌 10️⃣ Contract Testing

Untuk menjamin stabilitas:

* definisikan schema event
* gunakan contract tests untuk:
  ✔ enqueue/dequeue
  ✔ event payload validation
  ✔ idempotency behavior

---

## 📌 Summary

Model asynchronous menggunakan **event bus + workers** sangat penting untuk integrasi WhatsApp di Lawyers-Hub karena:

✔ memastikan webhook cepat di-ack
✔ memaksimalkan reliabilitas
✔ menyediakan retry yang bisa dikendalikan
✔ scalable saat beban tinggi

Praktik ini didukung oleh sumber best practices integrasi WhatsApp Cloud API yang menyarankan pemrosesan webhook **asynchronous dan queue-based** untuk menghindari timeout, retry storm, dan masalah duplikasi. ([todaysmm.com][3])

---

## 📎 Referensi

* WhatsApp webhook best practices (webhook async + queue) ([SMS Gateway Center][4])
* Asynchronous webhook handling guide ([docs.360dialog.com][2])
* Event bus integration patterns (message queue) ([docs.cbk.ai][5])

```

---

Jika format ini sudah cocok dan komprehensif, saya siap lanjut ke:

➡️ **06_AI_Assist_Integration_Policy.md**

Cukup jawab **lanjut**.
::contentReference[oaicite:11]{index=11}
```

[1]: https://technori.com/news/webhook-architecture-real-time-integrations/?utm_source=chatgpt.com "Webhook architecture patterns for real-time integrations"
[2]: https://docs.360dialog.com/partner/integrations-and-api-development/integration-best-practices/best-practices-for-designing-integrations/design-a-stable-webhook-receiving-endpoint?utm_source=chatgpt.com "Design a Stable Webhook Receiving Endpoint | 360Dialog"
[3]: https://www.todaysmm.com/en/blog/whatsapp-api-business?utm_source=chatgpt.com "WhatsApp Business API: Webhooks, Security & Scalable Bot Architecture"
[4]: https://www.smsgatewaycenter.com/blog/whatsapp-business-api-webhooks-real-time-integration-guide/?utm_source=chatgpt.com "WhatsApp Business API Webhooks: Real-time Integration Guide – SMSGatewayCenter Blog"
[5]: https://docs.cbk.ai/whatsapp-integration?utm_source=chatgpt.com "WhatsApp Integration"

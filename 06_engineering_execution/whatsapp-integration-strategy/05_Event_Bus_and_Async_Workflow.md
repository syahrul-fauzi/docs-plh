# Event Bus & Async Workflow

## 1. Latar Belakang

Integrasi WhatsApp membutuhkan responsivitas tinggi (webhook harus di-ack dalam
<3 detik). Pemrosesan sinkron (langsung ke DB/AI) akan menyebabkan timeout dan
kegagalan webhook.

## 2. Arsitektur Event-Driven

Kami menggunakan pola **Producer-Consumer** dengan Message Queue (RabbitMQ atau
Redis Streams).

### 2.1 Topics / Queues

| Queue Name               | Producer         | Consumer         | Deskripsi                                           |
| :----------------------- | :--------------- | :--------------- | :-------------------------------------------------- |
| `wa.incoming.raw`        | WA Gateway       | Ingestor Service | Pesan mentah dari Webhook. Prioritas TINGGI.        |
| `wa.incoming.normalized` | Ingestor         | Core Service     | Pesan bersih siap diproses bisnis logic.            |
| `wa.outgoing.command`    | Core / AI        | WA Gateway       | Perintah kirim pesan ke user.                       |
| `wa.media.processing`    | Ingestor         | Media Worker     | Queue khusus untuk download/upload file besar.      |
| `wa.ai.draft.created`    | Core Service     | Lawyer Dashboard | Notifikasi ke lawyer bahwa ada draft respon baru.   |
| `wa.ai.draft.approved`   | Lawyer Dashboard | Core Service     | Trigger untuk mengirim draft yang sudah di-approve. |

## 3. Workflow Detail

### 3.1 Inbound Flow (Async)

1. **Gateway** menerima POST Webhook.
2. **Gateway** push payload ke `wa.incoming.raw`.
3. **Gateway** return HTTP 200 OK ke Meta (selesai dalam <100ms).
4. **Ingestor Worker** pull dari `wa.incoming.raw`.
5. **Ingestor** melakukan normalisasi & download media.
6. **Ingestor** push ke `wa.incoming.normalized`.
7. **Core Service** pull, simpan ke DB, dan trigger AI Logic.

### 3.2 Outbound Flow (Throttling)

1. **Core Service** ingin kirim broadcast ke 1000 user.
2. **Core Service** push 1000 event ke `wa.outgoing.command`.
3. **WA Gateway** consume satu per satu dengan **Rate Limiter**.
    - Meta Limit: misal 80 pesan/detik.
    - Gateway menahan kecepatan agar tidak kena ban/limit.

## 4. Resilience

- **Dead Letter Queue (DLQ)**: Jika pesan gagal diproses (misal format JSON
  rusak), pindahkan ke DLQ untuk inspeksi manual, jangan block queue utama.
- **Retry Policy**: Retry 3x dengan exponential backoff untuk error transient
  (misal koneksi DB putus).

Berikut **lanjutan isi file `03_WhatsApp_Gateway_Blueprint.md`** secara **rapih, mendalam, dan siap dijadikan dokumen referensi teknis** untuk implementasi integration layer WhatsApp di *Lawyers-Hub*.

---

````markdown
# 📘 03_WhatsApp_Gateway_Blueprint.md  
## WhatsApp Webhook Gateway — Blueprint Teknis  
*Version: 1.0 | Last Updated: 2026-01-05*

---

## 🎯 Tujuan Dokumen

Dokumen ini menjelaskan **arsitektur dan spesifikasi** untuk *Webhook Gateway* — yaitu komponen yang pertama menangani event dari **WhatsApp Cloud API** sebelum masuk ke sistem inti Lawyers-Hub.

Fokus utama:
✔ Security (signature verification)  
✔ Idempotency & deduplication  
✔ Event normalization  
✔ Minimal exposure of business logic  
✔ Asynchronous handoff ke core domain

Gateway ini harus:
- cepat merespons (< 200ms)
- tahan duplikasi webhook
- aman dari spoofing
- observable & auditable

---

## 📌 Terminologi Kunci

| Istilah | Definisi |
|--------|----------|
| Webhook | HTTP endpoint yang menerima event dari WhatsApp |
| Signature | HMAC SHA256 signature dari payload untuk verifikasi |
| Event | Satu unit notifikasi (pesan, status update) |
38| Idempotency key | Identifier unik untuk mencegah replay |

---

## 🛡️ 1.5 Gateway Rate Limiting & Auditing

### 🚦 Rate Limiting
Untuk melindungi layanan internal dari serangan DDoS atau spike traffic yang tidak wajar:
- **Global Limit:** Maksimal 500 requests per detik (tergantung kapasitas server).
- **Per-IP Limit:** Maksimal 50 requests per detik dari IP Meta (berdasarkan range IP resmi Meta).
- **IP Whitelisting:** Sangat disarankan untuk membatasi traffic hanya dari [range IP resmi Meta](https://developers.facebook.com/docs/whatsapp/cloud-api/support/ip-addresses/).
- **Action:** Return **429 Too Many Requests** jika limit tercapai.

### 📜 Auditing & Raw Logging
- **Raw Payload Log:** Simpan payload asli di storage terpisah (misal: S3/Object Storage) dengan enkripsi at-rest.
- **Audit Fields:** Log metadata setiap request (Timestamp, IP Origin, Signature Status, Processing Time).
- **Retention:** Maksimal 7 hari untuk debugging, kemudian auto-delete (GDPR/PDP compliance).

---

## 📍 1️⃣ Alur Kerja Gateway (High-Level)

1. Meta/WhatsApp Cloud API **POST event** ke endpoint Gateway  
2. Gateway **verifikasi signature**  
3. Gateway **deduplicate** event  
4. Gateway **sanitize & log audit**  
5. Gateway **normalize & emit** event ke ingestion layer

```mermaid
sequenceDiagram
  participant WA as WhatsApp Cloud API
  participant GW as Webhook Gateway
  participant NI as Normalizer
  participant EB as Event Bus

  WA->>GW: POST /whatsapp/webhook
  GW->>GW: verify signature
  GW->>GW: deduplicate check
  GW->>NI: send raw event
  NI->>EB: emit normalized event
  GW->>WA: 200 OK
````

---

## 📄 2️⃣ Webhook Subscription Verification

Saat pertama kali mendaftarkan webhook di Meta Developer Console, Meta akan mem-verify endpoint dengan `hub.challenge`. Gateway **harus mengembalikan challenge token** sebagai respons:

**Pattern:**

```
GET /webhook?hub.mode=subscribe
           &hub.verify_token=<VERIFY_TOKEN>
           &hub.challenge=<CHALLENGE>
```

Respons:

```
HTTP 200
<CHALLENGE>
```

Ini adalah langkah verifikasi dasar yang diperlukan untuk WhatsApp Cloud API Webhook setup (mirip dengan pola Graph API webhook). ([Stack Overflow][1])

---

## 🔐 3️⃣ Signature Verification (Keamanan Utama)

### 🔎 Konteks

WhatsApp menyertakan signature header (`X-Hub-Signature-256`) dengan setiap event untuk menjamin asal event. ([apiwsp.com][2])

### 🛠 Cara Verifikasi

1. Ambil raw body payload (BYTE / Buffer)
2. Hash dengan app secret (HMAC-SHA256)
3. Bandingkan hash dengan header signature
4. Gunakan **constant time comparison** untuk menghindari timing attack

**Contoh Node.js (konseptual):**

```ts
function verifySignature(rawBody, headerSignature, appSecret) {
  const computed = crypto
    .createHmac('sha256', appSecret)
    .update(rawBody)
    .digest('hex');

  return crypto.timingSafeEqual(
    Buffer.from(headerSignature, 'hex'),
    Buffer.from(computed, 'hex')
  );
}
```

### ⚠️ Aturan Gateway

✔ Signature harus diverifikasi **sebelum** parsing payload
✔ Jika gagal → return **401 Unauthorized**
✔ Tidak lanjutkan ke normalizer

---

## 🧠 4️⃣ Idempotency & Deduplication

Masalah umum webhook adalah pesan/event **terkirim ganda** karena retry dari provider (Meta).
Untuk menghindari *duplicate effect*, Gateway harus melakukan:

**Check dedup logic:**
* **Storage:** Gunakan **Redis** dengan TTL (Time To Live) minimal 24 jam.
* **Key:** `wa_dedup:{tenantId}:{wa_message_id}` (menambahkan tenantId untuk isolasi data).
* **Logic:** Jika key ada di Redis -> return **200 OK** (acknowledge) tanpa memproses ulang. Jika tidak ada -> simpan key dan lanjut proses.

---

## 🏢 4.5 Multi-tenant Inbound Routing

Karena satu gateway dapat menangani banyak firma hukum (tenants):
- **WABA mapping:** Gateway harus memiliki cache (Redis) yang memetakan `WABA_ID` atau nomor telepon tujuan ke `tenantId`.
- **Pre-routing validation:** Jika event datang dari WABA yang tidak terdaftar, Gateway harus log sebagai "Unknown Tenant" dan return **200 OK** (untuk menghentikan retry Meta) tetapi tidak meneruskan ke normalizer.

---

## 🏥 5️⃣ Health & Readiness Checks

Untuk mendukung orkestrasi container (Kubernetes/Docker):
- **GET /health:** Mengembalikan status liveness service gateway.
- **GET /ready:** Mengembalikan status readiness (termasuk koneksi ke Redis untuk dedup).

---

## 🧹 6️⃣ Sanitasi Payload & Audit Logging

Setelah verifikasi & dedup:

✔ Simpan **raw payload** di storage yang terenkripsi
✔ Log metadata:

* timestamp
* source IP
* event id
* type

Tujuan:

* audit internal
* replay jika perlu

**Teknis:**

```jsonc
{
  "event_id": "...",
  "received_at": "...",
  "raw_payload_ref": "<encrypted gateway storage reference>"
}
```

---

## 📦 6️⃣ Normalization Handoff

Setelah validasi, webhook harus **menyerahkan event ke komponen normalizer** melalui:

* Event bus
* Queue
* Internal API

**Payload minimal:**

```ts
WebhookEvent {
  eventId
  channel: "whatsapp"
  rawPayloadRef
  receivedAt
}
```

Kemudian versi normalnya:

```ts
NormalizedMessage {
  id,
  type,
  senderHash,
  contentRef,
  timestamp
}
```

---

## 🧪 7️⃣ Performance & Scalability

### 🚀 Latency

* Gateway wajib merespon **200 OK secepat mungkin**
  (backpressure / heavy logic boleh dipindah ke async)

### ⏱ Timeouts

* Selalu `2xx` untuk acknowledge
* Proses panjang di background worker

📌 Respons lambat bisa memicu retry dari WhatsApp.
Jika gagal atau timeout → meta akan resend → *duplikasi* (latency triggers retry). ([Reddit][3])

---

## 🛡 Gateway Security Checklist

| Item         | Requirement                       |
| ------------ | --------------------------------- |
| Signature    | HMAC-SHA256 + timing safe compare |
| HTTPS only   | Mandatory                         |
| Idempotency  | Event dedup store                 |
| Raw logs     | Encrypted                         |
| IP filtering | Optional whitelist                |

---

## 🧠 Gate Logic Summary

| Stage            | Action        | Output                  |
| ---------------- | ------------- | ----------------------- |
| Receive event    | POST /webhook | HTTP 200 / 401          |
| Verify signature | HMAC-SHA256   | Authenticated or reject |
| Deduplicate      | Event store   | Skip or proceed         |
| Sanitize & store | Mask raw      | Audit log               |
| Normalize        | Map fields    | emit to ingestion queue |

---

## 📌 Best Practices

✔ Response must be quickly acknowledging
✔ Process everything asynchronously after response
✔ Validate webhook fields config (messages, delivery updates)
✔ Implement alerting for frequent signature failures

---

## 📎 Referensi Teknis

* Signature & webhook verification principle (HMAC-SHA256) ([DeepWiki][4])
* Security & rate limiting best practices for webhook consumers ([API MESSAGING][5])

```

---

### Next?

Saya siap membuat **file berikutnya** dengan level yang sama, yakni:

➡️ `04_Message_Ingestor_and_Normalization.md` — mencakup schema detail, error semantics, media handling, dan retention policy.

Tinggal jawab: **lanjut**.
::contentReference[oaicite:6]{index=6}
```

[1]: https://stackoverflow.com/questions/73543318/what-is-the-request-that-whatsapp-cloud-api-does-to-verify-a-webhook?utm_source=chatgpt.com "https - What is the request that whatsapp cloud api does to verify a webhook? - Stack Overflow"
[2]: https://www.apiwsp.com/dev/?utm_source=chatgpt.com "WhatsApp Business API Documentation"
[3]: https://www.reddit.com//r/WhatsappBusinessAPI/comments/1p664jo/ghost_pings_from_whatsapp_webhook/?utm_source=chatgpt.com "Ghost Pings from WhatsApp Webhook"
[4]: https://deepwiki.com/gokapso/whatsapp-cloud-api-js/7.1-webhook-verification?utm_source=chatgpt.com "Webhook Verification | gokapso/whatsapp-cloud-api-js | DeepWiki"
[5]: https://apimessaging.com/api-docs/docs/code-examples?utm_source=chatgpt.com "WhatsApp Business API 2025 | Integration & Automation"

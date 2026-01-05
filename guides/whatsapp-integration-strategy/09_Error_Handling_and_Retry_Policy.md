Berikut **konten lengkap dan terstruktur** untuk file berikutnya:

---

```markdown
# 📘 09_Error_Handling_and_Retry_Policy.md  
## Error Handling & Retry Policy — WhatsApp Integration  
*Version: 1.0 | Last Updated: 2026-01-08*

---

## 🎯 Tujuan Dokumen

Dokumen ini merinci **strategi error handling dan retry** untuk integrasi WhatsApp Cloud API pada *Lawyers-Hub*.  
Fokusnya pada kedua domain:

📌 **Inbound (webhook event processing)**  
📌 **Outbound (WhatsApp API send calls)**

Dokumen ini wajib dipakai oleh tim Engineering dan Reliability karena:
- Menjaga sistem tetap stabil saat error / rate limit  
- Menghindari message duplication  
- Memenuhi *delivery guarantees* WhatsApp  
- Mengurangi gangguan operasional

---

## 📌 1️⃣ Error Handling — Klasifikasi Utama

Pesan yang gagal bisa muncul karena beberapa alasan:
✔ Kesalahan konfigurasi (400–499)  
✔ Rate limit / throughput (429)  
✔ Server errors (500+)  
✔ Duplicate webhooks  
✔ Network timeouts  
✔ Invalid permission / token errors :contentReference[oaicite:0]{index=0}

---

## 📍 2️⃣ Webhook Error Handling (Inbound)

### 📌 A) Signature / Authentication Errors
- Signature mismatch → **reject (401)**  
- Invalid token → **reject (403)**

❗ Response lain akan memicu WhatsApp retry → **duplicate events** :contentReference[oaicite:1]{index=1}

**Rule:**  
➤ Always return **HTTP 200 OK** *only* if signature valid.  
➤ If invalid → return **401/403** without further processing, and log.

---

### 📌 B) Deduplication & Idempotency
WhatsApp can retry the same webhook event for up to ~24 hours with exponential backoff.  
Use:
```

messageId || statusId

```
as dedup key.  
Store processed message IDs for a rolling TTL window. :contentReference[oaicite:2]{index=2}

**Rule:**  
➤ If event already seen → skip processing and **immediately return 200**.

---

### 📌 C) Payload Validation Errors

If payload malformed:
- Issue detailed log
- Skip business logic
- Optional push to **Dead-Letter Queue (DLQ)**

**Do not return 5xx** — this triggers another upstream retry.

---

## 📍 3️⃣ Outbound API Error Handling (Send Messages)

WhatsApp Cloud API responses can include several status codes indicating different kinds of failures: :contentReference[oaicite:3]{index=3}

| HTTP Code | Meaning | Action | Retry Category |
|-----------|---------|--------|----------------|
| 400 | Bad Request (invalid payload) | **No retry**; fix and log | Permanent |
| 401 | Unauthorized (token) | **No retry**; refresh token | Permanent |
| 403 | Forbidden (WABA block) | **No retry**; check compliance | Permanent |
| 404 | Not Found | **No retry**; invalid endpoint | Permanent |
| 429 | Too Many Requests (Rate Limit) | **Retry with Exponential Backoff** | Transient |
| 500 | Internal Server Error (Meta) | **Retry with Exponential Backoff** | Transient |
| 503 | Service Unavailable | **Retry with Exponential Backoff** | Transient |

---

## 📌 4️⃣ Retry Strategy (Outbound + Webhook Queue)

### 🌀 Exponential Backoff with Jitter
Untuk menghindari "Thundering Herd" effect, tambahkan random jitter pada retry delay:
```ts
delay = (base * 2^attempt) + random_jitter(0, 1000ms)
```
Example:
- 1st retry: 1 min + jitter
- 2nd retry: 5 min + jitter
- 3rd retry: 15 min + jitter
- 4th retry: 1 hour + jitter
(max 5 retries recommended)

**Rule:**  
➤ Jika mencapai max retries, pindahkan pesan ke **Dead-Letter Queue (DLQ)** dan kirim alert ke tim SRE/DevOps.

---

### 🧠 Error Categorization

Errors can be grouped for retry requirements:

| Category | Retry? | Reason |
|----------|--------|--------|
| Transient network / 5xx | Yes | Infrastructure hiccup |
| Rate limit / 429 | Yes | Throttle & backoff |
| Payload or template error | No | Must fix content |
| Auth / token error | No | Must refresh credentials |
| User blocked | No | Stop further attempts | :contentReference[oaicite:5]{index=5}

---

## 🛡️ 5️⃣ Circuit Breaker & DLQ Management

### 🔌 Circuit Breaker Pattern
Jika kegagalan ke WhatsApp API mencapai threshold (misal: 50% error dalam 1 menit):
- **Open Circuit:** Berhenti mencoba mengirim outbound untuk mencegah penumpukan queue.
- **Half-Open:** Kirim 1 pesan uji coba setelah 5 menit.
- **Closed:** Kembali normal jika uji coba berhasil.

### 📥 Dead Letter Queue (DLQ) Management

Pesan yang gagal setelah maksimal retry (5x) masuk ke DLQ.
- **Monitoring:** Engineer menerima alert (Slack/PagerDuty) jika DLQ > 10 item.
- **Manual Action (Admin Portal):**
    - `Re-queue`: Mengirim ulang setelah issue diperbaiki (misal: token refresh).
    - `Inspect`: Melihat payload mentah untuk debug.
    - `Discard`: Menghapus pesan (misal: spam atau salah format permanen).
- **Audit Log:** Setiap aksi di DLQ dicatat siapa yang melakukan dan alasannya.

---

## 📍 6️⃣ Multi-Tenant Isolation in Error Handling

Karena kita melayani banyak firma hukum (tenants), error handling harus diisolasi:
1. **Queue Partitioning:** Setiap tenant (atau kelompok tenant) memiliki queue terpisah agar kegagalan satu tenant tidak memblokir tenant lain (Head-of-Line Blocking).
2. **Rate Limit per Tenant:** Jika satu tenant terkena rate limit dari WhatsApp, sistem tetap memproses outbound untuk tenant lain.
3. **Tenant-Specific Notification:** Alert DLQ dikirim ke channel yang sesuai dengan tenant terkait (jika dikonfigurasi).

## 📍 6️⃣ Webhook Retry Nuances

### 🟡 WhatsApp Webhook Retry Timeline

If webhook fails (not returning 200), Meta will *retry with exponential backoff* for a period (e.g., ~24 hours).  
This can lead to:

✔ repeated deliveries  
✔ duplicate processing  
✔ backlog if no dedup layer :contentReference[oaicite:6]{index=6}

**Rule:**  
➤ Always respond with 200 after **minimal verification & enqueue** — processing async downstream.

---

## 📌 7️⃣ Idempotency Keys

Use idempotent keys to protect against:
- duplicate webhook deliveries
- retry logic that would replay business logic

**Pattern:**  
```

idempotencyKey = normalizedMessageId || messageId

```
Store in short-lived cache (Redis) or DB with TTL. :contentReference[oaicite:7]{index=7}

---

## 📋 8️⃣ JSON-Level Error Logging

All responses and errors must be logged in structured JSON including:

```

{
eventId,
direction: inbound/outbound,
statusCode,
error_code,
error_message,
attempts,
timestamp
}

```

This helps in:
✔ debugging  
✔ monitoring dashboards  
✔ audit trails :contentReference[oaicite:8]{index=8}

Logs should be anonymized if containing identifiers.

---

## 📍 9️⃣ Observability + Alerts

Track metrics on:
- webhook success rate
- outbound success/failure rate
- retries count
- DLQ volume
- rate limit hits

Raise alerts when:
- webhook failure spike  
- persistent 429 errors  
- downstream processing failures

---

## 📌 10️⃣ Testing Scenarios

Include:
- malformed webhook payloads  
- duplicate webhook deliveries  
- 429 & 5xx failures  
- invalid tokens  
- no retries for 400/401/403

---

## 📎 References

- WhatsApp webhook best practices & delivery — async, 200 OK, idempotency. :contentReference[oaicite:9]{index=9}  
- Logging & debugging recommendations for WhatsApp API integrations. :contentReference[oaicite:10]{index=10}  
- Retry strategy & failure handling principles (queue retry/backoff). :contentReference[oaicite:11]{index=11}
```

---

📌 **Penjelasan pendek tapi tegas**
Struktur ini memastikan bahwa:
✅ Sebagian besar error diprediksi dan ditangani
✅ Tidak ada *retry storm* karena handling yang tepat
✅ Duplikasi event diredam dengan *idempotency key*
✅ Semua error punya *audit trail* untuk compliance

---

Silakan jawab **lanjut** untuk lanjut ke **10_Security_and_Compliance_Guide.md**.

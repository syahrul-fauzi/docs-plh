Berikut **dokumen mendalam dan terstruktur** untuk **12_Testing_Strategy.md** — fokus pada pengujian integrasi WhatsApp Cloud API di *Lawyers-Hub*, mencakup *unit tests*, *integration tests*, *end-to-end testing*, serta kerangka *CI/CD* dan skenario error & load testing.

---

````markdown
# 📘 12_Testing_Strategy.md  
## Testing Strategy — WhatsApp Integration  
*Version: 1.0 | Last Updated: 2026-01-11*

---

## 🎯 Tujuan Dokumen

Dokumen ini merinci strategi **pengujian lengkap** untuk integrasi WhatsApp Cloud API di *Lawyers-Hub*, termasuk:

✔ Unit testing  
✔ Integration testing  
✔ End-to-End (E2E) testing  
✔ Load & performance testing  
✔ Security & compliance testing  
✔ Test environments & CI/CD  
✔ Automation & regression  

Pendekatan ini memastikan implementasi tidak hanya *berfungsi secara teknis*, tapi juga **tahan terhadap edge case, skenario error, dan skala produksi**.

---

## 📌 1️⃣ Testing Principles

Mengutip best practices dari dokumentasi integrasi API, pengujian WhatsApp integrasi harus:

- Mulai dari **sandbox environment**  
- Memvalidasi semua response dan edge cases  
- Mensimulasikan skenario error & rate limit  
- Menjalankan test dengan data yang representatif  
- Mengotomasi test suite di CI/CD pipeline :contentReference[oaicite:0]{index=0}

---

## 🧪 2️⃣ Unit Testing

### Tujuan
Memastikan **logika internal** di setiap komponen (gateway, normalizer, services) bekerja sesuai ekspektasi tanpa memanggil external API.

### Fokus
✔ Schema mapping  
✔ Normalization logic  
✔ Deduplication guard  
✔ AI assist transformation  
✔ RBAC / permission logic

### Contoh
```js
// Pseudocode: test normalization
test('normalize inbound text message', () => {
  const raw = sampleWhatsAppEvent();
  const result = normalizer(raw);
  expect(result.channel).toBe('whatsapp');
  expect(result.messageType).toBe('text');
});
````

---

## 🔗 3️⃣ Integration Testing

### Tujuan

Memastikan **komponen internal (termasuk external API calls dengan mock)** saling berinteraksi dengan benar.

### Fokus

* Webhook handler → normalizer → event bus
* Outbound template send pipeline
* Database persistence & session handling
* Contract compliance dengan WhatsApp API responses

### Tools & Pattern

* **Mock WhatsApp API responses**
* Automated collections (e.g., Postman, REST clients) ([API MESSAGING][1])
* Contract tests memastikan skema expected payload

---

## 🌐 4️⃣ End-to-End (E2E) Testing

### 🏢 A) Multi-Tenant Isolation Testing
Karena *Lawyers-Hub* adalah platform multi-tenant, E2E test harus mencakup:
1. **Data Leakage Check:** Kirim pesan dari User A (Firma Hukum 1) dan pastikan tidak muncul di Dashboard Firma Hukum 2.
2. **Configuration Isolation:** Gunakan `WHATSAPP_BUSINESS_ACCOUNT_ID` yang berbeda untuk setiap tenant dalam test suite.

### 📩 B) WhatsApp Specific Workflows
* **Template Flow:** Menguji pengiriman template dengan berbagai variabel (string, currency, date).
* **Media Intake:** Menguji pengiriman PDF/Gambar dari WhatsApp dan memverifikasi ketersediaannya di internal storage (S3/MinIO).
* **Opt-out Flow:** Mengirim keyword "STOP" dan memastikan sistem tidak mengirim template marketing lagi ke nomor tersebut.

---

## 🎭 4.5 Mocking & Chaos Strategy

### 🧱 A) Mocking Strategy
Gunakan **WireMock** atau **Nock** untuk mensimulasikan respon WhatsApp Cloud API:
- **Mock Success:** Return 200 OK dengan message ID.
- **Mock Error:** Return 429 (Rate Limit) untuk menguji retry logic.
- **Mock Webhook:** Script untuk mengirim POST payload ke gateway internal.

### 🌪️ B) Chaos Engineering Scenarios
Uji ketahanan sistem dengan:
1. **Redis Down:** Pastikan gateway tetap memberikan 200 OK dan menyimpan event ke file lokal/backup jika queue tidak tersedia.
2. **Slow Network:** Simulasi delay 5 detik pada koneksi ke WhatsApp API untuk menguji timeout.
3. **Large Payload:** Kirim dokumen 100MB melalui webhook untuk menguji stabilitas ingestor.

---

## ⚡ 5️⃣ Load & Performance Testing

### Tujuan

Mengetahui *how the system behaves under peak load*, terutama:

* webhook spikes
* many inbound messages
* heavy AI classification

### Skema

* *Spike test*: tiba-tiba jumlah event masuk sangat tinggi
* *Soak test*: load normal konstan dalam jangka waktu panjang ([Google for Developers][3])

### Tools

* **JMeter**, **Locust**, **Artillery**
* Define thresholds:

  * average processing latency
  * 95/99 percentile latency
  * queue depth under load

---

## 🔐 6️⃣ Security & Compliance Testing

### Tujuan

Memastikan integrasi tetap aman & mematuhi PDP/etika hukum, termasuk:

* signature verification
* unauthorized access
* invalid payload scenarios

### Fokus

* Simulate invalid signatures
* Test RBAC rules
* Verify log immutability and audit trails

👉 **Security tests tidak boleh dilewatkan** karena webhook exposure rentan terhadap spoofing & replay attacks ([SMS Gateway Center][4])

## 👥 9.5 User Acceptance Testing (UAT)
Sebelum rilis ke produksi, libatkan **lawyer (user internal)** untuk menguji:
1. **Intake Flow Accuracy:** Apakah pertanyaan yang diajukan sistem sudah sesuai dengan kebutuhan data awal perkara.
2. **Dashboard Usability:** Apakah notifikasi dan summary AI benar-benar membantu pekerjaan mereka.
3. **Manual Override:** Menguji kemampuan lawyer untuk mengambil alih sesi dari bot.

## 🧹 9.6 Test Data Sanitization
- **No Production Data:** Dilarang keras menggunakan data klien asli dalam lingkungan testing.
- **Mock Data Generator:** Gunakan script untuk menghasilkan data calon klien fiktif yang realistis namun aman.

---

## 🔄 7️⃣ Regression Testing

Automate regression suite untuk:

* normalizer logic
* onboarding
* AI classification path
* billing approvals

Regression harus dijalankan di setiap merge request di CI pipeline.

---

## 🛠 8️⃣ CI/CD Pipeline Integration

Masukkan test suite ke **CI/CD** sebagai mandatory step **sebelum deploy**:

```
lint → unit tests → integration tests → E2E tests → performance tests → deployment
```

Gunakan *test environments*:

* staging (sandbox WhatsApp)
* preprod (mirroring prod config tanpa data sensitif)

---

## 🔍 9️⃣ Testing Environment Setup

### A) Sandbox Environment

Use sandbox/test keys from WhatsApp BSP/provider for safe testing ([API MESSAGING][2])

### B) Mock Servers

* Mock WhatsApp Cloud API
* Mock webhook retries & status updates

### C) Database Fixtures

Use fixture data to simulate:

* conversation threads
* sessions
* edge conditions

---

## 🧾 10️⃣ Error & Edge Case Testing

Focus on scenarios like:
✔ Invalid WhatsApp payload
✔ Repeated webhook deliveries
✔ Rate limit errors
✔ Token expiration cases
✔ Outbound template rejection
✔ AI low confidence paths

Pastikan setiap case:

* ditangani sesuai error handling policy
* tercatat di log

---

## 📊 11️⃣ Test Metrics & KPIs

Pantau:

* pass rate per suite
* build break frequency
* time to fix failures
* test coverage

Automate reporting ke Slack / email.

---

## 📍 12️⃣ Collaboration & Documentation in Testing

* Dokumentasikan *test cases* dengan jelas
* Map test cases ke *requirements* (intake flows, billing, compliance)
* Include *expected outcomes*

---

## 📎 Referensi Best Practices

* Test integrations thoroughly in sandbox environment before production. ([API MESSAGING][2])
* Use webhook.site or ngrok to inspect webhook payloads and simulate scenarios. ([API MESSAGING][1])
* Validate responses and error conditions automatically. ([API MESSAGING][2])

```

---

📌 **Ringkasan Singkat:**  
Dokumen ini memastikan bahwa WhatsApp integration di *Lawyers-Hub* diuji dari semua perspektif: fungsional, integrasi, end-to-end, keamanan, performa, dan compliance.  
Pengujian ini penting karena salah konfigurasi webhook atau error handling yang tidak lengkap bisa menyebabkan sistem gagal — termasuk *retry spam*, *duplicate events*, atau *message delivery failures* — yang berpengaruh pada reliability secara keseluruhan. :contentReference[oaicite:10]{index=10}

---

Silakan jawab **lanjut** untuk melanjutkan ke **13_Rollout_and_Deployment_Checklist.md**.
::contentReference[oaicite:11]{index=11}
```

[1]: https://www.apimessaging.com/docs/whatsapp-api/api-testing?utm_source=chatgpt.com "WhatsApp Business API 2025 | Integration & Automation"
[2]: https://apimessaging.com/api-docs/docs/code-examples?utm_source=chatgpt.com "WhatsApp Business API 2025 | Integration & Automation"
[3]: https://developers.google.com/assistant/conversational/testing-best-practices?utm_source=chatgpt.com "Testing best practices  |  Conversational Actions  |  Google for Developers"
[4]: https://www.smsgatewaycenter.com/blog/whatsapp-business-api-webhooks-real-time-integration-guide/?utm_source=chatgpt.com "WhatsApp Business API Webhooks: Real-time Integration Guide – SMSGatewayCenter Blog"

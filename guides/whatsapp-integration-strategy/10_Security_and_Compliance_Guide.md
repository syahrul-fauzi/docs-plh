Berikut **konten lengkap untuk file `10_Security_and_Compliance_Guide.md`** yang disusun secara **rapih, mendalam, dan siap dokumentasi teknis**, dengan fokus pada **keamanan, privasi, dan kepatuhan regulasi** dalam integrasi WhatsApp di *Lawyers-Hub*.

---

````markdown
# 📘 10_Security_and_Compliance_Guide.md  
## Security & Compliance Guide — WhatsApp Integration  
*Version: 1.0 | Last Updated: 2026-01-09*

---

## 🎯 Tujuan Dokumen

Dokumen ini merinci **strategi keamanan dan kepatuhan (compliance)** untuk integrasi WhatsApp Cloud API ke *Lawyers-Hub*.  
Berfokus pada:

✔ Perlindungan data pribadi  
✔ Keamanan infrastruktur  
✔ Kepatuhan UU PDP Indonesia / prinsip global  
✔ Autentikasi & otorisasi  
✔ Audit trail & logging  
✔ Kebijakan akses  
✔ Risiko & mitigasi

Panduan ini wajib dibaca oleh:
- Engineering
- Security
- Legal / Compliance
- DevOps / SRE

---

## 📌 1️⃣ Prinsip Utama (Security & Compliance)

Dalam konteks hukum dan komunikasi profesional:

1. **Data Privacy First**  
   WhatsApp hanyalah *transport layer*. Konten sensitif tidak disimpan secara clear text tanpa persetujuan eksplisit dan hanya sesuai kebutuhan pemrosesan. :contentReference[oaicite:0]{index=0}

2. **Defense-in-Depth**  
   Keamanan dibangun berlapis (webhook, API, akses internal, audit log).

3. **Least Privilege Access**  
   Sistem dan user hanya diberi akses minimum yang dibutuhkan.

4. **Auditability & Traceability**  
   Semua event penting harus dicatat secara immutable dan siap untuk audit. :contentReference[oaicite:1]{index=1}

5. **Regulatory Alignment**  
   Mengikuti UU PDP (ID) dan prinsip data minimization sesuai praktik global. :contentReference[oaicite:2]{index=2}

---

## ⚖️ 1.5 Perlindungan Rahasia Jabatan Advokat (Legal Privilege)

Dalam konteks hukum Indonesia (UU Advokat), kerahasiaan komunikasi antara pengacara dan klien adalah mutlak.
- **End-to-End Integrity:** Meskipun WhatsApp menggunakan enkripsi end-to-end, sistem *Lawyers-Hub* harus memastikan bahwa data yang didekripsi di gateway tidak bocor ke pihak ketiga yang tidak berwenang.
- **Privileged Data Marking:** Pesan yang mengandung informasi sensitif hukum harus ditandai sebagai `Privileged` dalam database dan tidak boleh digunakan untuk melatih model AI internal maupun eksternal.
- **Access Logs for Privilege:** Setiap akses ke data `Privileged` harus dicatat dengan alasan akses (misal: "Review perkara oleh Senior Partner").

---

## 🔐 2️⃣ Data Privacy & Minimization

### A. Hashing & Tokenization
📌 Semua **identitas pribadi (mis. phone number)** disimpan hanya dalam bentuk hash (HMAC-SHA256) untuk identifikasi unik tanpa mengekspos nomor asli.
📌 **PII Masking:** Sebelum data dikirim ke layanan AI Assist, sistem wajib melakukan masking otomatis pada:
- Nama Orang -> `[PERSON]`
- Alamat -> `[ADDRESS]`
- Nominal Uang -> `[CURRENCY]`
- Tanggal Lahir -> `[DATE]`

### B. Data Residency & Sovereignty
Sesuai dengan **PP No. 71 Tahun 2019** dan **UU PDP**:
- **Lokasi Server:** Seluruh data elektronik yang berisi informasi hukum dan data pribadi penduduk Indonesia **WAJIB** dikelola dan disimpan di pusat data yang berlokasi di **Indonesia**.
- **Cross-border Transfer:** Pengiriman data ke luar negeri (misal: ke server AI di luar Indonesia) hanya diperbolehkan jika negara tujuan memiliki tingkat perlindungan data yang setara atau melalui persetujuan subjek data dengan kontrak standar PDP.

---

### B. Data Retention Policies

* **Raw payloads** → disimpan terenkripsi sementara (90 hari)
* **Normalized & domain data** → disimpan sesuai retensi minimal compliance
* **Audit logs** → disimpan sesuai kebutuhan hukum

Hambatan utama adalah bagaimana data tersebut dikelola saat pengguna meminta penghapusan sesuai UU PDP.

**Catatan:**
WhastApp sendiri **tidak menyimpan pesan setelah diteruskan**, sehingga bisnis perlu mengelola penyimpanan data dengan hati-hati. ([Interakt.shop][1])

---

## 🔐 2.5 Encryption & Breach Response

### A. Encryption at Rest
- **Database:** Semua tabel yang menyimpan `NormalizedMessage` atau data klien harus menggunakan Transparent Data Encryption (TDE) atau enkripsi tingkat kolom (AES-256).
- **Files:** Dokumen yang di-upload melalui WhatsApp harus disimpan di bucket terenkripsi dengan KMS (Key Management Service).

### B. Security Incident Classification
| Level | Dampak | Contoh | Respon |
|-------|--------|--------|--------|
| L1 | Low | Salah signature berkali-kali | Log & Block IP |
| L2 | Medium | Kegagalan sistemik pada 1 tenant | Notifikasi Tenant Admin |
| L3 | Critical | Kebocoran PII atau Token Meta | Notifikasi Otoritas (PDP) & User |

### C. Privacy Impact Assessment (PIA)
Setiap perubahan besar pada workflow AI atau penyimpanan data wajib melalui **PIA** untuk mengevaluasi risiko privasi subjek data sesuai standar ISO/IEC 29134.

### D. Data Breach Response Plan (WhatsApp Context)
1. **Detection:** Alert otomatis jika ada akses tidak sah ke Webhook Gateway atau Database.
2. **Containment:** Cabut `System User Access Token` di Meta Business Suite jika terjadi kebocoran token.
3. **Notification:** Jika data PII bocor, notifikasi wajib dikirim ke subjek data dalam waktu maksimal 3x24 jam sesuai UU PDP.
4. **Audit:** Melakukan forensik menggunakan audit logs yang disimpan secara immutable.

---

## 🔐 3️⃣ Infrastructure Hardening

### A. HTTPS & TLS

Semua endpoint menerima traffic hanya melalui HTTPS.
Pastikan TLS **≥ 1.2 atau 1.3** dengan cipher suite modern. ([SMS Gateway Center][2])

### B. Webhook Origin Validation

* Validasi signature Meta (`X-Hub-Signature-256`)
* Bandingkan dengan HMAC yang dihitung oleh server
  Ini mencegah spoofing dan injection dari pihak tidak berwenang. ([SMS Gateway Center][2])

### C. IP Whitelisting

Rekomendasi: whitelist IP ranges resmi dari WhatsApp/Meta untuk port webhook. ([Sent][3])

### D. Secret Management & Token Rotation

* **Secret Storage:** Jangan pernah menyimpan `WHATSAPP_ACCESS_TOKEN` atau `WEBHOOK_VERIFY_TOKEN` dalam environment variable biasa atau source code. Gunakan **AWS Secrets Manager**, **HashiCorp Vault**, atau **Azure Key Vault**.
* **Rotation:** Implementasikan rotasi otomatis untuk System User Access Token setiap 60-90 hari.
* **Least Privilege:** Token yang digunakan oleh Gateway hanya boleh memiliki izin `whatsapp_business_messaging` dan `whatsapp_business_management`.

---

## 🛡️ 3.5 Security Checklist for Developers

Sebelum deploy perubahan ke WhatsApp Integration, pastikan:
- [ ] Apakah ada PII yang bocor ke console log?
- [ ] Apakah webhook signature sudah divalidasi dengan `crypto.createHmac`?
- [ ] Apakah payload size dibatasi (max 16MB untuk attachment)?
- [ ] Apakah rate limiting sudah aktif untuk endpoint webhook?
- [ ] Apakah semua koneksi database menggunakan SSL/TLS?

---

## 🛡 4️⃣ Authentication & Authorization

### A. Role-Based Access Control (RBAC)

* Hanya role tertentu yang diizinkan:

  * approve invoice
  * review intake
  * override AI suggestion

Session & permission checks wajib dilakukan *server-side*.

### B. Multi-Factor Authentication (MFA)

Disarankan untuk:

* Admin account
* DevOps account
* Roles with audit privileges ([pancake.id][4])

---

## 🏛 5️⃣ Regulatory Compliance (UU PDP & Global Principles)

### A. Consent Management

Consent eksplisit harus dicatat untuk:

* WhatsApp communications
* Data processing
* Billing notifications
  Ini memperkuat dasar hukum pemrosesan data pribadi sesuai UU PDP dan GDPR-like standards. ([Interakt.shop][1])

### B. Data Subject Rights

Implementasikan mekanisme untuk:

* access
* correct
* delete
* withdraw consent

Sesuai prinsip umum PDP dan UU ITE. ([Liputan6][5])

---

## 🧠 6️⃣ Audit Logging & Immutability

### A. Audit Trail Requirements

Setiap aksi penting harus dicatat:

```
{
  actor,
  action,
  timestamp,
  object reference,
  previous state,
  new state
}
```

### B. Append-Only Log Storage

Tidak boleh ada update/delete pada log.
Jika perlu koreksi, buat *log koreksi terpisah*. ([ChatArchitect][6])

---

## 🔍 7️⃣ Threat Modeling & Risk

### A. Common Threats

| Threat              | Mitigation                     |
| ------------------- | ------------------------------ |
| Phishing / spoofing | webhook signature verification |
| Unauthorized access | RBAC + MFA                     |
| DDoS                | rate limiting + CDN protection |
| Data leak           | encryption + hashing           |
| Phone enumeration   | hashed identifiers             |

**Risiko lainnya: phishing & malware dalam pesan WhatsApp** juga perlu diperhatikan sebagai bagian dari operasi keamanan. ([ivosights.com][7])

---

## 🧾 8️⃣ Incident Response & Monitoring

* Alert jika:

  * frequent webhook failures
  * unusual access patterns
  * signature mismatches
* Log retention & review workflow
* Prepare incident response playbook

---

## 🧪 9️⃣ Testing & Validation

### Test Types

* Contract tests for webhook schema
* Security tests:

  * signature bypass
  * replay detection
  * token management
* Penetration testing

---

## 📌 10️⃣ Best Practices Summary

✔ Gunakan BSP resmi (lewat Meta / approved partners) untuk menghindari risiko compliance & security issue. ([Sprint Asia Technology][8])
✔ HTTPS + webhook signature verification wajib. ([SMS Gateway Center][2])
✔ Enkripsi data in transit & at rest. ([WatBis][9])
✔ Least privilege & RBAC. ([pancake.id][4])
✔ Hash sensitive identifiers (phone). ([Interakt.shop][1])

---

## 📎 Referensi

* Meta / WhatsApp Cloud API security best practices
* Policy guidelines Meta for business API
* Indonesia PDP / UU ITE data privacy principles

```

---

Dokumen ini menyusun **security & compliance blueprint** untuk WhatsApp di Lawyers-Hub secara holistik — dari transport layer hingga audit trail, dan dari PDP compliance hingga RBAC.

Jika format ini sesuai, saya bisa lanjut ke **11_Monitoring_and_Observability.md** — cukup jawab **lanjut** 👍
::contentReference[oaicite:19]{index=19}
```

[1]: https://www.interakt.shop/id/whatsapp-business-api/data-privacy/?utm_source=chatgpt.com "Cara Menjaga Keamanan Data Pelanggan Saat Menggunakan Integrasi API"
[2]: https://www.smsgatewaycenter.com/blog/whatsapp-business-api-webhooks-real-time-integration-guide/?utm_source=chatgpt.com "WhatsApp Business API Webhooks: Real-time Integration Guide – SMSGatewayCenter Blog"
[3]: https://www.sent.dm/resources/whatsapp-cloud-api?utm_source=chatgpt.com "WhatsApp Cloud API: Complete Implementation Guide for 2025"
[4]: https://pancake.id/blog/whatsapp-business-security-engage-at-scale-without-compromising-trust?utm_source=chatgpt.com "Pancake | The All-in-One Business Messaging Platform"
[5]: https://www.liputan6.com/tekno/read/4487837/kemkominfo-minta-whatsapp-jelaskan-kebijakan-privasi-terbaru-ke-pengguna?utm_source=chatgpt.com "Kemkominfo Minta WhatsApp Jelaskan Kebijakan Privasi Terbaru ke Pengguna"
[6]: https://www.chatarchitect.com/news/securing-custom-messaging-integrations-compliance-best-practices?utm_source=chatgpt.com "Securing Custom Messaging Integrations: Compliance Best Practices"
[7]: https://ivosights.com/read/artikel/whatsapp-business-api-kenali-risiko-keamanan-dan-cara-mengatasinya?utm_source=chatgpt.com "Kenali Risiko Keamanan WhatsApp Business API dan Cara Mengatasinya"
[8]: https://sprintasia.co.id/whatsapp-api-indonesia-why-choosing-an-official-whatsapp-api-provider-matters/?utm_source=chatgpt.com "WhatsApp API Indonesia: Why Choosing an Official WhatsApp API Provider Matters - Sprint Asia Technology"
[9]: https://watbis.com/kebijakan-privasi?utm_source=chatgpt.com "Kebijakan Privasi - Watbis | WhatsApp Business API"

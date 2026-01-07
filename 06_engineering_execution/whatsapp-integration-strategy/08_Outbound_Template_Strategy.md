Berikut **08_Outbound_Template_Strategy.md** yang sudah saya susun secara
_rapih, mendalam, dan siap dokumentasi_ untuk integrasi WhatsApp di
_Lawyers-Hub_. Dokumen ini mencakup kebijakan template, klasifikasi, mekanisme
penggunaan, kategori, dan best practices yang relevan dengan ekosistem _WhatsApp
Cloud API_ 2025/2026.

---

```markdown
# 📘 08_Outbound_Template_Strategy.md

## Outbound Template Strategy — WhatsApp Integration

_Version: 1.0 | Last Updated: 2026-01-07_

---

## 🎯 Tujuan Dokumen

Dokumen ini merumuskan **strategi lengkap penggunaan WhatsApp message
templates** untuk outbound komunikasi di _Lawyers-Hub_, termasuk:

✔ Template kategori & tujuan  
✔ Opt-in / consent requirements  
✔ Rules & best practices  
✔ Approval & category management  
✔ Alur sistem untuk send / fallback  
✔ KPI kesuksesan template  
✔ Mekanisme compliance estimate

Fokus utamanya adalah:

> memaksimalkan deliverability, menjaga compliance, dan menekan risiko penalti
> dari Meta/WhatsApp.

---

## 📌 1️⃣ Konteks & Kenapa Template Penting

WhatsApp Cloud API **memisahkan dua mode pesan**:

🔹 _Session messages_  
→ pesan bebas dalam 24-jam sejak user terakhir mengirim  
🔹 _Template messages_  
→ pesan pra-approved untuk komunikasi proaktif di luar window 24-jam
:contentReference[oaicite:0]{index=0}

**Outbound otomatis ke user yang tidak aktif >24 jam** harus _berdasarkan
template_ yang disetujui Meta. :contentReference[oaicite:1]{index=1}

---

## 📋 2️⃣ Template Kategori & Aturan

Menurut pedoman terbaru dari WhatsApp (pasca 1 Juli 2025), template dibagi
menjadi **tiga kategori utama**:

### 🔹 A) Utility Templates

Digunakan untuk pemberitahuan fungsional, non-promosi, dan relevan dengan
permintaan user.  
Contoh: pengingat jadwal konsultasi, pengumuman hukum, update status perkara.
:contentReference[oaicite:2]{index=2}

**Rules:**

- Wajib non-promotional
- Harus diminta atau relevan secara langsung dengan user
- Punya konteks yang jelas (mis. tanggal, nomor case)
  :contentReference[oaicite:3]{index=3}

⚠️ Dilarang: kampanye marketing, penawaran, upsell, atau persuasive copy.
:contentReference[oaicite:4]{index=4}

---

### 🔹 B) Marketing Templates

Template ini boleh untuk konten promosi, re-engagement, atau edukasi layanan
berbayar (mis. seminar atau konten premium komunitas), **tetapi hanya jika
opt-in eksplisit telah disetujui**. :contentReference[oaicite:5]{index=5}

**Rules:**

- Usahakan relevan dengan konteks legal/layanan
- Hindari overly promotional text yang bisa dikategorikan spam
  :contentReference[oaicite:6]{index=6}

---

### 🔹 C) Authentication Templates

Digunakan untuk verifikasi identitas, kode OTP, atau akses aman.  
Tidak boleh ada media, URL, atau emoji; parameter harus pendek (<15 karakter).
:contentReference[oaicite:7]{index=7}

Contoh:
```

“{{1}} adalah kode verifikasi Anda.”

```

---

## 📖 3.5 Template Catalog Examples (Lawyers-Hub Specific)

| Nama Template | Kategori | Isi Pesan (Sample) | Variabel |
|---------------|----------|-------------------|----------|
| `consultation_reminder` | Utility | "Halo {{1}}, pengingat jadwal konsultasi Anda besok pukul {{2}}." | 1: Nama, 2: Waktu |
| `case_status_update` | Utility | "Update: Perkara nomor {{1}} saat ini berada pada tahap {{2}}." | 1: No Case, 2: Status |
| `document_request` | Utility | "Kami memerlukan dokumen {{1}} untuk melanjutkan perkara {{2}}." | 1: Nama Dokumen, 2: No Case |
| `billing_invoice` | Utility | "Invoice {{1}} untuk layanan {{2}} telah diterbitkan." | 1: No Invoice, 2: Layanan |
| `otp_verification` | Authentication | "{{1}} adalah kode verifikasi Lawyers-Hub Anda." | 1: OTP Code |
| `legal_insight_weekly` | Marketing | "Halo {{1}}, baca insight hukum mingguan kami tentang {{2}} di sini." | 1: Nama, 2: Topik |

---

## 🛠️ 3.6 Fallback & Priority Strategy
1. **Priority Queue:** Pesan `Authentication` (OTP) masuk ke queue prioritas tinggi dengan latency < 5 detik.
2. **Internal Retry:** Coba kirim ulang hingga 3 kali (khusus error 429/5xx).
3. **Email Fallback:** Jika WhatsApp tetap gagal > 2 jam untuk kategori `Utility`, kirim notifikasi penting via Email.
4. **Log & Alert:** Catat kegagalan di dashboard Monitoring untuk tindak lanjut manual.

---

## 📌 3️⃣ Opt-in & Consent Rules (Lawyers-Hub Compliance)

📌 **Pengguna harus memberikan Opt-in TELESKOPIK** (berlapis) sesuai UU PDP:

1. **Explicit Consent:** User mencentang checkbox "Saya setuju menerima notifikasi perkara via WhatsApp" saat pendaftaran.
2. **Channel Specific:** Consent harus spesifik untuk nomor WhatsApp yang didaftarkan.
3. **Immutable Logging:** Setiap perubahan status opt-in/opt-out dicatat dalam audit log yang tidak bisa diubah.
4. **Easy Opt-out:** User bisa berhenti kapan saja dengan membalas `STOP`.

---

## 🧠 4️⃣ Template Creation & Approval

### 🛠 Proses
1. **Tulis template** sesuai aturan (nama, body, placeholder)
2. Submit ke Meta / WhatsApp Manager
3. Tunggu approval **sebelum dipakai di produksi** :contentReference[oaicite:9]{index=9}

### ⚠️ Best Practices
✔ Gunakan nama yang *clear, descriptive, professional*
✔ Hindari teks spam / overly “call-to-action” :contentReference[oaicite:10]{index=10}
✔ Placeholder harus relevan dan natural

Contoh template naming yang baik:
```

consultation_confirm_CS

````

---

## 🧱 5️⃣ Template Variable Strategy

📌 Gunakan placeholders ({{1}}, {{2}}, …) untuk:
- Nama klien
- Tanggal pengingat sidang
- Case ID reference
- Lokasi kantor

**Tips:** Gunakan data kontekstual yang nyaman dibaca user, tanpa over-personalization yang bisa dianggap spam. :contentReference[oaicite:11]{index=11}

---

## 📬 6️⃣ Outbound Template Use Cases untuk Lawyers-Hub

| Use Case | Template Category | Contoh Parameter |
|----------|------------------|------------------|
| Reminder jadwal konsultasi | Utility | {{1}} date, {{2}} time |
| Intake approved | Utility | {{1}} intake ID |
| Billing invoice status | Utility | {{1}} invoice ID |
| Premium content alert | Marketing (opt-in) | {{1}} topic, {{2}} date |
| OTP login | Authentication | {{1}} code |

---

## 🛡 7️⃣ Compliance & Quality Guardrails

### 📌 Avoid Rejection
- Jelas tujuan pesan
- Tidak promosi tersembunyi
- Relevant placeholders
- Tidak menanyakan PII secara langsung :contentReference[oaicite:12]{index=12}

### ➖ Avoid Spam Classification
- Jangan kirim banyak template dalam periode singkat
- Hindari pesan generik tanpa konteks
- Pastikan opt-in masih valid

---

## 🤖 8.1 Dynamic Selection Logic
Sistem harus secara otomatis menentukan jenis pesan yang dikirim:
```ts
if (lastInboundMessageTime < 24_HOURS) {
  sendFreeFormMessage(content);
} else {
  const template = selectApprovedTemplate(intent);
  sendTemplateMessage(template, variables);
}
````

---

## 🚫 9.1 Opt-out Management (STOP Keyword)

Khusus untuk kategori **Marketing**, sistem **WAJIB** menangani kata kunci
`STOP` atau `UNSUBSCRIBE`:

- **Immediate Action:** Jika user mengirim `STOP`, tandai `opt_out: true` pada
  profil user di database (Tenant-specific).
- **Confirmation:** Kirim satu pesan terakhir (template Utility) yang
  mengonfirmasi bahwa mereka tidak akan menerima pesan promosi lagi.
- **Enforcement:** Sistem (Event Bus) harus mem-filter pesan outbound dan
  mem-block pengiriman jika status `opt_out` aktif.
- **Global vs Tenant Opt-out:** Jika user opt-out dari satu Firma Hukum
  (Tenant), mereka tetap bisa menerima pesan dari Firma Hukum lain di platform
  Lawyers-Hub (Isolasi Tenant).

---

## 🌍 9.2 Template Localization Strategy

- **Language Detection:** Simpan preferensi bahasa user (default: `id` untuk
  Bahasa Indonesia).
- **Multi-language Templates:** Setiap template wajib memiliki versi `id` dan
  `en`.
- **Automatic Routing:** Kirim template berdasarkan `language_code` yang
  tersimpan di profil user. Jika tidak ada, gunakan default sistem.
- **Variable Formatting:** Pastikan format tanggal dan mata uang (IDR/USD)
  sesuai dengan locale user.

---

## 🧪 9️⃣ Testing & Deployment Checklist

Before activation:

- [ ] All templates approved in Meta
- [ ] Template category validated (Utility/Marketing/Auth)
- [ ] Opt-in flow integrated & tracked
- [ ] Rate limits accounted
- [ ] Logging for send & status events

---

## 📊 10️⃣ Observability & Metrics

Pantau KPI:

- **Template send success rate**
- **Delivery & read status**
- **Block / complaint rate**
- **Opt-in compliance rate**

---

## 📎 Summary – Strategy Must-Do

✔ Template types harus sesuai konteks (Utility first)  
✔ Explicit opt-in wajib dicatat  
✔ Free-form messaging hanya dalam window  
✔ Template approval sebelum deployment  
✔ Avoid spammy content for high quality score

---

## 📜 Referensi

- WhatsApp Message Template Guidelines — template categories & rules (2025
  update) :contentReference[oaicite:14]{index=14}
- WhatsApp Business API template do’s & don’ts
  :contentReference[oaicite:15]{index=15}
- Opt-in / consent rule for messaging :contentReference[oaicite:16]{index=16}
- Best practice messaging compliance :contentReference[oaicite:17]{index=17}

```

---

Dokumen ini memastikan *Lawyers-Hub* punya **strategi outbound template yang compliant, efektif, dan aman**, terutama untuk konteks legal & privacy.

Kalau sudah siap, saya bisa lanjut ke **09_Error_Handling_and_Retry_Policy.md** — cukup jawab **lanjut**.
```

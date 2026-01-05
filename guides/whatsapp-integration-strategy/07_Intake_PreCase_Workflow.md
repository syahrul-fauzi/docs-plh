Berikut **dokumen kelanjutan yang komprehensif** untuk integrasi WhatsApp dalam *Lawyers-Hub*, sesuai dengan struktur yang kita bahas. Fokusnya adalah **07_Intake_PreCase_Workflow.md** — mencakup alur intake pra-kasus yang aman, etis, dan terstruktur untuk penggunaan WhatsApp sebagai kanal pre-case.

---

```markdown
# 📘 07_Intake_PreCase_Workflow.md  
## Intake Pre-Case Workflow (WhatsApp) — Lawyers-Hub  
*Version: 1.0 | Last Updated: 2026-01-06*

---

## 🎯 Tujuan Dokumen

Dokumen ini menjelaskan secara komprehensif **end-to-end workflow intake pra-kasus** (Pre-Case) untuk pesan yang masuk melalui **WhatsApp Cloud API**.  
Fokusnya adalah:

✔ Menangkap informasi awal dari calon klien  
✔ Menjaga compliance etika profesi  
✔ Menjamin data privacy / PDP  
✔ Menyediakan struktur data yang bisa di-audit  
✔ Memberi alur yang dapat otomatis di-route ke lawyer

---

## 📌 Prinsip Utama

Dalam konteks komunitas pengacara, intake **BUKAN konsultasi hukum**.  
Ini berarti:

- WhatsApp hanya untuk **mengumpulkan data faktual awal**  
- AI hanya untuk **klasifikasi & summary**, bukan advice  
- Semua keputusan lanjut dilakukan oleh *lawyer manusia*  
- UI/UX memberikan disclaimer yang jelas

> “WhatsApp adalah *transport layer* intake — bukan final advisor.”

---

## 🧱 1️⃣ Alur End-to-End (Canvas)

```

WA Message Inbound
↓ webhook verification
Webhook Gateway
↓ normalize
Message Ingestor
↓ enqueue
Event Bus
↓ process → Intake Service
Intake Session State Machine
↳ AI Assist (read-only) for classification
↳ Lawyer Review
↓
Pre-Case Outcome
├─ reject with education
├─ schedule consultation
└─ convert to formal case

```

> Inbound WhatsApp diarahkan ke queue segera setelah verifikasi webhook, lalu diproses secara async tanpa blok siklus webhook. :contentReference[oaicite:0]{index=0}

---

## 🔍 2️⃣ Intake Session States (State Machine)

| Status | Deskripsi | Next Possible State |
|--------|-----------|---------------------|
| draft | Baru dibuat, belum ada data cukup | in_progress |
| in_progress | Mulai input informasi awal | review |
| review | Semua data dikumpulkan, siap review | closed / scheduled / promoted |
| closed | Intake ditutup (reject) | — |
| scheduled | Konsultasi dijadwalkan | — |
| promoted | Naik ke formal case | — |

---

## 👨‍⚖️ 2.6 Manual Override & Handover
- **Lawyer Override:** Lawyer memiliki wewenang penuh untuk mengubah state session secara manual (misal: dari `draft` langsung ke `review`).
- **Bot-to-Human Handover:** Jika calon klien mengetik "Bicara dengan pengacara" atau AI mendeteksi frustrasi tinggi, sistem harus segera menghentikan alur pertanyaan otomatis dan menugaskan sesi ke lawyer yang tersedia (Human-in-the-loop).

---

## 🕒 2.5 Session Timeout & Auto-Response

### 🚦 Auto-Response Policy
- **Acknowledgement:** "Terima kasih, data Anda telah kami terima. Tim kami akan meninjau informasi ini dalam waktu 1x24 jam kerja."
- **Off-Hours:** Jika pesan masuk di luar jam kerja, kirim template khusus yang menginformasikan jam operasional firma.

### ⏳ Timeout Logic
- **Idle Timeout:** Jika calon klien tidak merespon dalam 48 jam saat status `in_progress`, sistem akan otomatis mengubah status menjadi `closed` dengan alasan `timeout`.
- **Notification:** Kirim pengingat 6 jam sebelum timeout dilakukan.

---

## 🧠 3️⃣ Consent & Compliance Guardrails

### A) Consent Flow

Sebelum session lanjut, client harus secara eksplisit memberikan:

```

[ ] Saya menyetujui komunikasi via WhatsApp
dan memahami ini bukan nasihat hukum

````

Consent ini **dicatat terpisah**:

```ts
ConsentRecord {
  id
  sessionId
  type: "whatsapp_comm" | "data_processing"
  grantedAt
}
````

❗ Tanpa consent → **reject intake** (automated template message)

> Consent eksplisit ini penting untuk PDP compliance. ([apiwsp.com][1])

---

## 📋 4️⃣ Question Tree — Intake Structured

Intake menggunakan **pertanyaan bertahap** untuk mengumpulkan data objektif:

### Q1 — Fakta Dasar

* Apakah Anda saat ini sudah memiliki perkara hukum?
* Apakah Anda menghubungi mengenai kasus baru?

### Q2.5 — Conflict of Interest (Critical)
- "Siapa pihak lawan dalam perkara ini?" (Nama Lengkap / Instansi)
- "Apakah Anda pernah berkonsultasi dengan firma kami sebelumnya?"

---

## 📂 4.5 Media & Document Intake
Jika user mengirimkan dokumen (PDF/Gambar) selama intake:
- **Automatic Scanning:** Dokumen diproses oleh Media Service (virus scan + OCR jika diperlukan untuk summary).
- **Encrypted Storage:** Dokumen disimpan di storage per-tenant dengan enkripsi AES-256.
- **Reference:** Tautkan dokumen ke `PreCaseSession` sebagai `PreCaseDocument`.

---

## 🗺️ 7.5 Intelligent Routing & Availability
- **Specialty Matching:** Berdasarkan hasil klasifikasi AI (`legalDomain`), sistem merekomendasikan lawyer yang memiliki spesialisasi tersebut.
- **Availability Check:** Hubungkan dengan kalender internal firma. Jika lawyer spesialis tidak tersedia, tawarkan jadwal konsultasi terdekat.
- **Load Balancing:** Distribusikan intake secara merata (Round Robin) ke lawyer junior jika tidak ada preferensi spesifik.

---

* Apakah ada tenggat waktu hukum dalam 14 hari?

### Q4 — Lokasi

* Di mana domisili hukum?

  * Kota / Provinsi

❗ **Tidak boleh** bertanya hal yang bersifat opini keputusan hukum (mis. “apa yang harus saya lakukan?”).

---

## 📦 5️⃣ Intake Session Schema

```ts
PreCaseSession {
  id: UUID
  channel: "whatsapp"
  status: "draft" | "in_progress" | "review" | "closed" | "scheduled" | "promoted"
  requesterHash: string
  createdAt: DateTime
  updatedAt: DateTime
}
```

```ts
PreCaseAnswer {
  sessionId
  questionId
  answerValue
  answeredAt
}
```

---

## 🧪 6️⃣ AI Assist (Classification Only)

AI ini selalu **read-only** — bukan advice.

```ts
AIClassification {
  sessionId
  legalDomain: "family" | "criminal" | "civil" | ...
  urgency: "low" | "medium" | "high"
  summary: string
  confidence: number
  generatedAt
}
```

**Always include disclaimer**:

> *This classification is AI generated and not legal advice.* ([DeepWiki][2])

Jika AI confidence rendah (<70%), flag untuk **human review**.

---

## 🧾 7️⃣ Review & Routing

Setelah intake:

* Lawyer dashboard menunjukkan outline summary
* Lawyer dapat:

  * Mendeklarasikan reject dengan pesan edukasi
  * Jadwalkan konsultasi
  * Convert menjadi formal case

**Routing logic:**

```
IF urgency == high OR missing info
  → flag human review
ELSE normal processing
```

---

## 📬 8️⃣ Template Responses (WA Outbound)

Contoh template outbound setelah intake:

```
1. Intake Rejected
   “Terima kasih. Berdasarkan informasi awal, kami tidak bisa lanjut. Silakan ke sumber hukum publik.”

2. Schedule Consultation
   “Intake lengkap, silakan pilih slot waktu konsultasi.”

3. Convert to Case
   “Intake dinyatakan layak, data sudah terkirim ke tim hukum. Case formal dibuat.”
```

⚠️ Semua outbound harus:

* approved template
* opt-in consent
* respect 24-hour window

---

## 🧠 9️⃣ Edge Cases & Guardrails

### Duplication

Gunakan **senderHash** dan **messageId** untuk mencegah duplikasi sesi. ([DeepWiki][2])

### Missing Info

Jika user berhenti di tengah intake:

* Simpan state
* Kirim reminder inbound template
* Terapkan expiry policy

### Invalid or Spam

Jika message pattern menunjukkan spam:

* auto reject
* log risk score

---

## 🔐 10️⃣ Logging & Audit

* Semua session changes dicatat:

  * old status
  * new status
  * actor
  * timestamp
* Immutable log (append-only)
* Log siap ditampilkan di compliance dashboard

---

## 🧪 11️⃣ Testing Scenarios

| Test Case                 | Expected Outcome                |
| ------------------------- | ------------------------------- |
| User sends unrelated text | system ask structured questions |
| User does not consent     | session rejected                |
| Multi-message intake      | normalize & merge               |
| AI low confidence         | flag human review               |
| Duplicate webhook         | ingest dedup                    |

---

## 📌 12️⃣ Summary

Intake Pre-Case Workflow dijaga agar:

* aman secara privasi & etika
* terstruktur untuk routing lawyer
* audit-ready dan observable
* scalable dengan event bus + webhook

Teknik yang digunakan:

* hashed identifiers
* async queue
* question tree
* AI classification only

---

## 📎 Referensi

WhatsApp webhook & signature verification basics (HMAC-SHA256) dari WhatsApp Cloud API docs dan integrasi best practices. ([DeepWiki][2])

```

---

Kalau format dan detail ini sudah sesuai, saya siap lanjut ke **08_Outbound_Template_Strategy.md** — cukup jawab **lanjut**.
::contentReference[oaicite:5]{index=5}
```

[1]: https://www.apiwsp.com/dev/?utm_source=chatgpt.com "WhatsApp Business API Documentation"
[2]: https://deepwiki.com/gokapso/whatsapp-cloud-api-js/7.1-webhook-verification?utm_source=chatgpt.com "Webhook Verification | gokapso/whatsapp-cloud-api-js | DeepWiki"

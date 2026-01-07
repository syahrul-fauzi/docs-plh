# Kebijakan Integrasi AI Assist (AI Assist Integration Policy)

## 1. Prinsip Dasar

Sesuai dengan Foundation Lawyers Hub, AI dalam WhatsApp integration berfungsi
sebagai **Support System**, bukan Lawyer pengganti.

> **HUKUM BESI:** AI DILARANG KERAS memberikan nasihat hukum spesifik (Legal
> Advice) secara otonom. Pelanggaran terhadap ini berisiko sanksi etika dan
> hukum.

## 2. Klasifikasi Intent & Respon AI

Sistem AI (CopilotKit) harus mengklasifikasikan pesan masuk ke dalam kategori
berikut:

| Kategori Intent                                         | Tindakan AI             | Contoh Respon                                                                                                              |
| :------------------------------------------------------ | :---------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| **Legal Question** (e.g., "Apakah saya bisa menuntut?") | **BLOCKED / HANDOFF**   | "Maaf, sebagai asisten virtual saya tidak dapat memberikan nasihat hukum. Saya akan hubungkan Anda dengan pengacara kami." |
| **Intake / Pendaftaran**                                | **ALLOWED** (Guided)    | "Boleh tahu nama lengkap dan jenis masalah hukumnya?"                                                                      |
| **Scheduling**                                          | **ALLOWED**             | "Pengacara Budi tersedia besok jam 10.00. Mau dibooking?"                                                                  |
| **Status Update**                                       | **ALLOWED** (Lookup DB) | "Kasus #123 saat ini dalam tahap mediasi."                                                                                 |
| **Chit-Chat / Greeting**                                | **ALLOWED**             | "Halo! Selamat pagi."                                                                                                      |

## 3. Fitur "Human-in-the-Loop" (Draft Mode)

Untuk pertanyaan yang kompleks namun bukan legal advice fatal, AI dapat
menggunakan **Draft Mode**:

1. User bertanya.
2. AI men-generate _usulan jawaban_.
3. Jawaban TIDAK dikirim ke User, tapi masuk ke **Lawyer Dashboard** sebagai
    "Draft".
4. Lawyer me-review, edit (jika perlu), dan klik **Approve**.
5. Pesan terkirim ke User.

## 4. Transparansi & Disclaimer

- **Initial Greeting**: "Saya adalah asisten virtual Lawyers Hub." (Harus jujur
  bahwa ini bot).
- **Watermark**: Jika mengirim dokumen draft, harus ada watermark "DRAFT - AI
  GENERATED".
- **Disclaimer**: Pada footer pesan tertentu: "Pesan ini digenerate oleh sistem.
  Hubungi profesional untuk kepastian hukum."

## 5. Kepatuhan Kebijakan Meta 2026 (CRITICAL)

Per 15 Januari 2026, Meta menerapkan aturan ketat terkait penggunaan AI di
WhatsApp Business API:

1. **Larangan Chatbot AI Umum (General-Purpose AI Ban)**:
    - Penggunaan AI bergaya "Open-ended Chat" (seperti ChatGPT murni tanpa
      batasan skope) dilarang.
    - **Solusi Lawyers Hub**: AI harus bersifat **Task-Oriented**. Setiap
      interaksi AI harus memiliki tujuan bisnis yang jelas (Intake, Scheduling,
      Status Check) dengan alur yang dapat diprediksi.
2. **Identifikasi AI**:
    - Sistem wajib memberitahu pengguna di awal sesi bahwa mereka sedang
      berinteraksi dengan AI.
3. **Human Escalation**:
    - Harus ada tombol atau kata kunci (misal: "Bicara dengan Pengacara") yang
      langsung memicu handoff ke manusia.

## 6. Implementasi "Lawyer-in-the-Loop"

Sesuai dengan `docs/00_foundation/README.md`, AI tidak boleh mengambil keputusan
hukum. Implementasi teknisnya:

- **Filter Output**: Menggunakan modul `PromptGuardService` (di
  `apps/ai-gateway`) untuk mendeteksi jika AI mencoba memberikan nasihat hukum
  yang dilarang.
- **Draft Approval**: Semua dokumen hukum yang dihasilkan AI harus melewati
  status `PENDING_REVIEW` di dashboard pengacara sebelum bisa dikirim ke
  WhatsApp.

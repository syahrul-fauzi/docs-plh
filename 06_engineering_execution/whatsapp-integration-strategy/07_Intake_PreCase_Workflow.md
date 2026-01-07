# Alur Kerja Intake (Pre-Case Workflow)

## 1. Tujuan

Mengotomatisasi proses pengumpulan data awal calon klien (Intake) melalui
WhatsApp untuk mengurangi beban admin, namun tetap menjaga sentuhan personal.

## 2. Diagram Alur Intake

```mermaid
graph TD
    Start[User Chat: "Butuh bantuan"] --> Greet[Bot: Salam & Disclaimer]
    Greet --> Menu{Pilih Layanan}

    Menu --Konsultasi--> Form[Bot: Minta Nama & Topik]
    Menu --Cek Status--> Status[Cek DB Status Perkara]
    Menu --Info Tarif--> Tarif[Kirim Info Umum]

    Form --> Detail[Bot: Jelaskan Kronologi Singkat]
    Detail --> Upload[Bot: Ada Dokumen Pendukung?]

    Upload --Ya--> Media[User Upload Foto/PDF]
    Upload --Tidak--> Summary[Bot: Konfirmasi Data]

    Media --> Summary
    Summary --> CreateLead[System: Create Lead di CRM]
    CreateLead --> Handover[Notifikasi ke Lawyer]
    Handover --> End[Bot: Terima kasih, Lawyer akan menghubungi]
```

## 3. Implementasi Teknis

### 3.1 Menggunakan Interactive Messages & Flows (v22.0)

Untuk mengurangi typo dan mempercepat respon, gunakan fitur interaktif WhatsApp:

- **List Messages**: Untuk memilih kategori kasus (Pidana, Perdata, Keluarga,
  Bisnis).
- **Reply Buttons**: Untuk jawaban Ya/Tidak (misal: "Apakah Anda memiliki bukti
  tertulis?").
- **WhatsApp Flows**: Untuk formulir intake yang lebih kompleks (misal: input
  alamat lengkap, detail pihak lawan, dll) dalam satu layar tanpa banyak chat
  bolak-balik.
- **Keuntungan**: User experience lebih baik, data lebih terstruktur, dan
  meningkatkan conversion rate lead hukum.

### 3.2 Single Source of Truth (CMS Integration)

Setiap interaksi intake WAJIB terintegrasi dengan Case Management System (CMS):

- **Automated Case Log:** Setiap pesan, gambar, dan dokumen yang dikirim selama
  proses intake harus secara otomatis di-attach ke file perkara (Case File) di
  CMS.
- **No Data Silos:** Dilarang menyimpan data intake hanya di gateway. Data harus
  segera di-push ke Core Database untuk visibilitas tim pengacara.
- **Audit Trail:** Catat siapa yang melakukan intake (AI) dan kapan transisi ke
  manusia (Lawyer) terjadi.

### 3.3 Data Mapping

Data yang dikumpulkan bot akan dipetakan ke objek `Lead` di database:

```json
{
  "source": "whatsapp",
  "phone": "+628123...",
  "name": "Budi Santoso",
  "case_category": "Perdata",
  "initial_notes": "Sengketa tanah di Bogor...",
  "has_documents": true,
  "status": "NEW",
  "gdpr_consent": true,
  "consent_timestamp": "2026-01-06T10:00:00Z"
}
```

### 3.3 Eskalasi

Setelah tahap Intake selesai, status percakapan berubah menjadi **"Pending
Lawyer Review"**. Bot berhenti merespon otomatis (mute) sampai Lawyer mengambil
alih atau mengirim pesan manual.

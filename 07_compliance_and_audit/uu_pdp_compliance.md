# UU PDP Compliance Framework — Lawyers Hub

## Metadata

- **Document ID**: LH-COMP-PDP-001
- **Status**: Draft v0.1
- **Owner**: Legal Counsel / DPO (Data Protection Officer)
- **Stakeholders**: Engineering, Product, Security, Management
- **Regulatory Basis**: Undang-Undang No. 27 Tahun 2022 tentang Perlindungan Data
  Pribadi (UU PDP)

---

## 1. Tujuan Dokumen

Mendefinisikan strategi Lawyers Hub untuk memenuhi kewajiban hukum di bawah
**UU PDP Indonesia**, khususnya dalam konteks pemrosesan data hukum yang
sensitif oleh sistem AI.

---

## 2. 5 Pilar Kepatuhan PDP (Lawyers Hub)

### 2.1 Dasar Pemrosesan (Legal Basis)

- **Persetujuan (Consent)**: User harus memberikan persetujuan eksplisit saat
  onboarding.
- **Kewajiban Kontrak**: Pemrosesan data diperlukan untuk pemenuhan jasa hukum
  antara lawyer dan klien.

### 2.2 Minimimalisasi Data (Data Minimization)

- AI hanya memproses data yang relevan dengan kasus hukum yang sedang ditangani.
- Penyimpanan data (retention) mengikuti standar profesi advokat (minimal 5-10
  tahun) atau sesuai permintaan penghapusan (right to erasure).

### 2.3 Hak Subjek Data (Data Subject Rights)

Sistem harus menyediakan fitur untuk:

- **Akses & Koreksi**: User dapat melihat dan mengubah data pribadi mereka.
- **Penghapusan (Erasure)**: Mekanisme "Right to be Forgotten" untuk data
  non-arsip wajib.
- **Portabilitas**: Ekspor data dalam format standar (.json / .pdf).

### 2.4 Keamanan Data (Data Security)

- **Enkripsi**: Data dienkripsi saat istirahat (AES-256) dan saat transmisi
  (TLS 1.3).
- **Anonymization & Masking**: PII (NIK, Nama, Alamat) dimask sebelum dikirim ke
  pihak ketiga (LLM Provider).
- **Data Residency**: Server dan database diutamakan berlokasi di wilayah
  Indonesia sesuai regulasi sektoral.

### 2.5 Akuntabilitas & Audit (Accountability)

- **Record of Processing Activities (RoPA)**: Log otomatis untuk setiap akses
  dan modifikasi data.
- **Data Protection Impact Assessment (DPIA)**: Dilakukan setiap ada perubahan
  arsitektur AI yang signifikan.

---

## 3. Penanganan Data Sensitif AI

| Tipe Data | Perlakuan | Alasan |
| :--- | :--- | :--- |
| **Identitas** | Masking | Mencegah profiling oleh AI provider |
| **Dokumen** | E2E Encryption | Kerahasiaan Advokat-Klien |
| **Log Chat** | Retention 30 hari | Keperluan tracing malpraktik AI |

---

## 4. Insiden Kebocoran Data

Prosedur standar sesuai UU PDP:

1. **Notifikasi**: Memberitahu subjek data dan otoritas dalam waktu maksimal
   3x24 jam.
2. **Mitigasi**: Isolasi tenant yang terdampak.
3. **Audit Pasca-Insiden**: Investigasi penyebab dan perbaikan sistem.

---

## 5. Status Penguncian

🚧 **Draft — Belum terkunci**

Akan dikunci setelah:

- Legal Counsel Review
- DPO Appointment & Sign-off

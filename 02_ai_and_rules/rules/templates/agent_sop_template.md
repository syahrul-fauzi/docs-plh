# 🤖 Agent SOP: [Nama Agent/Tugas]

| Dokumen ID      | [SOP-AGENT-00X]                  |
| :-------------- | :------------------------------- |
| **Target User** | Lawyer / Paralegal / Admin       |
| **Tipe Agent**  | Drafting / Research / Compliance |
| **Versi**       | 1.0                              |

---

## 1. Tujuan

_Panduan ini menjelaskan cara berinteraksi dengan [Nama Agent] untuk tugas
[Sebutkan Tugas]._

## 2. Prasyarat (Pre-requisites)

Sebelum memulai, pastikan:

1. Anda memiliki akses level [Level Akses] (misal: Pro Plan).
2. Dokumen pendukung (misal: Surat Kuasa) sudah diunggah ke Case Dashboard.

## 3. Instruksi Operasional (Step-by-Step)

### Langkah 1: Inisiasi

- Buka dashboard "Case Details".
- Klik tombol "AI Drafting".
- Pilih Template: [Sebutkan Template].

### Langkah 2: Prompt Engineering (Cara Memberi Perintah)

Gunakan format berikut untuk hasil terbaik:

> "Buatkan [Jenis Dokumen] untuk klien [Nama Klien] melawan [Pihak Lawan] dengan
> poin-poin kesepakatan berikut: [Daftar Poin]."

**Do's (Lakukan):**

- Berikan konteks spesifik.
- Sebutkan yurisdiksi (Indonesia).

**Don'ts (Jangan):**

- Jangan memasukkan data pribadi sensitif (NIK, No. Rekening) secara langsung di
  prompt (gunakan placeholder).
- Jangan meminta nasihat hukum yang bersifat opini subjektif.

### Langkah 3: Review & Validasi

Setelah Agent menghasilkan output:

1. Periksa "Compliance Badge" (Hijau/Merah).
2. Baca "Risk Score". Jika > 50%, wajib review manual mendalam.
3. Verifikasi pasal-pasal yang dikutip.

## 4. Troubleshooting

| Masalah                 | Solusi                                             |
| :---------------------- | :------------------------------------------------- |
| Agent menolak memproses | Cek apakah prompt melanggar "Global Safety Rules". |
| Hasil terlalu umum      | Tambahkan detail spesifik pada prompt lanjutan.    |
| Error "Quota Exceeded"  | Upgrade plan atau hubungi admin.                   |

## 5. Eskalasi

Jika menemukan kesalahan fatal (halusinasi hukum berat), segera laporkan melalui
tombol "Report Issue" atau email ke [support-email].

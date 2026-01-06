# Panduan Monitoring CI/CD untuk Dokumentasi

Dokumen ini menjelaskan cara memantau dan mengelola alur kerja CI/CD otomatis
untuk dokumentasi Lawyers Hub guna memastikan kualitas dan konsistensi tetap
terjaga.

## 1. Alur Kerja (Workflows)

Kami menggunakan GitHub Actions untuk memvalidasi dokumentasi setiap kali ada
perubahan. Workflow utama berada di
[docs-validation.yml](file:///home/inbox/smart-ai/lawyers-hub/.github/workflows/docs-validation.yml).

### Pemeriksaan yang Dilakukan

1. **Markdown Linting**: Memeriksa format file Markdown (header, list, line
   length, dll) menggunakan `markdownlint`.
2. **Link Checker**: Memeriksa apakah semua tautan (internal & eksternal) masih
   aktif dan benar menggunakan `lychee`.
3. **API Documentation**: Menjalankan generator `typedoc` untuk memastikan
   komentar kode (JSDoc) valid dan dokumentasi API terbaru berhasil dibuat.

## 2. Cara Memantau di GitHub

1. Buka tab **"Actions"** di repository GitHub Lawyers Hub.
2. Di sidebar kiri, pilih workflow **"Docs Validation"**.
3. Anda akan melihat daftar eksekusi terbaru.
   - ✅ **Hijau**: Berhasil. Semua standar terpenuhi.
   - ❌ **Merah**: Gagal. Klik pada eksekusi tersebut untuk melihat log detail.

## 3. Menangani Kegagalan (Troubleshooting)

### A. Gagal di Tahap `markdownlint`

- **Pesan Error**: Biasanya menunjukkan file dan nomor baris (misal:
  `docs/README.md:12 MD001/heading-increment`).
- **Solusi**: Perbaiki format di file tersebut sesuai dengan aturan yang
  dilanggar. Gunakan ekstensi Markdownlint di VS Code untuk melihat error secara
  real-time.

### B. Gagal di Tahap `Link Checker`

- **Pesan Error**: Menunjukkan URL yang rusak (misal:
  `[404] https://example.com/dead-link`).
- **Solusi**: Perbarui tautan yang rusak atau hapus jika sudah tidak relevan.

### C. Gagal di Tahap `API Documentation`

- **Pesan Error**: Biasanya terkait dengan error sintaks JSDoc atau kegagalan
  build `typedoc`.
- **Solusi**: Periksa log build untuk melihat pesan error dari
  TypeScript/TypeDoc. Pastikan semua ekspor tipe data benar.

## 4. Pelaporan dan Dokumentasi

- Hasil monitoring harus ditinjau oleh tim Engineering setiap minggu.
- Jika ada masalah sistemik dalam CI/CD (misal: API eksternal sering *timeout*),
  segera laporkan ke tim DevOps/Infrastructure.

---

Terakhir diperbarui: 2026-01-06 oleh Super Agent

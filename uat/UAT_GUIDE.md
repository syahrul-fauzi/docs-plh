# Panduan Pengujian Penerimaan Pengguna (UAT) - Lawyers Hub ⚖️

Selamat datang di fase UAT Lawyers Hub. Panduan ini dirancang untuk membantu Anda menguji aplikasi di lingkungan staging sebelum dirilis ke produksi.

## 🏁 Persiapan
1. **Akses Staging**: Buka [http://localhost:3006](http://localhost:3006).
2. **Kredensial**: Gunakan akun pengujian yang telah disediakan oleh administrator.
3. **Browser**: Gunakan Google Chrome atau Mozilla Firefox versi terbaru.

## 🧪 Skenario Pengujian Utama

### 1. Manajemen Kasus (Case Management)
- **Tujuan**: Memastikan pengguna dapat membuat, mengedit, dan melihat kasus hukum.
- **Langkah**:
  1. Login ke aplikasi.
  2. Klik tombol "New Case" di Dashboard.
  3. Isi formulir dengan data valid.
  4. Simpan dan pastikan kasus muncul di daftar kasus.

### 2. Otomasi Dokumen (Document Automation)
- **Tujuan**: Memastikan penggabungan template dan pembuatan draft PDF berjalan lancar.
- **Langkah**:
  1. Buka salah satu kasus.
  2. Pilih menu "Multi-Merge".
  3. Pilih minimal 2 template dokumen.
  4. Klik "Create Combined Document".
  5. Periksa apakah draft PDF yang dihasilkan sesuai dengan variabel kasus.

### 3. Kepatuhan & Keamanan (Compliance)
- **Tujuan**: Memastikan data sensitif (PII) terdeteksi dan dilindungi.
- **Langkah**:
  1. Unggah dokumen yang berisi data sensitif buatan (misal: nomor KTP palsu).
  2. Periksa apakah sistem memberikan peringatan atau melakukan masking secara otomatis.

## 📝 Cara Melaporkan Temuan
Jika Anda menemukan bug atau ketidaksesuaian, silakan gunakan [Formulir Laporan Bug](./BUG_REPORT_FORM.md) dan kirimkan melalui sistem ticketing internal atau email ke `qa-team@lawyers-hub.com`.

---
*Terakhir Diperbarui: 2026-01-05*

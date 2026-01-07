# Panduan Pengguna - Lawyers Hub

## Pendahuluan

Lawyers Hub adalah platform manajemen hukum berbasis AI yang dirancang untuk
membantu profesional hukum dalam mengelola kasus, menganalisis kepatuhan, dan
mengotomatisasi draf dokumen.

## Fitur Utama

### 1. Dashboard Utama

Dashboard memberikan ringkasan aktivitas terbaru, status kasus, dan metrik
performa secara real-time.

### 2. Analisis & Statistik

Fitur ini memungkinkan Anda untuk melihat penggunaan resource AI, efisiensi
kerja, dan tren kasus dalam bentuk grafik interaktif.

### 3. Monitoring Kepatuhan (Compliance)

- **PII Detection**: Secara otomatis mendeteksi informasi sensitif (Nama,
  Alamat, NIK) dalam dokumen.
- **AI Drift Detection**: Memantau akurasi model AI untuk memastikan kualitas
  draf tetap konsisten.

### 4. Manajemen Kasus

Kelola semua dokumen, komunikasi, dan timeline kasus dalam satu tempat yang
terpusat.

## Cara Penggunaan

### Memulai Aplikasi (Developer)

1. Pastikan Docker berjalan.
2. Jalankan database: `docker compose up -d db`.
3. Jalankan API: `cd apps/api && npm run dev`.
4. Jalankan Web: `cd apps/web && npm run dev`.

### Akses Dashboard

Buka browser dan navigasikan ke `http://localhost:3005/dashboard`.

## Pemecahan Masalah

- **Error 401**: Pastikan Anda sudah login melalui Clerk atau gunakan header
  bypass jika dalam mode pengujian.
- **Koneksi Database Gagal**: Periksa apakah container PostgreSQL sedang
  berjalan dengan `docker ps`.

---

© 2026 Lawyers Hub Team

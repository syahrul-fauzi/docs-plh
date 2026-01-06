# Riset Best Practices: Deployment, UAT, & Load Testing

Dokumen ini merangkum riset terbaru tentang praktik terbaik dalam siklus rilis
software, khususnya untuk platform enterprise seperti Lawyers Hub.

## 1. Best Practices Deployment (CI/CD)

- **Immutable Infrastructure**: Menggunakan Docker container untuk menjamin
  konsistensi antara environment development, staging, dan produksi.
- **Canary Releases**: Meluncurkan fitur baru ke persentase kecil pengguna
  (misal 5-10%) untuk mendeteksi error sebelum rilis penuh.
- **Automated Rollback**: Menyiapkan skrip yang dapat mendeteksi kegagalan
  (Health Check fail) dan secara otomatis kembali ke versi stabil sebelumnya.
- **Database Migrations Safety**: Selalu gunakan migrasi database yang bersifat
  "additive" untuk mendukung rilis tanpa downtime.

## 2. Efektivitas UAT (User Acceptance Testing)

- **Real-world Scenarios**: UAT harus didasarkan pada alur kerja nyata
  pengacara, bukan hanya pengetesan tombol.
- **Feedback Loop**: Gunakan tool seperti Sentry atau LogRocket di staging untuk
  melihat interaksi user secara langsung.
- **Acceptance Criteria**: Setiap fitur wajib memiliki kriteria keberhasilan
  yang disetujui oleh Product Owner.

## 3. Teknik Load Testing yang Efektif

- **Shift-Left Performance**: Jalankan load test sederhana di tahap
  development, bukan hanya di akhir siklus.
- **Realistic Data Volume**: Pastikan database staging memiliki volume data
  yang mirip dengan produksi.
- **Breakpoint Testing**: Lakukan *stress test* untuk mengetahui di titik mana
  sistem akan "patah" (crash).
- **Monitoring Integration**: Integrasikan k6 dengan Grafana/Prometheus untuk
  visualisasi metrik secara real-time.

## 4. Temuan Relevan untuk Lawyers Hub

- **Bottleneck Potensial**: PII Masking Engine menggunakan regex kompleks yang
  bisa menjadi CPU-intensive. Rekomendasi: Gunakan caching.
- **Optimasi Database**: Penggunaan RLS menambah overhead pada query.
  Rekomendasi: Pastikan semua kolom tenant_id terindeks.

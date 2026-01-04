# Lawyers Hub Deployment Guide

Panduan ini merinci langkah-langkah untuk mendeploy Lawyers Hub ke lingkungan produksi secara aman.

## 1. Persiapan Environment
Pastikan variabel berikut telah dikonfigurasi di server produksi (file `.env`):

### API & Worker
- `DATABASE_URL`: Koneksi ke PostgreSQL.
- `CLERK_SECRET_KEY`: Kunci rahasia dari dashboard Clerk.
- `STRIPE_SECRET_KEY`: Kunci rahasia dari dashboard Stripe.
- `REDIS_URL`: URL untuk BullMQ (jika menggunakan eksternal).

### Web Frontend
- `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY`: Kunci publik Clerk.
- `NEXT_PUBLIC_API_URL`: URL publik ke backend API.

## 2. Strategi Deployment (Gradual)

### Fase 1: Staging
- Deploy kode ke environment `staging.lawyershub.id`.
- Jalankan integrasi test penuh.
- Verifikasi dashboard Grafana (`ai-oversight`) menerima data dari staging.

### Fase 2: Canary Deployment (5-10% User)
- Deploy versi baru ke sebagian kecil pod/instance.
- Pantau metrik `legal_rule_violations_total` di Grafana.
- Jika tingkat pelanggaran kebijakan > 5% dibandingkan baseline, segera lakukan penghentian rilis.

### Fase 3: Full Production
- Deploy ke seluruh infrastruktur.
- Lakukan Smoke Test otomatis menggunakan skrip yang disediakan.

## 3. Integrasi CI/CD
Pipeline CI/CD telah dikonfigurasi di `.github/workflows/ci.yml` untuk menyertakan langkah-langkah berikut secara otomatis:
1. **Build & Test**: Memastikan kode dapat dikompilasi dan lulus semua unit test.
2. **Deploy**: Konfigurasi deployment di `ci.yml` menyediakan template untuk Vercel, AWS CLI, dan Kubernetes. Sesuaikan dengan target infrastruktur Anda.
3. **Smoke Test**: Menjalankan `scripts/smoke-test.sh` setelah deployment selesai.

### Konfigurasi Notifikasi
Untuk menerima notifikasi kegagalan di channel DevOps:
1. Tambahkan Secret baru di repositori GitHub dengan nama `DEVOPS_WEBHOOK_URL`.
2. Isi dengan URL webhook dari Slack, Microsoft Teams, atau Discord.
3. Pipeline akan secara otomatis mengirimkan notifikasi jika Smoke Test gagal.

## 4. Monitoring Pasca-Deploy (Checklist QA)
Pantau panel berikut di Grafana selama 24 jam pertama:
- **Metrik Kunci**:
    - `Error rates`: Cek kenaikan log error pada API.
    - `Latency`: Pastikan `legal_rule_duration_average_ms` < 2000ms.
    - `Throughput`: Pantau rate eksekusi rule per detik.
    - `Resource utilization`: Cek penggunaan CPU/RAM pada pod API & Worker.
- **Verifikasi Manual**:
    - Bandingkan performa saat Canary dengan baseline (versi stabil sebelumnya).
    - Dokumentasikan temuan dan berikan rekomendasi "Go/No-Go" untuk rilis penuh.

## 4. Persetujuan Rilis (Checklist Product Owner)
Sebelum rilis penuh (Phase 3), PO wajib memverifikasi:
- [ ] Jadwal rilis telah disetujui dan tidak bentrok dengan event bisnis utama.
- [ ] Dampak bisnis (fitur baru/perbaikan) telah dikomunikasikan ke stakeholder.
- [ ] Rencana rollback telah diuji dan tim teknis siap sedia.
- [ ] Persetujuan tertulis telah diberikan melalui sistem manajemen proyek.

## 5. Rencana Rollback
Jika ditemukan masalah kritis (misal: data leakage, downtime > 5 menit):
1. Identifikasi commit ID versi stabil sebelumnya.
2. Jalankan perintah rollback pada pipeline CI/CD:
   ```bash
   git checkout <previous-stable-sha>
   npm install
   npm run build
   # Deploy ulang
   ```
3. Verifikasi kesehatan database. Jika migrasi database bermasalah, gunakan backup snapshot terbaru.

## 6. Checklist Eksekusi Deployment

### DevOps
- [ ] Aktifkan blok deployment di `.github/workflows/ci.yml` (Vercel telah diaktifkan secara default).
- [ ] Verifikasi `VERCEL_TOKEN`, `AWS_ACCESS_KEY_ID`, dan `AWS_SECRET_ACCESS_KEY` di GitHub Secrets.
- [ ] Pastikan resource target (Vercel Project/AWS S3) sudah siap menerima build.

### QA
- [ ] Validasi `STAGING_API_URL` dan `STAGING_WEB_URL` di blok `env` job `smoke_test` pada `ci.yml`.
- [ ] Jalankan manual trigger workflow atau push ke `main`.
- [ ] Pantau log Smoke Test dan pastikan status `PASS`.

### User
- [ ] Tambahkan `DEVOPS_WEBHOOK_URL` di GitHub Secrets.
- [ ] Verifikasi notifikasi masuk ke channel (Slack/Teams/Email) jika terjadi kegagalan.

## 7. Kontak Tim
- **DevOps**: devops@lawyershub.id
- **QA**: qa@lawyershub.id
- **Product**: product@lawyershub.id

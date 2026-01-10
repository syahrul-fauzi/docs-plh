# Dokumentasi Deployment Staging

Dokumen ini menjelaskan prosedur deployment aplikasi Lawyers Hub ke lingkungan Staging menggunakan Docker Compose.

## Prasyarat

- Docker Engine & Docker Compose (v2+)
- Node.js (untuk script lokal jika perlu)
- Akses ke server staging
- File `.env.staging` yang telah dikonfigurasi

## Konfigurasi Environment

Pastikan file `.env.staging` ada di root direktori proyek. Contoh konfigurasi:

```env
POSTGRES_USER=staging_user
POSTGRES_PASSWORD=staging_secure_password_change_me
POSTGRES_DB=lawyers_hub_staging
DATABASE_URL=postgresql://staging_user:staging_secure_password_change_me@staging-db:5432/lawyers_hub_staging
REDIS_HOST=staging-redis
REDIS_PORT=6379
API_PORT=3001
WEB_PORT=3000
NEXT_PUBLIC_API_URL=http://localhost:3002/api/v1
FRONTEND_URL=http://localhost:3006
NODE_ENV=staging
```

> **Catatan:** Ganti `NEXT_PUBLIC_API_URL` dan `FRONTEND_URL` dengan domain publik atau IP server jika diakses dari luar localhost server.

## Cara Melakukan Deployment

Gunakan script helper yang telah disediakan di `scripts/deploy-staging.sh`.

### 1. Deploy Baru / Update
Untuk membangun ulang image dan menjalankan container:

```bash
./scripts/deploy-staging.sh deploy
```

Proses ini akan:
1. Membaca konfigurasi dari `.env.staging`.
2. Melakukan build Docker image untuk API dan Web (menggunakan cache jika ada).
3. Menjalankan container dengan `docker compose up -d`.
4. Membersihkan dangling images.

### 2. Menghentikan Layanan
Untuk mematikan semua layanan staging:

```bash
./scripts/deploy-staging.sh stop
```

### 3. Rollback
Jika terjadi masalah kritis pasca-deployment:

```bash
./scripts/deploy-staging.sh rollback
```

Saat ini mekanisme rollback akan mematikan layanan. Anda disarankan untuk melakukan `git checkout` ke versi stabil sebelumnya lalu menjalankan `./scripts/deploy-staging.sh deploy` kembali.

## Verifikasi Deployment

Setelah deployment sukses, verifikasi endpoint berikut:

1. **API Healthcheck**: `http://localhost:3002/api/v1/health`
2. **Web Dashboard**: `http://localhost:3005`
3. **Monitoring**: `http://localhost:9091` (Prometheus)

## Arsitektur Deployment

- **Database**: PostgreSQL 15 (Port host: 5433)
- **Cache**: Redis 7 (Port host: 6380)
- **API**: NestJS (Port host: 3002) - Menggunakan `helmet` untuk keamanan header.
- **Web**: Next.js (Port host: 3005) - Mode Standalone output.
- **Worker**: Background jobs (No public port).
- **Monitoring**: Prometheus (Port host: 9091).

## Keamanan & Pemeliharaan

### Audit Keamanan
Secara berkala, jalankan audit dependensi:
```bash
npm audit
```
*Catatan:* Pada Januari 2026, terdapat beberapa temuan *peer dependency conflict* dengan Expo 51 vs 54. Disarankan untuk **tidak** menjalankan `npm audit fix --force` secara otomatis karena dapat memecah kompatibilitas Mobile App. Lakukan update manual per paket.

### Log Rotation
Docker Compose telah dikonfigurasi untuk membatasi ukuran log guna mencegah disk penuh:
- Driver: `json-file`
- Max Size: `10m`
- Max Files: `3`

## Troubleshooting

- **Error CORS**: Pastikan `FRONTEND_URL` di `.env.staging` sesuai dengan URL tempat Web App diakses.
- **Error Koneksi DB**: Pastikan container `staging-db` `healthy` sebelum API start (sudah ditangani oleh `depends_on`).

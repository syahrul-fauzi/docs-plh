# Panduan Deployment (Staging Environment) - Lawyers Hub

Dokumen ini menjelaskan prosedur untuk melakukan deployment aplikasi Lawyers Hub
ke lingkungan staging.

## 1. Persiapan Environment

Pastikan Anda memiliki akses ke instance staging dan telah menyiapkan variabel
lingkungan berikut:

### Backend (`apps/api/.env`)

- `DATABASE_URL`: Koneksi ke database PostgreSQL staging.
- `CLERK_SECRET_KEY`: Secret key dari dashboard Clerk (Staging Instance).
- `AUDIT_LOG_ENCRYPTION_KEY`: Key 64-karakter hex untuk enkripsi log audit.
- `STRIPE_SECRET_KEY`: Stripe secret key (Test Mode).

### Frontend (`apps/web/.env.local` atau CI/CD Secrets)

- `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY`: Publishable key dari dashboard Clerk.
- `NEXT_PUBLIC_API_URL`: URL endpoint API staging.

## 2. Langkah-langkah Deployment

### A. Migrasi Database

Jalankan migrasi Prisma untuk memastikan skema database di staging sesuai dengan
kode terbaru:

```bash
npx prisma migrate deploy --schema=packages/database/prisma/schema.prisma
```

### B. Build Monorepo

Gunakan Turbo untuk melakukan build pada seluruh paket secara efisien:

```bash
npm run build
```

### C. Menjalankan Service

Gunakan process manager seperti PM2 untuk menjalankan aplikasi di server:

**Backend:**

```bash
cd apps/api
pm2 start dist/main.js --name "lawyers-hub-api-staging"
```

**Frontend:**

```bash
cd apps/web
pm2 start npm --name "lawyers-hub-web-staging" -- start
```

## 3. Verifikasi Pasca Deployment

Setelah deployment selesai, lakukan pemeriksaan berikut:

1. **Health Check**: Akses `${API_URL}/health` atau cek log PM2.
2. **Autentikasi**: Pastikan login via Clerk berfungsi di staging URL.
3. **Database**: Verifikasi data dapat dibaca dan ditulis.
4. **Audit Logs**: Pastikan log audit terenkripsi dengan benar.

## 4. Pemecahan Masalah

- **Error Enkripsi**: Pastikan `AUDIT_LOG_ENCRYPTION_KEY` sama dengan saat log
  dibuat.
- **CORS Error**: Pastikan `FRONTEND_URL` di backend sudah dikonfigurasi dengan
  URL staging yang benar.
- **Prisma Client**: Jika terjadi error tipe data, jalankan
  `npx prisma generate` sebelum build.

---

### Metadata Dokumen

- **Dibuat oleh**: World-Class Super Agent
- **Tanggal**: 2026-01-04

# Dokumentasi Teknis Fase 14: Invitation System

## Deskripsi

Fase ini mengimplementasikan sistem undangan anggota (Invitation System) yang
memungkinkan Admin Firma untuk mengundang anggota baru melalui email. Sistem
ini mencakup alur pembuatan undangan, pengiriman email, dan penerimaan
undangan oleh anggota baru.

## Komponen Utama

### 1. Backend (NestJS)

- **EmailModule & EmailService**: Layanan global untuk pengiriman email
  menggunakan `nodemailer`. Mendukung konfigurasi SMTP dan preview Ethereal
  untuk pengembangan.
- **InvitationsModule**: Mengelola logika bisnis undangan.
  - `create`: Membuat token unik, menyimpan data undangan ke database, dan
    mengirim email undangan.
  - `findByToken`: Validasi token undangan dan mengambil detail terkait.
  - `accept`: Membuat user baru di database dan mengubah status undangan
    menjadi `ACCEPTED`.
  - `revoke`: Membatalkan undangan yang masih pending.

### 2. Frontend (Next.js)

- **Accept Invitation Page**: Halaman khusus (`/auth/accept-invitation`) untuk
  anggota yang diundang untuk melengkapi profil mereka.
- **Member Management UI**: Pembaruan pada halaman Members untuk menampilkan
  daftar undangan pending dan fungsi untuk mengirim undangan baru.
- **Logo Component**: Komponen UI baru untuk branding yang konsisten.
- **Toast Notifications**: Integrasi `react-hot-toast` untuk feedback
  pengguna yang lebih baik.

## Alur Kerja (Workflow)

1. **Admin** memasukkan email dan peran di dashboard Members.
2. **Backend** membuat record `Invitation` dengan token unik dan mengirim email.
3. **User** menerima email dan mengklik link undangan.
4. **User** diarahkan ke halaman penerimaan undangan di frontend.
5. **User** memasukkan nama lengkap dan mengonfirmasi penerimaan.
6. **Backend** membuat akun user dan menandai undangan sebagai selesai.
7. **User** diarahkan ke halaman login untuk masuk ke platform.

## Konfigurasi Environment Variables

Untuk mengaktifkan pengiriman email, pastikan variabel berikut dikonfigurasi
di `apps/api/.env`:

- `SMTP_HOST`: Host server SMTP.
- `SMTP_PORT`: Port server SMTP (default: 587).
- `SMTP_USER`: Username SMTP.
- `SMTP_PASS`: Password SMTP.
- `EMAIL_FROM`: Alamat email pengirim.
- `FRONTEND_URL`: URL frontend untuk link undangan
  (default: <http://localhost:3000>).

## Keamanan & Validasi

- Token undangan menggunakan UUID v4 yang sulit ditebak.
- Undangan memiliki masa berlaku (default: 7 hari).
- Validasi peran (RBAC) memastikan hanya Admin yang bisa mengundang atau
  membatalkan undangan.
- Validasi Zod di frontend dan backend untuk konsistensi data.

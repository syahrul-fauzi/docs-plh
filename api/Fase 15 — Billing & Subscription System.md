# Dokumentasi Teknis Fase 15: Billing & Subscription System

## Deskripsi
Fase ini mengimplementasikan sistem penagihan (billing) dan manajemen langganan (subscription) menggunakan Stripe. Sistem ini memungkinkan firma hukum untuk memilih paket layanan (Free, Pro, Enterprise) dan mengelola pembayaran mereka secara mandiri.

## Komponen Utama

### 1. Database (Prisma)
- **Subscription Model**: Menyimpan status langganan, ID pelanggan Stripe, ID harga Stripe, dan masa berlaku paket. Terhubung 1-ke-1 dengan model `Tenant`.

### 2. Backend (NestJS)
- **BillingModule & BillingService**: 
  - Integrasi dengan Stripe SDK.
  - Pembuatan Checkout Session untuk proses upgrade paket.
  - Pembuatan Billing Portal Session agar pengguna bisa mengelola metode pembayaran dan membatalkan langganan di portal Stripe.
  - **Webhook Handler**: Menangani event dari Stripe (misal: `customer.subscription.updated`) secara asinkron untuk memperbarui status langganan di database lokal.
- **Security**: 
  - Menggunakan Stripe Signature Verification untuk memastikan webhook benar-benar berasal dari Stripe.
  - Memerlukan peran `FIRM_ADMIN` untuk melakukan tindakan terkait billing.

### 3. Frontend (Next.js)
- **Billing Page**: Terletak di `/dashboard/settings/billing`. Menampilkan kartu paket (pricing cards) dan status langganan saat ini.
- **Integrasi Stripe**: Mengarahkan pengguna ke Stripe Checkout untuk pembayaran yang aman dan Stripe Customer Portal untuk manajemen mandiri.

## Alur Kerja (Workflow)
1. **Admin Firma** membuka halaman Billing.
2. **Sistem** menampilkan paket yang tersedia (Free, Pro, Enterprise).
3. **Admin** mengklik "Upgrade" pada paket Pro.
4. **Backend** membuat Stripe Checkout Session dan mengembalikan URL-nya.
5. **Admin** diarahkan ke Stripe untuk melakukan pembayaran.
6. **Stripe** mengirimkan Webhook ke backend setelah pembayaran berhasil.
7. **Backend** memperbarui status langganan tenant menjadi `ACTIVE` dan paket menjadi `PRO`.
8. **Admin** diarahkan kembali ke dashboard dengan status paket yang sudah diperbarui.

## Konfigurasi Environment Variables
Pastikan variabel berikut dikonfigurasi di `apps/api/.env`:
- `STRIPE_SECRET_KEY`: API Key rahasia dari Stripe.
- `STRIPE_WEBHOOK_SECRET`: Secret key untuk memvalidasi tanda tangan webhook.

## Rencana Pengembangan Selanjutnya (Fase 16)
- Implementasi pembatasan fitur (feature flagging) berdasarkan paket langganan (misal: kuota dokumen, akses ke fitur AI tertentu).
- Notifikasi email otomatis sebelum masa langganan berakhir.

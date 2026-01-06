# Dokumentasi Teknis Fase 15: Billing & Subscription System

## Deskripsi

Fase ini mengimplementasikan sistem penagihan (billing) dan manajemen
langganan (subscription) menggunakan Stripe. Sistem ini memungkinkan firma
hukum untuk memilih paket layanan (Free, Pro, Enterprise).

## Komponen Utama

### 1. Database (Prisma)

- **Subscription Model**: Menyimpan status langganan, ID pelanggan Stripe,
  ID harga Stripe, dan masa berlaku paket.

### 2. Backend (NestJS)

- **BillingModule & BillingService**:
  - Integrasi dengan Stripe SDK.
  - Pembuatan Checkout Session untuk proses upgrade paket.
  - Pembuatan Billing Portal Session untuk manajemen mandiri.
  - **Webhook Handler**: Menangani event dari Stripe secara asinkron.
- **Security**:
  - Menggunakan Stripe Signature Verification.
  - Memerlukan peran `FIRM_ADMIN` untuk tindakan billing.

### 3. Frontend (Next.js)

- **Billing Page**: Terletak di `/dashboard/settings/billing`. Menampilkan
  pricing cards dan status langganan.
- **Integrasi Stripe**: Mengarahkan pengguna ke Stripe Checkout.

## Alur Kerja (Workflow)

1. **Admin Firma** membuka halaman Billing.
2. **Sistem** menampilkan paket yang tersedia.
3. **Admin** mengklik "Upgrade" pada paket Pro.
4. **Backend** membuat Stripe Checkout Session.
5. **Admin** diarahkan ke Stripe untuk pembayaran.
6. **Stripe** mengirimkan Webhook ke backend.
7. **Backend** memperbarui status langganan tenant.
8. **Admin** diarahkan kembali ke dashboard.

## Konfigurasi Environment Variables

Pastikan variabel berikut dikonfigurasi di `apps/api/.env`:

- `STRIPE_SECRET_KEY`: API Key rahasia dari Stripe.
- `STRIPE_WEBHOOK_SECRET`: Secret key untuk memvalidasi webhook.

## Rencana Pengembangan Selanjutnya (Fase 16)

- Implementasi pembatasan fitur (feature flagging) berdasarkan paket.
- Notifikasi email otomatis sebelum masa langganan berakhir.

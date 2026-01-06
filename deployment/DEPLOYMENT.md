# Deployment Guide - Lawyers Hub

## Strategi Deployment

Lawyers Hub menggunakan strategi **Blue-Green Deployment** untuk meminimalkan
downtime selama rilis fitur baru.

## Environment Staging

- **URL**: `https://staging.lawyershub.id`
- **Tujuan**: Verifikasi akhir sebelum produksi, UAT stakeholder.
- **Trigger**: Push ke branch `develop`.

## Langkah-langkah Deployment (Staging)

1. **Build**: Jalankan `npm run build` di root monorepo.
2. **Database Migration**: Jalankan `npx prisma db push`.
3. **Infrastructure**: Pastikan container Redis dan PostgreSQL berjalan.
4. **Verification**: Jalankan `npx ts-node scripts/verify-staging.ts`.

## Environment Produksi

- **URL**: `https://app.lawyershub.id`
- **Trigger**: Tag release di branch `main`.

## Monitoring & Rollback

- Gunakan Prometheus & Grafana untuk memantau error rate.
- Jika error rate > 5% selama 10 menit, sistem akan otomatis melakukan rollback
  ke image sebelumnya.

---

**Terakhir Diperbarui**: 2026-01-05

# Persiapan Tim & Training - Lawyers Hub

Rencana pelatihan dan pengaturan kerja tim untuk mendukung peluncuran Lawyers Hub.

## 1. Jadwal Training (3 Hari Intensif)

### Hari 1: Arsitektur & Teknologi
- **Sesi 1**: Overview Arsitektur Hybrid FSD + DDD.
- **Sesi 2**: Deep dive `apps/web` (Next.js) dan `apps/api` (NestJS).
- **Sesi 3**: Pemahaman Logic Engine di `packages/rules`.
- **Sesi 4**: Keamanan & Compliance (PII Masking, UU PDP).

### Hari 2: Operasional & Monitoring
- **Sesi 1**: Penggunaan Dashboard Grafana & Prometheus.
- **Sesi 2**: Prosedur Deployment (CI/CD Pipeline).
- **Sesi 3**: Manajemen Log (Audit Logs, Application Logs).
- **Sesi 4**: Simulasi penanganan insiden ringan.

### Hari 3: Skenario Darurat & Final Check
- **Sesi 1**: Simulasi Rollback Plan.
- **Sesi 2**: Simulasi Disaster Recovery.
- **Sesi 3**: Review Checklist Go-Live.
- **Sesi 4**: Q&A dan Sign-off Training.

## 2. Jadwal Shift Jaga (2 Minggu Pertama)
Shift dibagi menjadi 3 tim untuk mencakup 24/7:
- **Shift A (07:00 - 15:00)**: 2 Engineer + 1 QA.
- **Shift B (15:00 - 23:00)**: 2 Engineer + 1 DevOps.
- **Shift C (23:00 - 07:00)**: 1 Senior Engineer (On-call) + 1 SRE.

## 3. Kanal Komunikasi
- **Incident Room**: Slack Channel `#war-room-golive`.
- **Daily Sync**: Zoom/Teams Meeting setiap pukul 09:00 WIB selama masa transisi.
- **Eskalasi**: Gunakan PagerDuty untuk alert kritis di luar jam kerja.

---
*Terakhir diupdate: 2026-01-10*

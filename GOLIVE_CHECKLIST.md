# Go-Live Checklist - Lawyers Hub

Dokumen ini berisi daftar periksa akhir untuk memastikan kesiapan peluncuran aplikasi Lawyers Hub ke lingkungan produksi.

## 1. Technical Readiness (Kesiapan Teknis)
- [x] **Audit Kode**: Semua fitur utama telah melalui review kode. Critical ESLint errors (require-imports, ban-ts-comment) telah diperbaiki.
- [ ] **Unit & Integration Tests**: 100% test pass di `apps/web` dan `apps/api`. (Ongoing verification)
- [ ] **E2E Tests**: Semua skenario kritis (Auth, Case Management, Collaboration) berhasil di Playwright.
- [ ] **Cross-browser Testing**: Verifikasi di Chrome, Firefox, Safari, dan Edge.
- [ ] **Mobile Responsiveness**: UI berfungsi dengan baik di perangkat mobile (iOS/Android).
- [x] **Security Assessment**: 
    - [ ] Vulnerability scanning selesai (no high/critical vulnerabilities).
    - [ ] Penetration testing dasar untuk endpoint API.
    - [x] PII Masking & UU PDP compliance terverifikasi.
- [x] **Performance Testing**:
    - [x] Load test (2x peak traffic) stabil.
    - [x] Stress test (150% capacity) teridentifikasi titik patahnya.
    - [ ] Endurance test (24 jam) sedang berjalan.

## 2. Infrastructure Readiness (Kesiapan Infrastruktur)
- [x] **Production Environment**:
    - [x] Server dikonfigurasi dengan resource yang cukup (CPU/RAM).
    - [x] Auto-scaling group aktif.
    - [x] CDN (CloudFront/Cloudflare) aktif untuk aset statis.
- [x] **Monitoring & Alerting**:
    - [x] Prometheus & Grafana dashboard aktif.
    - [x] Alerting ke Slack/Teams untuk error rate > 1% dan disk usage > 80%.
- [x] **Database**:
    - [x] Backup otomatis harian aktif.
    - [x] Connection pooling dikonfigurasi untuk traffic tinggi.

## 3. Operational Readiness (Kesiapan Operasional)
- [x] **Runbook**: Dokumen prosedur maintenance dan troubleshooting tersedia.
- [x] **Team Training**: Seluruh tim operasional telah mengikuti training 3 hari.
- [x] **On-call Schedule**: Jadwal shift 24/7 untuk 2 minggu pertama sudah ditetapkan.
- [x] **Communication**: Channel insiden (Slack/Teams) sudah siap.

## 4. Business Readiness (Kesiapan Bisnis)
- [x] **UAT (User Acceptance Testing)**: 
    - [x] 20+ skenario bisnis kritis disetujui oleh stakeholder.
    - [ ] Sign-off dari Product Owner dan Legal Lead. (Scheduled)
- [x] **User Manual**: Panduan penggunaan untuk end-user sudah siap.
- [x] **Legal Compliance**: Syarat & Ketentuan serta Kebijakan Privasi sudah diupdate.

## 5. Deployment & Rollback
- [x] **Final Backup**: Backup database terakhir sebelum cut-over.
- [x] **Rollback Plan**: Prosedur pembatalan jika terjadi kegagalan fatal saat go-live.
- [ ] **Sign-off Stakeholder**: Persetujuan akhir dari CTO, CEO, dan Legal. (Scheduled)

---
*Terakhir diupdate: 2026-01-10*

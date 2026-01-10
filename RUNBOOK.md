# Operational Runbook - Lawyers Hub

Panduan praktis untuk operasional harian, maintenance, dan penanganan masalah umum.

## 1. Prosedur Maintenance Rutin
- **Update Dependencies**: Dilakukan setiap awal bulan, diikuti dengan full regression test di staging.
- **Database Optimization**: `VACUUM ANALYZE` terjadwal setiap minggu untuk menjaga performa query.
- **Log Rotation**: Pastikan log di server tidak memenuhi disk. Gunakan `logrotate` dengan kebijakan retensi 14 hari.
- **Certificate Renewal**: SSL/TLS certificate auto-renewal (Let's Encrypt) dipantau setiap 60 hari.

## 2. Monitoring & Alerting
- **Dashboard**: [Link Grafana/Datadog]
- **Metrik Kritis**:
    - **API Latency**: Harus < 200ms untuk P95.
    - **Error Rate (5xx)**: Harus < 0.1%.
    - **Memory Usage**: Alert jika > 85% konsisten selama 5 menit.
- **Kanal Notifikasi**: Slack channel `#ops-alerts`.

## 3. Skenario Troubleshooting Umum

### Masalah: API Response Time Tinggi
1. Cek utilisasi CPU/Memory di `staging-api` atau `prod-api`.
2. Periksa slow query log di database.
3. Cek latensi AI Gateway jika masalah terjadi pada fitur berbasis AI.
4. Skalakan instance secara horizontal jika load tinggi.

### Masalah: Gagal Login (Auth Issue)
1. Cek status Clerk (Identity Provider).
2. Verifikasi JWT Secret di environment variables.
3. Pastikan Redis (Session Cache) berjalan normal.

### Masalah: Dokumen Tidak Muncul/Gagal Upload
1. Verifikasi koneksi ke Storage Service.
2. Cek kuota penyimpanan tenant.
3. Periksa log `AuditInterceptor` untuk melihat jika ada penolakan akses (RBAC).

## 4. Prosedur Eskalasi
1. **Level 1 (Ops/Support)**: Investigasi awal, gunakan runbook ini.
2. **Level 2 (Backend/DevOps)**: Jika masalah teknis mendalam atau infrastruktur.
3. **Level 3 (Architect/CTO)**: Jika masalah sistemik atau kegagalan total.

---
*Terakhir diupdate: 2026-01-10*

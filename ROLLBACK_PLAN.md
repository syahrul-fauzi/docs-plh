# Rollback Plan - Lawyers Hub

Dokumen ini menjelaskan prosedur untuk mengembalikan sistem ke keadaan stabil sebelumnya jika terjadi kegagalan kritis selama atau setelah proses Go-Live.

## 1. Kriteria Rollback
Rollback akan dipicu jika salah satu kondisi berikut terpenuhi:
- Error rate aplikasi > 5% selama 15 menit berturut-turut.
- Kegagalan fungsional pada fitur kritis (misal: gagal simpan dokumen hukum).
- Kebocoran data atau celah keamanan kritis yang ditemukan pasca-deploy.
- Performa sistem menurun drastis (Response time > 5 detik).

## 2. Prosedur Rollback Step-by-Step

### Langkah 1: Penghentian Traffic
- Alihkan traffic dari load balancer ke halaman maintenance (static page).
- Matikan auto-scaling sementara untuk mencegah instansi baru dengan versi bermasalah.

### Langkah 2: Rollback Aplikasi (Frontend & Backend)
- **Container Rollback**: Revert image tag di Docker/Kubernetes ke versi stabil terakhir (tag: `stable-last-known`).
- **Frontend**: Jika menggunakan CDN, lakukan pembersihan cache (purge) setelah revert.

### Langkah 3: Rollback Database (Jika Perlu)
- **Migrasi Data**: Jika migrasi database menyebabkan masalah, jalankan script `down` pada migrasi Prisma.
- **Restore Backup**: Jika data korup, lakukan restore dari backup terakhir sebelum go-live.
    - Lokasi Backup: `/backups/pre-golive-snapshot-YYYYMMDD.sql`

### Langkah 4: Verifikasi
- Lakukan smoke test pada lingkungan produksi yang sudah di-rollback.
- Pastikan koneksi ke DB, Redis, dan AI Gateway kembali normal.

### Langkah 5: Re-enable Traffic
- Arahkan kembali traffic dari halaman maintenance ke aplikasi.
- Pantau log dan metrik selama 30 menit.

## 3. Tim Khusus Rollback
- **Lead Engineer**: Bertanggung jawab mengambil keputusan rollback.
- **DevOps Specialist**: Eksekusi teknis rollback infrastruktur.
- **Database Administrator**: Penanganan integritas data dan restore.
- **QA Lead**: Verifikasi pasca-rollback.

## 4. Pasca-Rollback (Post-Mortem)
- Lakukan analisis akar masalah (Root Cause Analysis).
- Dokumentasikan temuan dan perbaiki bug sebelum menjadwalkan ulang go-live.

---
*Terakhir diupdate: 2026-01-10*

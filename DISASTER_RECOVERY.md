# Disaster Recovery Plan - Lawyers Hub

Strategi untuk pemulihan sistem dari kegagalan total atau bencana infrastruktur.

## 1. Target Pemulihan
- **RTO (Recovery Time Objective)**: < 4 Jam (Waktu maksimal sistem offline).
- **RPO (Recovery Point Objective)**: < 15 Menit (Maksimal data yang hilang).

## 2. Strategi Backup
- **Database (PostgreSQL)**:
    - Backup otomatis harian (Full Backup) pukul 02:00 WIB.
    - WAL (Write Ahead Log) archiving setiap 10 menit ke storage eksternal (S3/Cloud Storage).
    - Retention Policy: 30 Hari.
- **Files/Documents**:
    - Replikasi lintas region pada storage bucket.
    - Versioning aktif untuk setiap dokumen hukum.
- **Konfigurasi (Environment Variables)**:
    - Disimpan di Secret Manager yang terenkripsi dan memiliki backup di Vault terpisah.

## 3. Skenario Pemulihan

### Skenario A: Kegagalan Server/Region
1. Deteksi kegagalan melalui sistem monitoring.
2. Aktivasi infrastruktur di region cadangan menggunakan Terraform/IaC.
3. Restore database dari snapshot terbaru + WAL log untuk meminimalkan data loss.
4. Update DNS records (TTL rendah) ke IP/Load Balancer region baru.

### Skenario B: Kerusakan Data/Ransomware
1. Isolasi sistem untuk mencegah penyebaran.
2. Identifikasi snapshot bersih terakhir (Last Known Good Configuration).
3. Lakukan restore database dan file ke environment baru yang bersih.
4. Verifikasi integritas data dengan script audit.

## 4. Prosedur Pengujian DR
- Simulasi pemulihan (DR Drill) dilakukan setiap 6 bulan sekali.
- Hasil pengujian didokumentasikan dalam `DR_TEST_REPORT.md`.

## 5. Kontak Darurat
- **CTO**: [Nama/Kontak]
- **SRE Lead**: [Nama/Kontak]
- **Cloud Provider Support**: [Nomor Telepon/Link Portal]

---
*Terakhir diupdate: 2026-01-10*

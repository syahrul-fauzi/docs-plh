# Dokumentasi Teknis: Monitoring Drift & Audit PII

Dokumen ini menjelaskan konfigurasi dan operasional sistem monitoring drift
otomatis serta mekanisme audit PII pada Lawyers Hub.

## 1. Monitoring Drift Otomatis (Canary Deployment)

### Konfigurasi Cron Job

- **Jadwal**: Setiap 6 jam (`0 */6 * * *`).
- **Layanan**: `ComplianceScheduler.handleAutomaticDriftMonitoring`.
- **Logic**:
  1. Mengambil semua model AI dengan status `ACTIVE`.
  2. Menjalankan evaluasi terhadap set prompt statis (**Canary Prompts**).
  3. Menghitung skor relevansi berdasarkan kata kunci yang diharapkan.
  4. Mencatat hasil evaluasi ke dalam metrik model di database.

### Mekanisme Alerting

- **Threshold Drift**: Skor < 0.75 (dihitung berdasarkan baseline 0.85 - 2σ).
- **Notifikasi**: Email dikirim ke daftar `CANARY_ALERT_RECIPIENTS` jika skor
  di bawah threshold.
- **Logging**: Semua hasil eksekusi dicatat dalam log server dengan prefix
  `📊 [CRON]`.

## 2. Audit Log PII (Masking & Access)

### Struktur Data

Sistem mencatat setiap akses ke data PII dalam tabel `PIIAuditLog` dengan
atribut:

- `userId`: Pengguna yang mengakses data.
- `piiType`: Kategori PII (e.g., PERSON, ADDRESS).
- `action`: Tindakan yang dilakukan (VIEW, DE-MASK, EXPORT).
- `isMasked`: Status apakah data ditampilkan secara masked atau plain.
- `metadata`: Informasi tambahan (IP Address, Resource ID).

### Akses & Filter

- Admin dapat melihat log audit melalui **Compliance Dashboard**.
- Tersedia fitur filter berdasarkan User ID, Tipe PII, dan Rentang Waktu.
- Data disimpan selama 90 hari (sesuai kebijakan retensi UU PDP).

## 3. Perbandingan Multi-Model

### Metrik yang Dipantau

Dashboard perbandingan menampilkan data real-time untuk:

- **Accuracy**: Ketepatan klasifikasi/generasi.
- **Precision & Recall**: Performa model dalam mendeteksi entitas hukum.
- **Latency**: Waktu respons rata-rata (ms).
- **Throughput**: Jumlah permintaan yang diproses per menit.

---

*Dokumentasi ini dikelola secara otomatis oleh @WorldClassAgent.*

# 📄 Template Laporan Deployment - STAGING

Gunakan format ini untuk setiap deployment ke lingkungan staging di Ticketing
System.

---

**[DEPLOYMENT REPORT - STAGING]**

- **Ticket ID** : LH-DEPLOY-YYYYMMDD-XXX
- **Status** : [IN_PROGRESS / SUCCESS / FAILED]
  - **IN_PROGRESS**: Deployment sedang berjalan
  - **SUCCESS**: Deployment selesai tanpa error
  - **FAILED**: Terjadi kegagalan selama proses
- **Executor** : [Nama Pelaksana]
- **Start Time** : YYYY-MM-DD HH:mm:ss (WIB)
- **Observation** :
  - **CI/CD Status**: [Success/Error] - Detail error (jika ada)
  - **Smoke Test Result**: [Passed/Failed] - Deskripsi temuan utama
  - **Monitoring Alert**: [Yes/No] - Jenis alert yang muncul
  - **New Metrics (Feedback Loop)**: [Nama Metrik] - Nilai/Observasi
- **Follow-up** : [None / Critical Fix / Scaling Needed]
  - **None**: Tidak ada tindakan lebih lanjut
  - **Critical Fix**: Perlu perbaikan segera
  - **Scaling Needed**: Perlukan penyesuaian kapasitas

---

## **Instruksi Tambahan**

1. **Lampiran**: Wajib menyertakan screenshot dashboard GitHub Actions atau log
   terminal jika status **FAILED**.
2. **Kepatuhan**: Update status tiket secara real-time untuk visibilitas tim
   pengembang dan legal.
3. **Smoke Test**: Jalankan `./scripts/smoke-test.sh` sebelum menyatakan status
   **SUCCESS**.

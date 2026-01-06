# Kriteria Penerimaan (Acceptance Criteria) - Lawyers Hub ⚖️

Sistem dianggap siap untuk rilis produksi (Go-Live) apabila memenuhi kriteria
berikut:

## ✅ Kriteria Fungsional

1. [ ] Pengguna dapat membuat kasus baru dengan sukses (100% success rate).
2. [ ] Penggabungan template menghasilkan PDF dengan format yang benar.
3. [ ] Pencarian kasus dan dokumen berfungsi dengan filter yang tepat.
4. [ ] Sistem otentikasi (Clerk) berfungsi untuk semua role (Admin, Lawyer).

## 🔒 Kriteria Keamanan & Kepatuhan

1. [ ] Deteksi PII (KTP, NPWP, Rekening) memiliki akurasi minimal 95%.
2. [ ] Kebijakan RLS memastikan isolasi data antar tenant.
3. [ ] Log audit mencatat setiap aksi penghapusan atau ekspor data sensitif.

## ⚡ Kriteria Performa

1. [ ] Waktu respon API rata-rata di bawah 300ms.
2. [ ] Beban 50 pengguna bersamaan (concurrent) tidak menyebabkan downtime.
3. [ ] UI Dashboard memuat data dalam waktu kurang dari 2 detik.

## 📦 Kriteria Deployment

1. [ ] Seluruh migrasi database berhasil dijalankan tanpa error.
2. [ ] Mekanisme rollback telah diuji dan berfungsi.
3. [ ] Semua variabel lingkungan (ENV) telah terkonfigurasi dengan benar.

---

**Persetujuan Stakeholder:**

- Product Owner: _________________
- Legal Lead: _________________
- Tech Lead: _________________

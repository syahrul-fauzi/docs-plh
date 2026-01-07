# Panduan Verifikasi Pengguna - Lawyers Hub

Dokumen ini memberikan panduan langkah demi langkah untuk memverifikasi fitur
baru: Document Automation, Multi-Template Merge, dan Audit Trail.

## 1. Document Automation & Version History

Fitur ini memungkinkan pengelolaan template dengan pelacakan versi otomatis.

### Verifikasi Document Automation

1. **Akses Template Gallery**:
   - Buka menu **Templates** di dashboard.
   - Klik tombol **Seed Standard Templates** jika galeri kosong.
2. **Edit Template**:
   - Pilih salah satu template dan klik ikon **Edit**.
   - Lakukan perubahan pada isi template dan simpan.
3. **Cek Riwayat Versi**:
   - Klik ikon **History** pada template yang baru saja diubah.
   - Verifikasi versi baru tercatat dengan timestamp yang benar.
4. **Restorasi Versi**:
   - Di dalam modal History, klik tombol **Restore** versi sebelumnya.
   - Verifikasi konten template kembali ke versi tersebut.
5. **Perbandingan Versi (Diff)**:
   - Pilih dua versi dan klik **Compare Selected Versions**.
   - Verifikasi perbedaan konten ditampilkan secara visual.

## 2. Multi-Template Merge

Fitur ini menggabungkan beberapa template menjadi satu dokumen draft.

### Verifikasi Multi-Merge

1. **Buka Detail Kasus**:
   - Pilih salah satu kasus dari menu **Cases**.
2. **Mulai Multi-Merge**:
   - Klik tombol **Multi-Merge** di bagian atas halaman detail kasus.
3. **Pilih Template**:
   - Pilih minimal 2 template (misal: NDA dan Service Agreement).
   - Klik **Combine Documents**.
4. **Verifikasi Hasil**:
   - Buka draft dokumen yang baru saja dibuat.
   - Pastikan konten dari kedua template ada di sana.
   - Pastikan placeholder telah terisi secara otomatis.

## 3. Audit Logs & Keamanan

Sistem sekarang mencatat aktivitas sensitif untuk kepatuhan hukum.

### Verifikasi Audit Logs

1. **Akses Audit Logs**:
   - Buka menu **Audit Logs** (atau melalui link di sidebar).
2. **Cek Aktivitas Terbaru**:
   - Pastikan aktivitas `TEMPLATE_RESTORE` tercatat di sana.
3. **Filter & Pencarian**:
   - Gunakan filter **Action** untuk mencari jenis aktivitas.
   - Gunakan kolom pencarian berdasarkan nama pengguna.
4. **Keamanan Data**:
   - Metadata log audit disimpan dalam bentuk terenkripsi (AES-256-CBC).

## 4. Deployment ke Staging

Prosedur deployment untuk memastikan transisi yang lancar ke staging.

### Verifikasi Teknis Deployment

1. Pastikan file `.env.staging` telah dikonfigurasi dengan benar.
2. Jalankan `npx prisma migrate deploy` untuk memperbarui skema.
3. Jalankan `npm run build` untuk memastikan semua paket siap.

---

**Catatan**: Jika Anda menemukan kendala, silakan hubungi tim pengembang.

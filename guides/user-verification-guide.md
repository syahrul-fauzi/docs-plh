# Panduan Verifikasi Pengguna - Lawyers Hub

Dokumen ini memberikan panduan langkah demi langkah untuk memverifikasi fitur-fitur baru yang telah diimplementasikan dalam Lawyers Hub, khususnya terkait Document Automation, Multi-Template Merge, dan Audit Trail.

## 1. Document Automation & Version History
Fitur ini memungkinkan Anda untuk mengelola template dokumen dengan pelacakan versi otomatis.

### Langkah Verifikasi:
1.  **Akses Template Gallery**:
    *   Buka menu **Templates** di dashboard.
    *   Klik tombol **Seed Standard Templates** jika galeri masih kosong.
2.  **Edit Template**:
    *   Pilih salah satu template dan klik ikon **Edit**.
    *   Lakukan perubahan pada isi template dan simpan.
3.  **Cek Riwayat Versi**:
    *   Klik ikon **History** (ikon jam) pada template yang baru saja diubah.
    *   Verifikasi bahwa versi baru telah tercatat dengan timestamp yang benar.
4.  **Restorasi Versi**:
    *   Di dalam modal History, klik tombol **Restore** pada versi sebelumnya.
    *   Verifikasi bahwa konten template kembali ke versi tersebut.
5.  **Perbandingan Versi (Diff)**:
    *   Pilih dua versi dalam riwayat dan klik **Compare Selected Versions**.
    *   Verifikasi bahwa perbedaan konten ditampilkan secara visual.

## 2. Multi-Template Merge
Fitur ini memungkinkan penggabungan beberapa template menjadi satu dokumen draft untuk sebuah kasus.

### Langkah Verifikasi:
1.  **Buka Detail Kasus**:
    *   Pilih salah satu kasus dari menu **Cases**.
2.  **Mulai Multi-Merge**:
    *   Klik tombol **Multi-Merge** di bagian atas halaman detail kasus.
3.  **Pilih Template**:
    *   Pilih minimal 2 template yang ingin digabungkan (misal: NDA dan Service Agreement).
    *   Klik **Combine Documents**.
4.  **Verifikasi Hasil**:
    *   Buka draft dokumen yang baru saja dibuat.
    *   Pastikan konten dari kedua template ada di sana dan dipisahkan dengan penanda halaman yang jelas.
    *   Pastikan placeholder (seperti nama firma hukum dan judul kasus) telah terisi secara otomatis.

## 3. Audit Logs & Keamanan
Sistem sekarang mencatat aktivitas sensitif untuk kepatuhan hukum.

### Langkah Verifikasi:
1.  **Akses Audit Logs**:
    *   Buka menu **Audit Logs** (atau melalui link di sidebar).
2.  **Cek Aktivitas Terbaru**:
    *   Pastikan aktivitas seperti `TEMPLATE_RESTORE` dan `TEMPLATE_MERGE_MULTIPLE` tercatat di sana.
3.  **Filter & Pencarian**:
    *   Gunakan filter **Action** untuk mencari jenis aktivitas tertentu.
    *   Gunakan kolom pencarian untuk mencari berdasarkan nama pengguna.
4.  **Keamanan Data**:
    *   Metadata log audit disimpan dalam bentuk terenkripsi di database (AES-256-CBC) untuk menjamin integritas dan privasi.

## 4. Deployment ke Staging
Prosedur deployment telah didokumentasikan untuk memastikan transisi yang lancar ke lingkungan staging.

### Verifikasi Teknis:
1.  Pastikan file `.env.staging` telah dikonfigurasi dengan `DATABASE_URL` dan `CLERK_KEYS` yang benar.
2.  Jalankan `npx prisma migrate deploy` untuk memperbarui skema database di staging.
3.  Jalankan `npm run build` di root folder untuk memastikan semua paket monorepo siap.

---
**Catatan**: Jika Anda menemukan kendala atau perilaku yang tidak sesuai, silakan hubungi tim pengembang atau buat issue di repositori proyek.

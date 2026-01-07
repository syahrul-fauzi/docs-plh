# Archive Management Guide (Panduan Manajemen Arsip)

Dokumen ini menjelaskan kebijakan dan prosedur untuk mengelola folder
`08_archives` di Lawyers Hub.

## 1. Tujuan

Folder arsip digunakan untuk menyimpan dokumen yang sudah tidak berlaku lagi
(deprecated), laporan fase yang sudah selesai, dan catatan historis lainnya yang
tidak lagi menjadi referensi aktif namun penting untuk audit atau pemahaman
sejarah pengembangan.

## 2. Struktur Folder

- `audit_reports/`: Menyimpan laporan audit keamanan, kepatuhan, dan kualitas
  kode yang sudah lewat.
- `deprecated_specs/`: Spesifikasi teknis atau fungsional yang telah digantikan
  oleh versi baru.
- `phase_reports/`: Laporan akhir untuk fase pengembangan atau proyek tertentu.
- `CHANGELOG_INFRA.md`: Catatan perubahan infrastruktur historis.

## 3. Prosedur Pengarsipan

1. **Identifikasi**: Dokumen diidentifikasi sebagai "Arsip" jika sudah ada versi
   pengganti yang lebih baru di folder kategori utama (00-07) atau jika
   fitur/proses yang dijelaskan sudah dihapus.
2. **Pemindahan**: Gunakan `git mv` untuk memindahkan file ke subfolder yang
   sesuai di `08_archives`.
3. **Pencatatan**: Perbarui `CHANGELOG.md` di root proyek jika pemindahan
   tersebut signifikan.
4. **Metadata**: Pastikan dokumen yang diarsip memiliki header yang jelas
   menyatakan statusnya sebagai "ARCHIVED" atau "DEPRECATED".

## 4. Retensi

Dokumen di folder arsip akan dipertahankan selama minimal 2 tahun atau sesuai
dengan kebijakan retensi data perusahaan untuk tujuan audit dan kepatuhan hukum
(UU PDP).

---

### Update Info

Terakhir diperbarui: 2026-01-06 oleh Super Agent

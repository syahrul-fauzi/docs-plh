# UAT Scenarios - Lawyers Hub

Dokumen ini berisi skenario pengujian untuk User Acceptance Testing (UAT) guna memastikan aplikasi memenuhi kebutuhan bisnis sebelum Go-Live.

## Skenario 1: Onboarding & Autentikasi
- **ID**: UAT-001
- **Deskripsi**: Verifikasi pengguna baru dapat mendaftar, login, dan melihat dashboard.
- **Langkah**:
  1. Buka halaman login.
  2. Masuk dengan kredensial yang valid.
  3. Verifikasi dialihkan ke dashboard.
- **Hasil yang Diharapkan**: Pengguna berhasil masuk dan statistik dashboard muncul dengan benar.

## Skenario 2: Siklus Hidup Kasus (Case Lifecycle)
- **ID**: UAT-002
- **Deskripsi**: Verifikasi pembuatan kasus hingga penutupan kasus.
- **Langkah**:
  1. Buat kasus baru dengan data lengkap.
  2. Tambahkan dokumen ke dalam kasus.
  3. Ubah status kasus menjadi "Closed".
- **Hasil yang Diharapkan**: Kasus tersimpan di database dan status diperbarui secara real-time.

## Skenario 3: Kolaborasi Real-time Dokumen
- **ID**: UAT-003
- **Deskripsi**: Verifikasi dua pengguna dapat mengedit dokumen yang sama secara bersamaan.
- **Langkah**:
  1. Pengguna A membuka dokumen hukum.
  2. Pengguna B membuka dokumen yang sama.
  3. Pengguna A mengetik, Pengguna B melihat perubahan secara instan.
- **Hasil yang Diharapkan**: Tidak ada konflik pengeditan dan perubahan muncul real-time via Socket.io.

## Skenario 4: Deteksi PII & Compliance
- **ID**: UAT-004
- **Deskripsi**: Verifikasi sistem mendeteksi dan menyamarkan data sensitif (UU PDP).
- **Langkah**:
  1. Unggah dokumen yang mengandung NIK dan alamat.
  2. Jalankan "Audit PII".
  3. Periksa apakah data sensitif ditandai atau disamarkan sesuai kebijakan.
- **Hasil yang Diharapkan**: Data PII terdeteksi dengan akurasi tinggi (>95%).

## Skenario 5: Integrasi AI Assistant
- **ID**: UAT-005
- **Deskripsi**: Verifikasi AI dapat memberikan ringkasan dokumen hukum.
- **Langkah**:
  1. Buka dokumen kontrak panjang.
  2. Klik "Ask AI to Summarize".
  3. Tinjau hasil ringkasan.
- **Hasil yang Diharapkan**: Ringkasan akurat dan mencakup poin-poin hukum utama.

## Skenario 6: Billing & Subscription
- **ID**: UAT-006
- **Deskripsi**: Verifikasi transisi paket langganan.
- **Langkah**:
  1. Buka menu Billing.
  2. Upgrade dari paket Basic ke Pro.
  3. Verifikasi fitur Pro (misal: unlimited documents) aktif.
- **Hasil yang Diharapkan**: Transaksi berhasil dan limitasi akun diperbarui.

## Skenario 7: Manajemen Anggota Tim
- **ID**: UAT-007
- **Deskripsi**: Admin mengundang anggota baru ke firma.
- **Hasil yang Diharapkan**: Undangan terkirim via email dan anggota dapat bergabung.

## Skenario 8: Pencarian Dokumen Global
- **ID**: UAT-008
- **Deskripsi**: Mencari dokumen berdasarkan kata kunci dalam isi file.
- **Hasil yang Diharapkan**: Dokumen relevan muncul di hasil pencarian.

## Skenario 9: Export Laporan Kasus
- **ID**: UAT-009
- **Deskripsi**: Export data kasus ke format PDF/Excel.
- **Hasil yang Diharapkan**: File terunduh dengan data yang akurat.

## Skenario 10: Notifikasi Real-time
- **ID**: UAT-010
- **Deskripsi**: Pengguna menerima notifikasi saat ada perubahan pada kasus.
- **Hasil yang Diharapkan**: Pop-up notifikasi muncul secara instan.

## Skenario 11-20: Skenario Bisnis Lanjutan
- **UAT-011**: Pemulihan dokumen dari Version History.
- **UAT-012**: Pengaturan Role & Permission (RBAC).
- **UAT-013**: Integrasi Kalender dengan Google/Outlook.
- **UAT-014**: Pengarsipan kasus lama (Archive).
- **UAT-015**: Audit Log viewer untuk Admin.
- **UAT-016**: Bulk upload dokumen hukum.
- **UAT-017**: Pengaturan Branding Firma (Logo, Warna).
- **UAT-018**: Chat Internal antar anggota tim.
- **UAT-019**: Verifikasi Two-Factor Authentication (2FA).
- **UAT-020**: Penanganan error saat koneksi terputus (Offline mode).

---
**Total Skenario: 20 Skenario Bisnis Kritis**
*Sign-off QA: [..........]*
*Sign-off Business: [..........]*

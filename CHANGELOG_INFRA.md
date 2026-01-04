# Changelog Infrastruktur Dokumentasi 📝

Semua perubahan besar pada infrastruktur dokumentasi Lawyers Hub dicatat di sini.

## [1.0.0] - 2026-01-04

### Added
- **Inisialisasi Git**: Menambahkan file `.gitignore` komprehensif untuk project dokumentasi.
- **Standar Kualitas**: Implementasi `.prettierrc` dan `.markdownlint.json`.
- **Otomatisasi**: Menambahkan GitHub Actions workflow `.github/workflows/docs-validation.yml` untuk linting dan validasi link otomatis.
- **Panduan**: Membuat `ROOT_UPDATE_GUIDE.md` untuk sinkronisasi konfigurasi root.
- **Sistem Cadangan**: Folder `backups/` untuk redundansi konfigurasi kritis.
- **Audit**: Laporan audit link internal `audit-report-links.md`.

### Changed
- **Reorganisasi Folder**: Memindahkan dokumen dari root `docs/` ke sub-folder kategori:
  - `api/`: Dokumen teknis & API.
  - `deployment/`: Panduan infrastruktur.
  - `guides/`: Tutorial & panduan pengguna.
  - `rules/`: Framework aturan AI.
- **Pembaruan Link**: Memperbaiki link relatif yang rusak akibat perubahan struktur folder.
- **Dokumentasi Utama**: Memperbarui `README.md` dan `CONTRIBUTING.md` dengan instruksi Git Hooks dan formatting.

### Security
- Konfigurasi `.gitignore` diperketat untuk mencegah kebocoran file `.env` dan data sensitif lainnya.

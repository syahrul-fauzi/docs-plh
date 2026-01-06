# Panduan Kontribusi 🤝

Terima kasih telah tertarik untuk berkontribusi pada **Lawyers Hub**! Sebagai proyek dokumentasi hukum, akurasi dan kerapian adalah prioritas utama kami.

## 🛠 Cara Berkontribusi

1.  **Fork** repositori ini.
2.  Buat **Branch** baru untuk fitur atau perbaikan Anda:
    ```bash
    git checkout -b fitur/nama-fitur
    ```
3.  Lakukan **Commit** dengan pesan yang jelas:
    ```bash
    git commit -m "Tambah: Dokumentasi kepatuhan privasi data"
    ```
4.  **Push** ke branch Anda:
    ```bash
    git push origin fitur/nama-fitur
    ```
5.  Buat **Pull Request**.

## 📝 Aturan Penulisan

- Gunakan format **Markdown** standar.
- Pastikan terminologi hukum yang digunakan akurat.
- Gunakan bahasa yang profesional dan mudah dipahami.
- Pastikan semua file `.md` telah diformat menggunakan **Prettier**.

## 🏗 Struktur Dokumentasi

Tambahkan dokumen baru ke subfolder yang sesuai di dalam `docs/`:
- `docs/api/`: Dokumentasi teknis integrasi API.
- `docs/legal/`: Dokumen terkait peraturan dan hukum (GDPR, Privacy).
- `docs/guides/`: Panduan operasional dan tutorial langkah-demi-langkah.
- `docs/deployment/`: Panduan infrastruktur dan deployment.
- `docs/qa/`: Laporan kualitas dan pengujian.
- `docs/rules/`: Aturan dan etika AI Agents.

## ✅ Validasi Otomatis (CI/CD)

Setiap Pull Request (PR) akan melalui proses validasi otomatis menggunakan **GitHub Actions**:
1. **Markdown Lint**: Memastikan format dokumen sesuai dengan standar `markdownlint`.
2. **Link Check**: Memverifikasi bahwa tidak ada link internal atau eksternal yang rusak (*broken links*).
3. **Prettier**: Memastikan kode/dokumen telah diformat dengan rapi.

### Menjalankan Format Secara Lokal

Sebelum melakukan commit, Anda disarankan untuk menjalankan formatting secara otomatis:

```bash
# Jika Anda berada di root proyek
npm run format

# Jika Anda ingin menjalankan Prettier secara manual di folder docs
npx prettier --write "docs/**/*.md"
```

### Git Hooks (Husky & lint-staged)

Untuk memastikan konsistensi format sebelum kode masuk ke repositori, kami menggunakan **Husky** dan **lint-staged**. Jika Anda belum mengaturnya, ikuti langkah berikut:

1.  **Instalasi**:
    ```bash
    npm install --save-dev husky lint-staged
    npx husky install
    ```
2.  **Konfigurasi lint-staged**: Pastikan ada bagian berikut di `package.json` Anda:
    ```json
    "lint-staged": {
      "**/*.{js,ts,tsx,md,json}": [
        "prettier --write"
      ]
    }
    ```
3.  **Tambah Hook**:
    ```bash
    npx husky add .husky/pre-commit "npx lint-staged"
    ```

Harap pastikan semua cek validasi ini lulus sebelum meminta review dari tim.

## 🚨 Pelaporan Masalah

Jika Anda menemukan kesalahan atau memiliki saran, silakan buka **Issue** baru di GitHub.

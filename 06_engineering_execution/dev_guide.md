# Panduan Pembaruan Root Project 🚀

Dokumen ini berisi instruksi spesifik untuk memperbarui konfigurasi di tingkat
root proyek `lawyers-hub`. Karena batasan akses keamanan, perubahan ini harus
dilakukan secara manual oleh administrator proyek.

## 1. Pembaruan `package.json`

Mohon perbarui file `package.json` di root proyek dengan konfigurasi berikut:

### Script Format

Ganti bagian `"scripts"` untuk memperluas cakupan formatting:

```json
"scripts": {
  ...
  "format": "prettier --write \"**/*.{js,ts,tsx,md,json}\"",
  ...
}
```

### Konfigurasi lint-staged

Tambahkan blok `lint-staged` sebelum penutup kurung kurawal terakhir:

```json
"lint-staged": {
  "**/*.{js,ts,tsx,md,json}": [
    "prettier --write"
  ]
}
```

### Verifikasi & Pengujian JSON

Sebelum menyimpan perubahan pada `package.json`, sangat disarankan untuk:

1. **Validasi Sintaks**: Gunakan tool seperti [JSONLint](https://jsonlint.com/)
    atau extension VS Code untuk memastikan tidak ada koma yang hilang atau
    kurung yang tidak tertutup.
2. **Dry Run**: Jalankan perintah berikut untuk memastikan dependensi masih
    valid:

    ```bash
    npm install --package-lock-only
    ```

## 2. Implementasi Pre-commit Hooks (Husky)

Jalankan perintah berikut di terminal root proyek untuk mengaktifkan validasi
otomatis sebelum commit:

```bash
# Instalasi dependencies
npm install --save-dev husky lint-staged

# Inisialisasi Husky
npx husky install

# Tambahkan hook pre-commit
npx husky add .husky/pre-commit "npx lint-staged"
```

## 3. Verifikasi & Pengujian Regresi

Setelah melakukan perubahan, lakukan pengujian berikut untuk memastikan tidak
ada dampak negatif:

1. **Format Check**: Jalankan `npm run format`. Pastikan semua file `.md` dan
    `.json` terformat tanpa error.
2. **Build Check**: Jika project ini memiliki proses build (seperti Turbo),
    jalankan `npm run build`.
3. **Hook Test**: Coba lakukan commit pada file dummy. Husky harus menjalankan
    `lint-staged` dan memformat file tersebut secara otomatis.

    ```bash
    echo "# Test" > test.md
    git add test.md
    git commit -m "test: verify husky and lint-staged"
    ```

4. **Rollback Plan**: Jika terjadi kesalahan, Anda dapat mengembalikan
    perubahan dengan `git checkout package.json`.

---

_Dokumen ini dibuat sebagai bagian dari inisialisasi infrastruktur dokumentasi
Lawyers Hub - 2026-01-04_

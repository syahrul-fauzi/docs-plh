# Panduan Pengujian dan Troubleshooting Memory Leak

Dokumen ini menjelaskan prosedur pengujian optimal untuk Lawyers Hub Core API,
mencakup validasi file dan pemantauan kebocoran memori.

## 1. Validasi Konten File (PDF/ZIP)

Kami menggunakan pengujian unit khusus untuk memastikan integritas konten yang
dihasilkan oleh sistem.

### Prosedur Pengujian

- **File Test**: `apps/api/src/file-validation.spec.ts`
- **Library**: `pdf-lib` (untuk PDF), `adm-zip` (untuk ZIP)
- **Cakupan**: Struktur file, metadata, dan integritas teks/data.

### Cara Menjalankan

```bash
cd apps/api
npx jest src/file-validation.spec.ts
```

---

## 2. Pemantauan Memory Leak

Pemantauan kebocoran memori dilakukan dengan melakukan stress test pada operasi
database (Prisma) dan CPU-intensive tasks.

### Flag dan Parameter Penting

- `--expose-gc`: Mengaktifkan akses ke fungsi `global.gc()` untuk pembersihan
  manual selama test.
- `--logHeapUsage`: Menampilkan penggunaan memori heap setelah setiap test
  suite.
- `--forceExit`: Memastikan proses berhenti jika ada handle yang menggantung.

### Cara Menjalankan

```bash
cd apps/api
export NODE_OPTIONS="--expose-gc"
npx jest src/memory-leak.spec.ts --logHeapUsage --forceExit
```

### Interpretasi Hasil

- **Initial Memory**: Penggunaan memori dasar setelah aplikasi diinisialisasi.
- **Final Memory**: Penggunaan memori setelah operasi berulang (looping).
- **Memory Diff**: Selisih antara Final dan Initial. Jika > 50MB secara
  konsisten, indikasi kebocoran memori.

### Laporan Trend (New)

Setiap kali pengujian memori dijalankan, laporan otomatis akan dibuat di:

- `apps/api/reports/memory-trend-report.json`: Data mentah untuk analisis
  historis.
- `apps/api/reports/memory-report.md`: Ringkasan format tabel untuk dibaca cepat
  di CI/CD Artifacts.

---

## 3. Panduan Troubleshooting Memory Leak

Jika ditemukan kebocoran memori (Memory Diff melebihi ambang batas):

### Langkah Identifikasi

1. **Analisis Laporan**: Cek scenario mana di `memory-report.md` yang statusnya
   `FAIL`.
2. **Identifikasi Operasi**: Lihat test case tersebut di `memory-leak.spec.ts`.
3. **Periksa Mocking**: Pastikan instance mock (seperti `PrismaService`)
   dibersihkan atau tidak menyimpan referensi objek besar secara global.
4. **Cek Event Listeners**: Pastikan tidak ada event emitter yang ditambahkan
   terus-menerus tanpa `removeListener`.
5. **Analisis Heap Dump**: Jika kebocoran parah, buat heap dump untuk dianalisis
   di Chrome DevTools:

   ```bash
   node --inspect src/main.js
   ```

### Solusi Umum

- Gunakan `weak-napi` untuk referensi yang tidak menghalangi GC.
- Pastikan koneksi database ditutup di `afterAll`.
- Hindari penggunaan variabel global untuk menyimpan data hasil query besar.

---

## 4. Integrasi CI/CD

Pengujian ini otomatis dijalankan di setiap Pull Request melalui GitHub Actions
(file `.github/workflows/ci.yml`).

| Stage           | Deskripsi                | Timeout | Threshold       |
| --------------- | ------------------------ | ------- | --------------- |
| File Validation | Memastikan PDF/ZIP valid | 5 min   | 100% Pass       |
| Memory Leak     | Memantau lonjakan memori | 10 min  | < 50MB Increase |

**Note**: Hasil laporan memori dapat diunduh dari tab **Artifacts** di GitHub
Actions run dengan nama `memory-leak-report`.

# Laporan Penelitian Mendalam: Lawyers Hub

Dokumen ini merangkum temuan penelitian sistematis untuk mendukung implementasi
Lawyers Hub yang aman dan efisien.

## 1. Arsitektur RAG Hukum (Best Practices)

- **Hierarchical Chunking**: Berbeda dengan dokumen umum, dokumen hukum
  (Undang-Undang, Kontrak) memiliki struktur hierarki (Bab, Pasal, Ayat). RAG
  harus mempertahankan konteks ini agar jawaban AI akurat secara hukum.
- **Hybrid Search**: Menggabungkan pencarian vektor (semantik) dengan pencarian
  kata kunci (BM25) sangat penting untuk istilah hukum yang spesifik.
- **PII Masking**: Masking harus dilakukan _sebelum_ data masuk ke Vector DB
  atau LLM eksternal untuk mematuhi UU PDP.

## 2. Kepatuhan UU PDP No. 27/2022 (Indonesia)

- **Definisi Data Pribadi**: Meliputi data identitas (NIK), kesehatan,
  biometrik, data keuangan, dan data anak.
- **Kewajiban Pengendali Data**:
  - Menjaga kerahasiaan data.
  - Melakukan penilaian dampak perlindungan data (DPIA).
  - Melaporkan kegagalan perlindungan data dalam 72 jam.
- **Implementasi**: Penggunaan Row Level Security (RLS) di PostgreSQL dan audit
  log akses adalah standar minimum yang direkomendasikan.

## 3. Solusi Masking PII

- **Microsoft Presidio**: Menawarkan mesin deteksi berbasis aturan dan model ML
  (SpaCy/Transformers). Sangat efektif untuk deteksi entitas global.
- **Custom Regex**: Diperlukan untuk pola spesifik Indonesia seperti NIK (16
  digit), NPWP (format lama & baru), dan pelat nomor kendaraan.
- **Contextual Clues**: Nama seringkali muncul setelah gelar seperti "Advokat",
  "Hakim", atau "Bapak/Ibu".

## 4. Studi Kasus Serupa

- **Harvey AI**: Menggunakan RAG dengan fokus tinggi pada sitasi dokumen asli
  untuk meminimalisir halusinasi.
- **Luminance**: Menggunakan AI untuk review kontrak dengan _deterministic
  rules_ untuk memastikan klausa wajib tidak terlewatkan.

## 5. Referensi Teknis

- [UU PDP No. 27 Tahun 2022](https://peraturan.go.id/id/uu-no-27-tahun-2022)
- [Prisma Row Level Security Guide](https://www.prisma.io/docs/guides/database/postgresql/row-level-security)
- [Turborepo Monorepo Management](https://turbo.build/repo/docs)

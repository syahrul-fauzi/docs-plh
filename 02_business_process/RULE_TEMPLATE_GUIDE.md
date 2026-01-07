# Panduan Penggunaan Template Aturan Hukum (Rule PRD Template)

Dokumen ini menjelaskan cara menggunakan
[rule_prd_template.md](file:///home/inbox/smart-ai/lawyers-hub/rule_prd_template.md)
untuk mendokumentasikan aturan hukum baru sebelum diimplementasikan ke dalam
sistem.

## 1. Mengapa Menggunakan Template Ini?

- **Standarisasi**: Memastikan setiap aturan memiliki informasi yang lengkap
  (konteks hukum, logika, dan kepatuhan data).
- **Kolaborasi**: Memudahkan tim Legal memberikan spesifikasi kepada tim
  Engineering.
- **Audit**: Menjadi bukti dokumentasi saat audit kepatuhan (UU PDP/GDPR).

## 2. Langkah-langkah Penggunaan

### Langkah 1: Persiapan

- Salin file `rule_prd_template.md` ke folder tujuan (misalnya di
  `docs/02_business_process/new_rules/`).
- Beri nama file yang deskriptif, contoh: `RULE-CORP-001-Quorum-RUPS.md`.

### Langkah 2: Mengisi Metadata

- **Rule ID**: Ikuti format `CORP-[CATEGORY]-[NUMBER]`.
- **Domain**: Bidang hukum terkait (Corporate, Labor, Privacy, dll).
- **Data Sensitivity**: Tentukan tingkat sensitivitas data yang akan diproses
  oleh aturan ini.

### Langkah 3: Menentukan Konteks Regulasi

- Sebutkan pasal dan undang-undang yang mendasari aturan ini. Ini sangat penting
  untuk keperluan audit di masa depan.

### Langkah 4: Merancang Logika (YAML)

- Bagian ini adalah jembatan ke tim Engineering.
- Gunakan blok YAML untuk mendefinisikan kondisi teknis. Contoh:

  ```yaml
  condition:
    field_name: 'value'
    operator: '>='
  ```

### Langkah 5: Skenario Pengujian

- Tuliskan minimal 2 skenario (Skenario Sukses dan Skenario Gagal/Warning) untuk
  membantu tim QA melakukan verifikasi.

## 3. Proses Review dan Persetujuan

1. **Drafting**: Tim Legal menyusun draft menggunakan template.
2. **Technical Review**: Tim Engineering meninjau kelayakan teknis dari logika
   YAML yang diusulkan.
3. **Approval**: Aturan disetujui untuk diimplementasikan ke dalam file
   konfigurasi sistem (misal: `rules.yaml`).

## 4. Tips Efektif

- **Gunakan Bahasa yang Jelas**: Hindari jargon hukum yang terlalu rumit tanpa
  penjelasan bagi non-legal.
- **Referensikan Dokumen Lain**: Gunakan tautan Markdown untuk menghubungkan
  aturan dengan spesifikasi teknis terkait.
- **Update Berkala**: Jika undang-undang berubah, segera perbarui dokumen PRD
  ini dan buat versi baru.

---

Terakhir diperbarui: 2026-01-06 oleh Super Agent

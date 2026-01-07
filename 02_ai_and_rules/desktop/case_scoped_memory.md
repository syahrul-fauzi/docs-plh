# AI Case-Scoped Memory — Desktop Implementation

**Status:** DRAFT **Versi:** 1.0.0 **Tanggal:** 2026-01-07

## 1. Konsep Dasar
*Case-Scoped Memory* adalah mekanisme di mana AI hanya memiliki akses ke konteks memori yang relevan dengan perkara (case) yang sedang dibuka oleh pengguna di aplikasi desktop. Hal ini mencegah kebocoran informasi antar perkara dan meningkatkan akurasi AI dalam memberikan bantuan hukum.

## 2. Arsitektur Memori
Dalam aplikasi desktop, memori ini dikelola secara hybrid antara penyimpanan lokal dan cloud.

### 2.1 Alur Data Memori
1. **Case Activation**: Saat pengguna memilih perkara, aplikasi desktop memuat indeks konteks lokal.
2. **Memory Isolation**: Tauri memastikan bahwa buffer memori untuk satu perkara dibersihkan sebelum memuat perkara lain.
3. **Context Injection**: Saat melakukan prompt, sistem secara otomatis menyuntikkan (inject) memori jangka pendek yang relevan dengan perkara tersebut.

## 3. Implementasi Teknis
### 3.1 Local Vector Cache (Desktop Only)
Aplikasi desktop menggunakan penyimpanan vektor lokal (seperti SQLite dengan ekstensi vss atau library serupa) untuk menyimpan embedding dari dokumen perkara yang sedang dikerjakan.

- **Kelebihan**: Pencarian konteks sangat cepat dan tidak memerlukan upload seluruh dokumen ke cloud untuk setiap pertanyaan.
- **Privasi**: Data sensitif tetap berada di mesin pengguna sampai benar-benar diperlukan oleh LLM.

### 3.2 Sinkronisasi & State
- Memori perkara disinkronkan ke server pusat hanya jika pengguna memberikan izin eksplisit.
- Sinkronisasi menggunakan protokol terenkripsi end-to-end.

## 4. Aturan Tata Kelola (Governance)
- **Automatic Expiry**: Memori jangka pendek akan dihapus setelah sesi perkara ditutup.
- **Manual Flush**: Pengguna dapat menghapus memori konteks perkara kapan saja.
- **PII Masking**: Sebelum dikirim ke LLM, data dalam memori perkara akan melewati filter PII (Personally Identifiable Information) di sisi desktop.

---
*Dokumen ini melengkapi panduan tata kelola AI di Lawyers Hub.*

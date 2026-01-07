# Standar Penjaminan Kualitas (QA Standards) - Lawyers Hub

Dokumen ini mendefinisikan standar kualitas kelas dunia untuk implementasi
proyek Lawyers Hub.

## 1. Kualitas Kode (@SOLOCoder)

- **Linting**: Semua kode harus lulus pemeriksaan ESLint dan format Prettier.
- **Tipe Data**: Penggunaan `any` dilarang. Semua interface dan tipe data harus
  didefinisikan secara eksplisit.
- **Validasi**: Semua input eksternal harus divalidasi menggunakan Zod schemas
  di layer `packages/core`.
- **Error Handling**: Gunakan kelas error kustom dari `packages/core`.

## 2. Cakupan Pengujian (Testing Coverage)

- **Unit Testing**: Minimal 80% coverage untuk `packages/domain` dan rules.
- **Integration Testing**: Semua endpoint API kritis memiliki tests.
- **AI Evaluation**: Menggunakan framework RAGAS untuk akurasi RAG.

## 3. Dokumentasi

- Setiap modul baru harus menyertakan README.md teknis.
- Perubahan arsitektur harus didokumentasikan dengan diagram Mermaid.
- Catatan perubahan (Changelog) diperbarui setiap minggu.

## 4. Keamanan & Kepatuhan

- **Isolasi Data**: Wajib menggunakan RLS (Row Level Security) untuk semua tabel
  tenant-aware.
- **PII Masking**: Data sensitif harus disamarkan sebelum dikirim ke LLM.
- **Audit Log**: Setiap akses data sensitif dicatat dalam audit trail.

---

**Dibuat oleh**: @WorldClassAgent

# Toolchain & Automation Configuration

## 1. Tujuan

Menstandarisasi alat bantu dan alur kerja otomatisasi untuk pengembangan,
dokumentasi, dan validasi di Lawyers Hub.

## 2. Version Control (Git)

- **Platform**: GitHub / GitLab (Enterprise).
- **Branching Strategy**: Trunk-Based Development dengan Short-Lived Feature
  Branches.
- **Commit Message**: Ikuti standar
  [Conventional Commits](https://www.conventionalcommits.org/).

## 3. CI/CD Pipeline

Pipeline otomatis menggunakan GitHub Actions untuk:

- **Linting**:
  - Kode: `eslint`, `prettier`.
  - Dokumentasi: `markdownlint`.
- **Testing**:
  - Unit Test: `jest` (packages).
  - Integration Test: `playwright` (apps/web).
- **Validation**:
  - Validasi schema YAML Rule menggunakan `RuleValidator` (custom script).
  - Validasi link markdown yang rusak.

## 4. Automated Documentation Generator

- **Technical API**: Menggunakan `TypeDoc` untuk menghasilkan dokumentasi API
  dari komentar JSDoc/TSDoc di `packages/`.
- **Database**: `prisma-docs-generator` untuk visualisasi schema database.
- **Deployment**: Dokumentasi dipublish ke GitHub Pages atau Vercel Preview
  untuk kolaborasi internal.

## 5. Notification System

- **Integrasi Slack/Discord**: Notifikasi otomatis jika:
  - PR baru dibuka (tag reviewer).
  - Pipeline CI/CD gagal.
  - Dokumentasi critical (misal: Compliance) diperbarui.

## 6. Diagramming Tool

- **Mermaid.js**: Standard utama untuk diagram di dalam Markdown.
- **Excalidraw**: Untuk brainstorming awal (disimpan sebagai `.excalidraw` file
  di `docs/assets/`).

## 7. Versi & Riwayat

| Versi | Tanggal    | Penulis  | Deskripsi Perubahan                 |
| :---- | :--------- | :------- | :---------------------------------- |
| v1.0  | 2026-01-05 | AI Agent | Inisialisasi konfigurasi toolchain. |

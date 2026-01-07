# Migration Plan — Lawyers Hub Documentation

## 1. Overview

Rencana ini merinci langkah-langkah untuk merestrukturisasi dokumentasi Lawyers
Hub dari sistem berbasis fase pengembangan ke Arsitektur Enterprise
Documentation v1.0.

## 2. Timeline & Milestones

### Milestone 1: Structural Migration (COMPLETED)

- [x] Create 9-pillar directory structure.
- [x] Migrate root files to category folders.
- [x] Standardize filenames (lowercase_with_underscores).
- [x] Initial commit of new structure.

### Milestone 2: Re-categorization (IN PROGRESS)

- [ ] Move legacy documents to 08_archives.
- [ ] Update internal document links.

### Milestone 3: Standardization

- [ ] Apply new templates to critical documents (Arch, Security, AI).
- [ ] Validate YAML frontmatter.

### Milestone 4: Integration (COMPLETED)

- [x] Setup validation pipeline (Linter, Link Checker).
- [x] Integrate TypeDoc for automated API documentation.
- [x] Activate CI/CD pipeline on push/PR.

## 3. Mapping Strategy (Lama ke Baru)

| Sumber (Lama)               | Target (Baru)                            | Catatan                         |
| :-------------------------- | :--------------------------------------- | :------------------------------ |
| `ARCHITECTURE.md`           | `01_architecture/system_overview.md`     | Tambahkan diagram Mermaid       |
| `TECHNICAL_SPEC.md`         | `01_architecture/api_and_service_map.md` | Gabungkan semua spesifikasi API |
| `PROJECT_PLAN.md`           | `05_delivery_and_ops/project_plan.md`    | Update status real-time         |
| `QA_REPORTS/`               | `08_archives/qa_reports/`                | Simpan sebagai audit trail      |
| `docs/.trae/Master Plan.md` | `00_foundation/README.md`                | Referensi utama                 |

## 4. Risk Mitigation

- **Risiko**: Kehilangan riwayat perubahan.
- **Mitigasi**: Gunakan `git mv` untuk memindahkan file agar history tetap
  terjaga.
- **Risiko**: Broken links antar dokumen.
- **Mitigasi**: Jalankan automated link checker setelah migrasi setiap fase.

## 5. Definition of Done (DoD)

- [ ] Semua file di root `docs/` telah dipindahkan ke folder kategori.
- [ ] Minimal 80% dokumen inti memiliki YAML frontmatter yang valid.
- [ ] Pipeline CI/CD untuk dokumentasi lulus (0 error).
- [ ] Style guide telah disosialisasikan ke tim.

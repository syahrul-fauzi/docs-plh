# Style Guide & Templates — Lawyers Hub

## 1. Writing Principles
- **Conciseness**: Gunakan kalimat aktif dan singkat.
- **Objectivity**: Fokus pada fakta teknis dan bisnis, hindari jargon yang tidak perlu.
- **Accessibility**: Gunakan bahasa yang dapat dipahami oleh stakeholder lintas fungsi (Engineering, Legal, Product).

## 2. Formatting Standards
- **File Naming**: Gunakan `snake_case` untuk nama file (contoh: `system_overview.md`).
- **Headers**: Gunakan Title Case untuk header level 1 dan 2.
- **Code Blocks**: Selalu sertakan tag bahasa (contoh: ` ```typescript `).
- **Diagrams**: Gunakan Mermaid.js untuk diagram alur dan arsitektur.

## 3. Metadata Standard (Frontmatter)
Setiap dokumen harus dimulai dengan blok YAML:
```yaml
---
id: LH-DOC-001
title: System Overview
status: approved
owner: architecture-team
last_updated: 2026-01-05
---
```

## 4. Documentation Templates

### 4.1 Technical Specification Template
(Lokasi: `docs/templates/tech_spec.md`)
```markdown
# [Feature Name] - Technical Spec

## Abstract
Ringkasan singkat tentang fitur/sistem.

## Architecture
[Mermaid Diagram]

## API Endpoints / Interfaces
Detail input, output, dan error handling.

## Security Considerations
Audit trail, encryption, and access control.
```

### 4.2 Business Process Template
(Lokasi: `docs/templates/business_process.md`)
```markdown
# [Process Name]

## User Persona
Siapa yang terlibat dalam proses ini?

## Process Flow
[Mermaid Sequence/Flowchart]

## Business Rules
Logika AI atau aturan hukum yang berlaku.
```

## 5. Taxonomy & Classification System
Gunakan sistem taksonomi berikut untuk metadata dan pencarian:

### 5.1 Content Classification
- **Jenis**: `Technical`, `Business`, `Regulatory`, `QA`, `Operations`.
- **Tingkat Kepentingan**: `Critical`, `Important`, `Standard`.
- **Status**: `Draft`, `In Review`, `Approved`, `Deprecated`, `Archived`.

### 5.2 Metadata Tags
Gunakan tag berikut untuk mempermudah navigasi:
- `#core`: Komponen sistem utama.
- `#ai`: Logika kecerdasan buatan & RAG.
- `#legal`: Kepatuhan (PDP), audit, dan regulasi.
- `#gtm`: Strategi pasar, pricing, dan launch.
- `#ops`: Deployment, monitoring, dan incident management.

## 6. Version Management & Approval
Untuk memastikan integritas dokumen, ikuti alur berikut:

### 6.1 Version Control
- Semua dokumen dikelola di Git.
- Perubahan mayor harus melalui **Pull Request (PR)**.
- Gunakan **Semantic Versioning** untuk dokumen arsitektur (v1.0.0).

### 6.2 Approval Workflow
| Role | Tanggung Jawab |
| :--- | :--- |
| **Author** | Penulisan draf awal dan riset. |
| **Peer Reviewer** | Memeriksa kelengkapan teknis dan format. |
| **Approver** | Stakeholder (CTO/Legal/Product) yang menyetujui rilis dokumen. |

### 6.3 Change Log
Setiap dokumen harus memiliki tabel riwayat di bagian akhir:
```markdown
## 7. Versi & Riwayat
| Versi | Tanggal | Penulis | Deskripsi Perubahan |
| :--- | :--- | :--- | :--- |
| v1.0 | 2026-01-05 | AI Agent | Inisialisasi dokumen. |
```

# API & Integration Catalog v1.0 — Lawyers Hub

## 1. Core Services

### 1.1 AI RAG Engine (`@lawyers-hub/copilot`)
Layanan utama untuk pemrosesan dokumen hukum dan tanya jawab berbasis AI.

| Endpoint/Method | Input | Output | Deskripsi |
| :--- | :--- | :--- | :--- |
| `indexDocument` | `tenantId, docId, content` | `void` | Melakukan hierarchical chunking dan indexing ke Vector Store. |
| `generateResponse` | `query, tenantId, options` | `answer, citations, warnings` | Menghasilkan jawaban AI dengan validasi rules dan masking PII. |
| `generateDraft` | `templateType, prompt` | `content, warnings, triggeredRule` | Membuat draft dokumen hukum berdasarkan template. |

### 1.2 Rules Engine (`@lawyers-hub/rules-engine`)
Mesin validasi deterministik untuk memastikan output AI sesuai dengan batasan hukum.

| Endpoint/Method | Input | Output | Deskripsi |
| :--- | :--- | :--- | :--- |
| `validate` | `ruleInput (YAML/Obj)` | `valid (bool), errors[]` | Memvalidasi schema aturan hukum. |
| `lintRule` | `rule` | `warnings[]` | Mengecek kompleksitas dan risiko keamanan pada aturan. |

## 2. Integration Points

### 2.1 Security & AI
- **PII Masking**: Semua query AI (`generateResponse`) wajib melewati `maskPII` sebelum dikirim ke LLM.
- **Audit Trail**: Setiap tindakan AI dicatat dalam `AuditLog` dan `PIIAuditLog` (database).

### 2.2 Database & Multitenancy
- **Tenant Isolation**: Semua query database wajib menyertakan `tenantId`.
- **Compliance Sync**: Hasil `ComplianceReview` disinkronkan secara periodik untuk retraining model NER.

## 3. Webhook & Events
(Placeholder untuk integrasi WhatsApp dan eksternal API lainnya).

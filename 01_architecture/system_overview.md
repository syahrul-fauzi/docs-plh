# Lawyers Hub — System Architecture Overview

**Status:** ACTIVE (Aligned with Foundation v1.0)
**Versi:** 1.0.0
**Tanggal:** 2026-01-05
**Pemilik:** Product Owner / System Architect

Dokumen ini mendefinisikan **arsitektur sistem menyeluruh Lawyers Hub**, diturunkan langsung dan **WAJIB konsisten** dengan `00_foundation/README.md`.

---

## 1. Tujuan Dokumen

* Menjelaskan arsitektur teknis Lawyers Hub secara end-to-end
* Menjadi referensi utama untuk seluruh engineer dan AI agent
* Mengunci batasan sistem, integrasi, dan tanggung jawab komponen
* Menjadi dasar desain detail (API, data flow, security, AI governance)

---

## 2. Ruang Lingkup

Dokumen ini mencakup:

* Arsitektur logical & physical
* Interaksi AG-UI, CopilotKit, dan backend
* Boundary data, AI, dan keamanan

Dokumen ini **tidak** mencakup:

* Implementasi kode detail
* Konfigurasi infra spesifik vendor

---

## 3. Prinsip Arsitektur Utama

1. **Assistive AI Architecture**
   AI selalu berada di lapisan bantuan, bukan eksekusi.

2. **Multi-Tenant by Design**
   Isolasi data & konteks adalah default.

3. **API-First & Event-Aware**
   Semua kapabilitas diakses via API & event.

4. **Governed AI**
   Tidak ada AI tanpa policy, audit, dan trace.

5. **Legal-Grade Security**
   Confidentiality > convenience.

---

## 4. High-Level Architecture Diagram (Logical)

```mermaid
graph TD
    User([User: Lawyer / Client])
    
    subgraph Presentation_Layer [Presentation Layer]
        WebUI[Web Frontend: apps/web]
    end

    subgraph AI_Interaction_Layer [AI Interaction Layer]
        Copilot[CopilotKit Layer]
    end

    subgraph AI_Governance_Layer [AI Governance & Orchestration]
        AIOrch[AI Orchestrator: apps/ai-gateway]
        Rules[Rules Engine: packages/rules-engine]
        LLM[LLM Provider]
        PostAudit[Post-Processor + Audit Log]
    end

    subgraph Backend_Layer [Core Backend Layer]
        CoreAPI[Core API: apps/api]
        Worker[Background Worker: apps/worker]
    end

    subgraph Data_Layer [Data & Compliance Layer]
        Data[(Data Layer + Audit Trail)]
    end

    User --> WebUI
    WebUI -->|Context + Intent| Copilot
    Copilot -->|Filtered Prompt| AIOrch
    AIOrch --> Rules
    AIOrch -->|Governed Request| LLM
    LLM --> PostAudit
    PostAudit --> CoreAPI
    CoreAPI --> Data
    Worker -->|OCR/RAG Ingestion| Data
    
    style User fill:#f9f,stroke:#333,stroke-width:2px
    style WebUI fill:#bbf,stroke:#333,stroke-width:2px
    style Copilot fill:#dfd,stroke:#333,stroke-width:2px
    style AIOrch fill:#fdd,stroke:#333,stroke-width:2px
    style Rules fill:#fff4dd,stroke:#d4a017,stroke-width:2px
    style Data fill:#eee,stroke:#333,stroke-width:4px
```

---

## 5. Komponen Utama Sistem

### 5.1 Web Frontend (`apps/web` & `packages/ag-ui`)

**Peran:**

* Menyediakan antarmuka profesional untuk lawyer & klien
* Menjadi host Copilot UI (via `@lawyers-hub/ag-ui`)

**Tanggung jawab:**

* Role-aware UI
* Copilot interaction surface
* Tidak menyimpan logika bisnis

---

### 5.2 CopilotKit & AI Engine (`packages/copilot`)

**Peran:**

* Menjembatani user intent dengan AI
* Menjaga konteks tetap sempit & aman
* Menyediakan mesin RAG dan legal embeddings

**Batasan keras:**

* Tidak akses DB langsung
* Tidak tahu multi-tenant global

---

### 5.3 AI Orchestrator (`apps/ai-gateway`)

**Peran:**

* Merakit prompt final
* Menegakkan policy & rules (.trae)
* Audit setiap interaksi AI

**Catatan penting:**

> Semua interaksi AI melewati layer ini.

---

### 5.4 Core Backend (`apps/api` & `apps/worker`)

**Peran:**

* **Core API:** Single source of truth bisnis & domain services.
* **Background Worker:** Mengolah tugas berat seperti OCR dokumen dan indexing RAG.

**Domain utama:**

* Identity & tenancy
* Case management
* Document service (OCR/RAG)
* Billing
* Audit & compliance

---

### 5.5 Rules Engine (`packages/rules-engine`)

**Peran:**

* Validasi kepatuhan hukum deterministik.
* Mencegah halusinasi AI dengan pengecekan aturan keras.
* Menegakkan batasan prompt (Green/Yellow/Red zones).

---

### 5.6 Data & Audit Layer (`packages/database` & `packages/audit-log`)

**Komponen:**

* PostgreSQL (transactional via Prisma)
* Immutable audit log (logging semua aktivitas user & AI)
* Vector DB / pgvector (AI retrieval)

**Prinsip:**

* Data isolation per tenant (RLS)
* Audit cannot be disabled dan terintegrasi ke setiap layer.

---

## 6. Data & Context Boundary

### 6.1 Context yang Boleh Masuk ke AI

* Ringkasan kasus
* Metadata non-PII
* Dokumen ter-redaksi

### 6.2 Data yang DILARANG

* Identitas klien lengkap
* Informasi finansial mentah
* Data lintas tenant

---

## 7. Alur Interaksi Utama

### 7.1 User → AI (Contoh)

1. Lawyer membuka case
2. Copilot UI aktif dengan context terbatas
3. User meminta draft
4. Policy dicek
5. AI menghasilkan draft
6. Output diberi disclaimer & audit

---

## 8. Security & Compliance Overview

* RBAC + ABAC
* Enkripsi end-to-end
* Prompt & output logging
* UU PDP compliant

---

## 9. Risiko Arsitektural & Mitigasi

| Risiko         | Mitigasi                 |
| -------------- | ------------------------ |
| AI overreach   | Hard policy enforcement  |
| Data leak      | Context filter + masking |
| Vendor lock-in | AI adapter abstraction   |

---

## 10. Stakeholder

* Product Owner
* Engineering Lead
* AI Governance Lead
* Security & Compliance

---

## 11. Versi & Riwayat

| Versi | Tanggal    | Catatan                 |
| ----- | ---------- | ----------------------- |
| 1.0.0 | 2026-01-05 | Initial system overview |

---

## 12. Referensi

* 00_foundation/README.md
* 02_ai_and_rules/prompt_governance.md
* 01_architecture/api_and_service_map.md

---

**Dokumen ini adalah blueprint teknis utama Lawyers Hub.**

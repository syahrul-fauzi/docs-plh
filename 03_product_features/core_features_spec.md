# Core Features Specification — Lawyers Hub `\home\inbox\smart-ai\lawyers-hub\docs\03_product_features\core_features_spec.md` 
 
 ## Metadata 
 
 * **Document ID**: LH-FEAT-CORE-001 
 * **Status**: Draft v0.1 (Built from zero) 
 * **Owner**: Product / System Architect 
 * **Stakeholders**: Legal Ops, Engineering, AI Team, GTM 
 * **Derived From**: 00_foundation/README.md, 01_architecture/system_overview.md 
 
 --- 
 
 ## 1. Tujuan Dokumen 
 
 Mendefinisikan **fitur inti Lawyers Hub** secara sistematis sebagai dasar: 
 
 * Pengembangan MVP & Pilot 
 * Implementasi AG-UI + CopilotKit 
 * Strategi Go-To-Market (GTM) 
 * Kontrol scope & prioritas 
 
 Dokumen ini menjadi **single source of truth** untuk fitur produk. 
 
 --- 
 
 ## 2. Prinsip Perancangan Fitur 
 
 Semua fitur harus mematuhi prinsip berikut: 
 
 1. **Assistive, not Decision-Making AI** 
 2. **Legal Accountability First** 
 3. **Auditability & Traceability by Default** 
 4. **Multi-Tenant & Role-Aware** 
 5. **Composable & API-First** 
 
 --- 
 
 ## 3. Segmentasi Pengguna (Primary Personas) 
 
 ### 3.1 Legal Professional (Lawyer / Firm) 
 
 * Partner 
 * Associate 
 * Paralegal 
 
 ### 3.2 Client (End User) 
 
 * Individu 
 * Korporasi 
 
 ### 3.3 Internal / System 
 
 * Admin Platform 
 * Compliance & Audit 
 
 --- 
 
 ## 4. Daftar Fitur Inti (Core Feature Set) 
 
 ### 4.1 AI Legal Assistant (Copilot) 
 
 **Priority**: P0 (MVP Critical) 
 
 **Deskripsi**: 
 AI Copilot berbasis CopilotKit untuk membantu lawyer dalam: 
 
 * Riset hukum 
 * Draft dokumen 
 * Review kontrak 
 * Klarifikasi regulasi 
 
 **Scope**: 
 
 * Context-aware (case, document, jurisdiction) 
 * Tidak memberikan keputusan hukum final 
 * Semua output bersifat draft & rekomendasi 
 
 **Key Capabilities**: 
 
 * Prompt Governance 
 * Role-based context injection 
 * Source citation 
 * Confidence disclaimer 
 
 --- 
 
 ### 4.2 Case & Matter Management 
 
 **Priority**: P0 
 
 **Deskripsi**: 
 Manajemen perkara terstruktur. 
 
 **Fitur**: 
 
 * Create / Update Case 
 * Case Timeline 
 * Case Notes (manual + AI-assisted) 
 * Attachment & Evidence 
 
 --- 
 
 ### 4.3 Document Automation & Management 
 
 **Priority**: P0 
 
 **Deskripsi**: 
 Otomatisasi dokumen hukum dengan kontrol penuh. 
 
 **Fitur**: 
 
 * Template-based drafting 
 * AI-assisted drafting (Copilot) 
 * Versioning 
 * Approval workflow 
 
 --- 
 
 ### 4.4 Secure Client Communication 
 
 **Priority**: P1 
 
 **Deskripsi**: 
 Komunikasi lawyer–klien yang aman dan teregistrasi. 
 
 **Channel**: 
 
 * In-app chat 
 * WhatsApp (via Gateway) 
 * Email (logged) 
 
 **Compliance**: 
 
 * Consent tracking 
 * Audit log 
 
 --- 
 
 ### 4.5 Onboarding & Verification 
 
 **Priority**: P0 
 
 **Deskripsi**: 
 Onboarding terkontrol untuk lawyer & firm. 
 
 **Fitur**: 
 
 * Lawyer verification 
 * Firm verification 
 * Role assignment 
 
 --- 
 
 ### 4.6 Audit Trail & Compliance 
 
 **Priority**: P0 
 
 **Deskripsi**: 
 Pencatatan seluruh aktivitas kritikal. 
 
 **Audit Scope**: 
 
 * AI interaction 
 * Document changes 
 * Case access 
 * Client communication 
 
 --- 
 
 ### 4.7 Billing & Subscription 
 
 **Priority**: P1 
 
 **Deskripsi**: 
 Monetisasi Lawyers Hub. 
 
 **Model**: 
 
 * Per-seat 
 * Per-case 
 * Usage-based (AI tokens) 
 
 --- 
 
 ## 5. Feature Prioritization Matrix 
 
 | Feature                   | Priority | Phase  | 
 | ------------------------- | -------- | ------ | 
 | AI Copilot                | P0       | MVP    | 
 | Case Management           | P0       | MVP    | 
 | Document Automation       | P0       | MVP    | 
 | Onboarding & Verification | P0       | MVP    | 
 | Audit & Compliance        | P0       | MVP    | 
 | Secure Communication      | P1       | Pilot  | 
 | Billing & Subscription    | P1       | Pilot  | 
 | Advanced Analytics        | P2       | Growth | 
 
 --- 
 
 ## 6. User Flow (High-Level) 
 
 ### Lawyer Flow (MVP) 
 
 1. Sign up & verification 
 2. Create firm / join firm 
 3. Create case 
 4. Draft document with Copilot 
 5. Review & approve 
 6. Share with client 
 
 ### Client Flow 
 
 1. Receive invitation 
 2. View documents 
 3. Communicate securely 
 
 --- 
 
 ## 7. Out of Scope (Explicit) 
 
 * AI making legal decisions 
 * Public legal advice marketplace 
 * Automated court filing (v1) 
 
 --- 
 
 ## 8. Dependency Map 
 
 * CopilotKit (AI interaction) 
 * AG-UI (stateful UI) 
 * Core API (NestJS) 
 * Rules Engine 
 * Audit Service 
 
 --- 
 
 ## 9. Dokumen Terkait 
 
 * 00_foundation/README.md 
 * 01_architecture/system_overview.md 
 * 02_ai_and_rules/prompt_governance.md (next) 
 * GTM Strategy Docs 
 
 --- 
 
 ## 10. Status Penguncian 
 
 🚧 **Draft — Belum terkunci** 
 
 Akan dikunci setelah: 
 
 * Review PO 
 * Review Legal 
 * Review GTM

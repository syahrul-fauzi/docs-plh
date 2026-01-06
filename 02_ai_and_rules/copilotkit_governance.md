# CopilotKit Governance & Implementation — Lawyers Hub

## Metadata

* **Document ID**: LH-AI-COPI-001
* **Status**: Draft v0.1
* **Owner**: AI Architect / Frontend Lead
* **Stakeholders**: Engineering, Product, AI Governance
* **Derived From**: 02_ai_and_rules/prompt_governance.md, 01_architecture/system_overview.md

---

## 1. Tujuan Dokumen

Mendefinisikan standar teknis penggunaan **CopilotKit** di Lawyers Hub untuk memastikan implementasi AI Interaction Layer yang aman, role-aware, dan patuh pada [Prompt Governance](file:///home/inbox/smart-ai/lawyers-hub/docs/02_ai_and_rules/prompt_governance.md).

---

## 2. Arsitektur Integrasi

CopilotKit bertindak sebagai jembatan antara **AG-UI** (Frontend) dan **AI Orchestrator** (Backend).

### 2.1 Frontend Integration (Next.js)
* **CopilotProvider**: Harus dibungkus oleh AuthProvider untuk memastikan ketersediaan `userToken` dan `tenantId`.
* **CopilotSidebar/Popup**: Hanya diaktifkan pada rute yang relevan (Case Management, Document Editor).

### 2.2 Backend Actions (NestJS)
* Semua `useCopilotAction` atau `CopilotAction` harus divalidasi di backend.
* **Backend-only context**: Copilot tidak boleh menarik data langsung dari DB; ia harus melalui Service Layer yang menerapkan RBAC.

---

## 3. Role-Based Access Control (RBAC) di Copilot

| Role | Copilot Capabilities | Constraints |
| :--- | :--- | :--- |
| **Partner** | Full drafting, Strategic analysis, Financial summary | Full audit trail |
| **Associate** | Drafting, Case research, Compliance checklist | Review by Partner required |
| **Client** | Case status Q&A, Document viewing assistance | No legal drafting, strictly informational |

---

## 4. Context Management (Narrowing)

Untuk menghindari *hallucination* dan kebocoran data:

1. **Explicit Context**: Hanya dokumen yang sedang aktif dibuka yang dimasukkan ke dalam `CopilotContext`.
2. **Auto-Purge**: Konteks dibersihkan setiap kali user berpindah Case atau Tenant.
3. **Redaction**: PII (Personal Identifiable Information) harus dimask sebelum dikirim ke LLM melalui CopilotKit.

---

## 5. Security Guardrails

* **API Key Safety**: OpenAI/LLM keys tidak boleh ada di frontend. CopilotKit harus menggunakan backend endpoint proxy.
* **Rate Limiting**: Diterapkan per user/tenant untuk mencegah penyalahgunaan resource AI.
* **System Prompt Injection**: System prompt global didefinisikan di backend Orchestrator, bukan dikirim dari frontend.

---

## 6. Monitoring & Logging

Setiap interaksi melalui CopilotKit wajib mencatat:
* `interaction_id` (UUID)
* `user_id` & `tenant_id`
* `action_name` (misal: `draft_contract_clause`)
* `timestamp`

---

## 7. Status Penguncian

🚧 **Draft — Belum terkunci**

Akan dikunci setelah:
* AI Architect Review
* Frontend Lead Sign-off

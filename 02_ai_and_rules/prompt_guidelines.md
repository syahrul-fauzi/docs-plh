# Prompt Governance & AI Rules — Lawyers Hub `\home\inbox\smart-ai\lawyers-hub\docs\02_ai_and_rules\prompt_governance.md`

## Metadata

- **Document ID**: LH-AI-GOV-001
- **Status**: Draft v0.1 (Built from zero)
- **Owner**: AI Architect / Platform Governance
- **Stakeholders**: Legal, Compliance, Engineering, Product
- **Derived From**: 00_foundation/README.md, 01_architecture/system_overview.md,
  03_product_features/core_features_spec.md

---

## 1. Tujuan Dokumen

Dokumen ini mendefinisikan **kerangka tata kelola (governance)** untuk seluruh
interaksi AI (CopilotKit) di Lawyers Hub, memastikan bahwa:

- AI **bersifat assistive**, bukan pengambil keputusan hukum
- Semua interaksi **terkontrol, dapat diaudit, dan patuh regulasi**
- Tidak terjadi kebocoran data, hallucination berbahaya, atau pelanggaran etika

Dokumen ini adalah **aturan keras (hard guardrail)** untuk semua AI Agent.

---

## 2. Prinsip Utama Prompt Governance

1. **Human-in-the-Loop (Mandatory)**
   - Semua output AI = draft / rekomendasi
   - Keputusan final selalu oleh lawyer

2. **Context is Privilege**
   - AI hanya menerima konteks minimum yang diperlukan
   - Tidak ada implicit global memory

3. **Role & Jurisdiction Aware**
   - Output AI disesuaikan role (Partner, Associate, Client)
   - Yurisdiksi eksplisit (Indonesia default)

4. **Auditability by Design**
   - Setiap prompt, context, dan output tercatat

5. **Fail-Safe over Fail-Smart**
   - Jika ragu → AI harus menolak atau meminta klarifikasi

---

## 3. Klasifikasi AI Interaction

### 3.1 Allowed (Green Zone)

- Drafting dokumen hukum
- Ringkasan regulasi
- Checklist compliance
- Analisis perbandingan (non-decisive)

### 3.2 Restricted (Yellow Zone)

- Strategi litigasi
- Estimasi risiko hukum
- Interpretasi abu-abu

➡️ Wajib disclaimer & explicit review

### 3.3 Forbidden (Red Zone)

- Memberikan keputusan hukum final
- Memberikan nasihat hukum langsung ke klien
- Meniru peran hakim / regulator
- Menggunakan data lintas tenant

➡️ AI **harus menolak**

---

## 4. Prompt Lifecycle (CopilotKit)

### 4.1 Prompt Assembly

Input:

- User intent
- Role
- Case context (optional)
- Document context (optional)

➡️ Diproses oleh **Prompt Orchestrator**

### 4.2 Validation Layer

- Role validation
- Jurisdiction check
- Scope check

Jika gagal → prompt ditolak

### 4.3 Execution

- CopilotKit executes dengan system prompt terkunci
- Temperature & tools dibatasi

### 4.4 Post-Processing

- Disclaimer injection
- Citation enforcement
- Confidence score (opsional)

---

## 5. System Prompt (Canonical)

**Aturan Global:**

- You are a legal assistant, not a lawyer
- You do not give legal advice
- You must ask for jurisdiction if missing
- You must cite sources when possible
- You must refuse forbidden requests

System prompt ini **immutable** di runtime.

---

## 6. Context Injection Policy

| Context Type | Source          | Rules              |
| ------------ | --------------- | ------------------ |
| User Role    | Auth Service    | Mandatory          |
| Firm ID      | Tenant Resolver | Mandatory          |
| Case Data    | Case Service    | Scoped             |
| Document     | DMS             | Explicit selection |

Tidak ada auto-context lintas case atau tenant.

---

## 7. Data Protection & Privacy

- No training on user data
- No cross-tenant memory
- PII masking default
- PDP-compliant logging

---

## 8. Audit & Monitoring

### Logged Items

- Prompt input hash
- Context references (ID only)
- Output hash
- User ID & role
- Timestamp

### Monitoring

- Hallucination rate
- Refusal rate
- Red-zone attempt alerts

---

## 9. Incident Handling

Jika AI melanggar aturan:

1. Immediate flag
2. Output suppressed
3. Audit log marked
4. Governance review

---

## 10. Explicit Non-Goals

- Autonomous legal agents
- Long-term AI memory
- Unsupervised decision-making

---

## 11. Dokumen Terkait

- [Foundation README](../00_foundation/README.md)
- [System Architecture Overview](../01_architecture/system_overview.md)
- [Core Features Specification](../03_product_features/core_features_spec.md)
- [User Journey & Interaction Flows](../03_product_features/user_journey_and_flows.md)
- [Analisis & Rencana Implementasi CopilotKit](<../00_foundation/Analisis%20&%20Rencana%20Implementasi%20%E2%80%94%20Lowyers-Hub%20%C3%97%20CopilotKit%20(agentic%20+%20UI%20+%20actions%20+%20shared%20state).md>)
- Compliance & Audit Docs

---

## 12. Status Penguncian

🚧 **Draft — Belum terkunci**

Akan dikunci setelah:

- Legal review
- Security review
- AI ethics approval

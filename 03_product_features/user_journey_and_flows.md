# User Journey & Interaction Flows — Lawyers Hub `\home\inbox\smart-ai\lawyers-hub\docs\03_product_features\user_journey_and_flows.md`

## Metadata

* **Document ID**: LH-UJ-FLOW-001
* **Status**: Draft v0.1 (Built from zero)
* **Owner**: Product Architect
* **Stakeholders**: UX, Engineering, AI, Legal Ops, GTM
* **Derived From**: [README.md](file:///home/inbox/smart-ai/lawyers-hub/docs/00_foundation/README.md), [system_overview.md](file:///home/inbox/smart-ai/lawyers-hub/docs/01_architecture/system_overview.md), [core_features_spec.md](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/core_features_spec.md), [prompt_governance.md](file:///home/inbox/smart-ai/lawyers-hub/docs/02_ai_and_rules/prompt_governance.md)

---

## 1. Tujuan Dokumen

Mendefinisikan **alur pengguna (user journey)** dan **interaction flow** Lawyers Hub secara end-to-end untuk memastikan:

* Pengalaman konsisten antara AG-UI, CopilotKit, dan backend
* AI muncul di *right moment, right context*
* Tidak ada pelanggaran governance saat interaksi pengguna

Dokumen ini menjadi referensi utama untuk:

* UX Design
* Frontend state management (AG-UI)
* AI entry points

---

## 2. Persona Utama

### 2.1 Lawyer / Legal Professional

* Partner
* Associate
* Paralegal

### 2.2 Client

* Individu
* Korporasi

### 2.3 Internal

* Platform Admin
* Compliance & Audit

---

## 3. High-Level Journey Map

### Lawyer (MVP Scope)

1. Signup & verification
2. Workspace (Firm) setup
3. Case creation
4. Document drafting
5. AI-assisted review
6. Client communication
7. Approval & audit

### Client

1. Invitation received
2. Secure access
3. Document review
4. Communication

---

## 4. Detailed Lawyer Journey

### 4.1 Signup & Verification

**Trigger**: Lawyer opens platform

**Steps**:

1. Register account
2. Submit verification data
3. Await approval

**AG-UI State**:

* `onboarding.pending`

**AI Role**:

* ❌ No AI access

---

### 4.2 Firm Workspace Setup

**Steps**:

1. Create or join firm
2. Assign role

**AG-UI State**:

* `workspace.active`

**AI Role**:

* ❌ No AI

---

### 4.3 Case Creation

**Steps**:

1. Create new case
2. Define jurisdiction & type

**AG-UI State**:

* `case.draft`

**AI Role**:

* Optional checklist suggestion (Green Zone)

---

### 4.4 Document Drafting (AI Entry Point #1)

**Trigger**: Lawyer opens document editor

**AI Capabilities**:

* Draft structure
* Clause suggestions

**AG-UI State**:

* `document.editing`

**Governance**:

* Mandatory disclaimer
* Citation required

---

### 4.5 AI-Assisted Review (AI Entry Point #2)

**Capabilities**:

* Risk highlight
* Consistency check

**Zone**: Yellow

**AG-UI State**:

* `document.review`

---

### 4.6 Client Communication

**Channels**:

* In-app
* WhatsApp (logged)

**AI Role**:

* Draft reply only

---

### 4.7 Approval & Audit

**Steps**:

1. Lawyer approves
2. Document locked

**AG-UI State**:

* `document.final`

**AI Role**:

* ❌ Disabled

---

## 5. Client Journey

### 5.1 Invitation & Access

**Steps**:

1. Receive invite
2. Accept terms

**AG-UI State**:

* `client.active`

---

### 5.2 Document Review

**Capabilities**:

* View only
* Comment

**AI Role**:

* ❌ No legal advice

---

## 6. AG-UI State Model (Simplified)

| Entity   | States                          |
| -------- | ------------------------------- |
| User     | onboarding → active → suspended |
| Case     | draft → active → closed         |
| Document | editing → review → final        |

---

## 7. CopilotKit Interaction Points

| Entry Point        | Context         | Zone   |
| ------------------ | --------------- | ------ |
| Document Draft     | Document + Case | Green  |
| Review Assist      | Document        | Yellow |
| Client Reply Draft | Message         | Green  |

---

## 8. Error & Guardrail UX

* AI refusal explanation
* Governance tooltip
* Manual override path

---

## 9. Out of Scope

* Client-facing AI advice
* Autonomous workflows

---

## 10. Dokumen Terkait

* [Core Features Spec](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/core_features_spec.md)
* [Prompt Governance](file:///home/inbox/smart-ai/lawyers-hub/docs/02_ai_and_rules/prompt_governance.md)
* [Architecture Overview](file:///home/inbox/smart-ai/lawyers-hub/docs/01_architecture/system_overview.md)

---

## 11. Status Penguncian

🚧 **Draft — Belum terkunci**

Akan dikunci setelah UX & Legal review

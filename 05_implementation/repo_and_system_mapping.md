# Repo & System Implementation Mapping — Lawyers Hub `\home\inbox\smart-ai\lawyers-hub\docs\05_implementation\repo_and_system_mapping.md`

## Metadata

- **Document ID**: LH-IMPL-MAP-001
- **Status**: Execution Phase - AI Gateway & RAG Implemented (v0.2)
- **Owner**: System Architect / Tech Lead
- **Stakeholders**: Backend, Frontend, AI, DevOps, Security
- **Derived From**:
  [README.md](file:///home/inbox/smart-ai/lawyers-hub/docs/00_foundation/README.md),
  [system_overview.md](file:///home/inbox/smart-ai/lawyers-hub/docs/01_architecture/system_overview.md),
  [core_features_spec.md](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/core_features_spec.md),
  [prompt_governance.md](file:///home/inbox/smart-ai/lawyers-hub/docs/02_ai_and_rules/prompt_governance.md),
  [user_journey_and_flows.md](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/user_journey_and_flows.md),
  [GTM & Pilot Conversion Architecture.md](file:///home/inbox/smart-ai/lawyers-hub/docs/04_gtm_strategy/GTM%20&%20Pilot%20Conversion%20Architecture.md)

---

## 1. Tujuan Dokumen

Menerjemahkan seluruh dokumen terkunci Lawyers Hub ke dalam **struktur
implementasi nyata** berbasis:

- **Turborepo (monorepo)**
- **Next.js + AG-UI (frontend)**
- **NestJS (core API & services)**
- **CopilotKit (AI runtime)**

Dokumen ini menjadi **blueprint eksekusi teknis**.

---

## 2. High-Level Monorepo Structure

```text
lawyers-hub/
├── apps/
│   ├── web/                # Next.js + AG-UI (Lawyer & Client UI)
│   ├── api/                # NestJS Core API
│   ├── ai-gateway/         # CopilotKit Orchestrator & Prompt Guard
│   └── worker/             # Async jobs (audit, notifications)
│
├── packages/
│   ├── ag-ui/              # Shared AG-UI components & states
│   ├── copilot/            # CopilotKit adapters & policies
│   ├── rules-engine/       # AI & business rules
│   ├── audit-log/          # Audit & compliance utilities
│   ├── auth/               # Auth & RBAC
│   ├── contracts/          # OpenAPI / DTOs
│   └── config/             # Shared config & feature flags
│
├── infra/
│   ├── docker/
│   ├── k8s/
│   ├── terraform/
│   └── observability/
│
├── docs/
└── turbo.json
```

---

## 3. Frontend Mapping — Next.js + AG-UI

### apps/web

**Responsibilities**:

- Lawyer UI
- Client UI
- Demo / Pilot UI

**Key Layers**:

- `app/(workspace)` → firm & case context
- `app/(demo)` → sandbox mode
- `components/` → AG-UI primitives
- `state/` → AG-UI state machines

**AG-UI States** (from locked docs):

- `workspace.demo | active | pilot`
- `case.draft | active | closed`
- `document.editing | review | final`

---

## 4. Backend Mapping — NestJS Core API

### apps/api

**Bounded Contexts**:

- Auth & Tenant
- Case Service
- Document Service
- Client Communication
- Billing
- Audit

**Key Patterns**:

- DDD-lite modules
- Explicit tenant resolver
- Event-driven (domain events)

---

## 5. AI Layer — CopilotKit Orchestration

### apps/ai-gateway

**Responsibilities**:

- Prompt assembly
- Validation (Green / Yellow / Red)
- Context injection
- Execution via CopilotKit

**Flow**:

1. Web → AI Gateway
2. Rules Engine validation
3. CopilotKit execution
4. Post-processing & audit

---

## 6. Rules Engine

### packages/rules-engine

**Rules Types**:

- AI prompt rules
- Feature access rules
- GTM gating rules

**Sources**:

- YAML / JSON DSL
- Derived from docs/rules

---

## 7. Audit & Compliance

### packages/audit-log

**Logged Events**:

- AI interactions
- Document lifecycle
- Client communication

**Storage**:

- Append-only DB / object storage

---

## 8. Auth & Security

### packages/auth

- RBAC
- Tenant isolation
- Role-aware claims

---

## 9. GTM Feature Flags

### packages/config

- Demo vs Pilot vs Production
- AI quota
- Feature availability

---

## 10. DevOps & Deployment

### infra/

- CI/CD via Turborepo pipelines
- Blue/green deploy
- Rollback support

---

## 11. Traceability Matrix

| Doc              | Code Area                                                                                                        |
| ---------------- | ---------------------------------------------------------------------------------------------------------------- |
| Core Features    | [web](file:///home/inbox/smart-ai/lawyers-hub/apps/web), [api](file:///home/inbox/smart-ai/lawyers-hub/apps/api) |
| AI Governance    | ai-gateway, rules-engine                                                                                         |
| User Journey     | ag-ui, web state                                                                                                 |
| GTM Architecture | config, web, api                                                                                                 |

---

## 12. Status

✅ **Monorepo structure aligned** ✅ **AI Gateway initialized & Orchestration
implemented** ✅ **Prompt Guard (Green/Yellow/Red) active** ✅ **Persistent RAG
with Prisma implemented** ✅ **Frontend-Gateway integration active** ✅
**Automated RAG ingestion on document creation** ✅ **Packages renamed and
cross-referenced** ✅ **Build integrity verified (Turbo)** 🚀 **Ready for pilot
feature rollout**

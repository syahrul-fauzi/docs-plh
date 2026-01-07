# Task Distribution: Lawyers Hub

## 🤖 @SOLOCoder (Technical Implementation)

**Focus**: Core logic, AI integration, Frontend/Backend features, Stripe,
Workers.

### Immediate Tasks

1. **PII Masking Service**:
    - Implement `PresidioMaskingService` in `packages/auth`.
    - Add custom regex for Indonesian-specific PII (NIK, NPWP, No. Telp
      Indonesia).
    - Integrate masking into the AI Gateway.
2. **RAG Pipeline Refactor**:
    - Implement hierarchical chunking for legal documents.
    - Add hybrid search (keyword + semantic).
3. **Real-time Collaboration**:
    - Integrate `Yjs` with `Socket.io` for document editing in `apps/web`.

---

## 🏗️ @SOLOBuilder (System Architecture)

**Focus**: Monorepo structure, Database Schema (RLS), AI Gateway,
Infrastructure.

### Immediate Tasks

1. **Prisma RLS Optimization**:
    - Refine Row Level Security (RLS) policies for multi-tenancy.
    - Ensure strict isolation between law firms (tenants).
2. **Vector DB Isolation**:
    - Setup namespace-based isolation in Pinecone/pgvector.
3. **CI/CD Pipeline**:
    - Configure Turborepo cache and parallel execution in GitHub Actions.

---

## 🌟 @WorldClassAgent (Expert Guidance & QA)

**Focus**: Security audits, Compliance, Documentation, Acceptance Criteria, E2E
Testing.

### Immediate Tasks

1. **Compliance Audit**:
    - Verify alignment with UU PDP No. 27/2022.
    - Draft "Right to be Forgotten" implementation plan.
2. **Quality Assurance**:
    - Setup Playwright for E2E testing of the collaboration flow.
    - Implement static code analysis (ESLint + Prettier + SonarQube rules).
3. **Project Oversight**:
    - Maintain `PROJECT_PLAN_V2.md`.
    - Perform peer reviews for all PRs from @SOLOCoder and @SOLOBuilder.

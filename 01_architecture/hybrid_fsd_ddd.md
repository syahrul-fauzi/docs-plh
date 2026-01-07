# Blueprint — Lawyers-Hub (Hybrid FSD + DDD, AI-Centric, Multi-Tenant, Next.js App Router)

Ringkasan singkat: rekomendasi ini adalah blueprint **pragmatis &
production-ready** untuk aplikasi web Lawyers-Hub yang memadukan Feature-Sliced
Design (UI/feature modular) dengan tactical DDD (bounded contexts, aggregate
roots). Fokus pada: AI-first features (document analysis, RAG recommendations,
chatbot), multi-tenant isolation, Next.js App Router modern (Server Components,
Route Groups, Streaming/Suspense), dan infrastructure untuk scalabilitas,
observability, dan QA.

> Catatan: sumber teknis utama dipakai untuk keputusan arsitektural (Next.js App
> Router, multi-tenant patterns, vector DB untuk RAG, Redis caching, BullMQ).
> ([Next.js][1])

---

# 1. High-level architecture (diagram & components)

ASCII diagram (high level):

```
                               +-----------------------------+
                               |    External Identity IdP    |  <-- OIDC / SSO (Auth0 / Keycloak)
                               +-------------+---------------+
                                             |
        +-----------------------+------------+-------------+-----------------------+
        |                       |                          |                       |
        |                       |                          |                       |
  +-----v-----+           +-----v-----+              +-----v-----+           +-----v-----+
  |  Next.js  |  <------> |    Core   | <----------> |  Domain   | <------>  |  Infra    |
  |  App UI   |   REST    |    API    | repositories |  (DDD)    | repos/api |  Adapters  |
  | (Server   |           |  (NestJS) |              |  services |           | (DB, S3,   |
  | Components|           +-----+-----+              +-----+-----+           | VectorDB,  |
  | Streaming)|                 |                          |                 | Redis, SCM) |
  +-----+-----+                 |                          |                 +-----+-----+
        |                       |                          |                       |
        |                       |                          |                       |
 +------+-------+     +---------v---------+        +-------v--------+    +---------v---------+
 |Browser/Client|     | Auth (OIDC) / ACL |        | Background Qs  |    | Vector DB (Pinecone|
 |(SSR/CSR/Edge)|     +-------------------+        | Workers (Bull) |    | / Weaviate) + Emb. |
 +--------------+                                  +----------------+    +---------------------+
```

**Primary components**

- **Next.js App (App Router)**: Server Components for data-heavy render, Route
  Groups for logical grouping, Streaming/Suspense for progressive UX.
  ([Next.js][1])
- **AI Interaction Layer (CopilotKit)**: Orchestrates AI interactions, providing
  a headless or ready-to-use chat UI, and managing state between frontend and AI
  Gateway.
- **Core API (NestJS)**: Central REST API for core legal domains, handling
  authentication, business logic, and data access.
- **AI Gateway (NestJS)**: Dedicated service for AI orchestration, prompt
  governance, and RAG service integration.
- **Domain (DDD)**: bounded contexts: `cases`, `clients`, `documents`,
  `scheduling` (court calendar), `billing`, `compliance`, `ai` (RAG /
  embeddings). Each context exposes domain services + repository interfaces.
- **Infra Adapters**: Prisma + PostgreSQL (multi-tenant), object store (S3),
  vector DB (Pinecone/Weaviate) for embeddings, Redis for caching/queues, BullMQ
  for background jobs. ([pinecone.io][3])
- **AI Layer**: Embeddings pipeline, RAG index, LLM orchestrator (OpenAI /
  Anthropic / private model), model ops for prompt & cost control, document
  OCR/ETL. Use vector DB for similarity search. ([pinecone.io][3])
- **Realtime Collaboration**: CRDT (Yjs) backed by WebSocket / awareness
  provider for collaborative editing of documents. ([Yjs Docs][4])
- **Security & Auth**: OIDC/OAuth2 with per-tenant configuration
  (Auth0/Keycloak/recommended pattern). ([Auth0][5])

---

# 2. Why Hybrid (FSD + DDD) here — design rationale

- **FSD** for front-end: allows parallel, team-scoped work on UI features (chat,
  templates, dashboards). UI code is grouped by feature and imports from
  `features/*`.
- **DDD** for core legal domains: Cases, Documents, Clients require invariants,
  complex business logic, audit trails, and strong isolation for compliance.
  Make aggregates and repositories to keep invariants inside domain boundaries.
- **Hybrid benefit**: UI teams can ship features quickly while domain teams
  evolve robust domain models (aggregate roots, domain events). This reduces
  coupling and improves testability.

---

# 3. Multi-Tenant strategy & recommendation

## Options & tradeoffs

- **Shared schema (tenant_id column)** — cheapest, easiest migrations, good for
  small tenants; needs RLS & strict application layer checks.
- **Schema-per-tenant** — better data isolation, easier per-tenant backups;
  moderate operational overhead.
- **DB-per-tenant** — strongest isolation (best for enterprise / compliance),
  higher cost and orchestration complexity. ([Bytebase][6])

## Recommended (realistic hybrid)

- **Default: Shared schema with explicit `tenantId` + PostgreSQL Row-Level
  Security (RLS) + strong application checks** for most tenants (cost
  effective).
- **Enterprise opt-in: Schema-per-tenant or DB-per-tenant** for regulated
  clients requiring data residency or stronger isolation (provisioned
  automatically). Use feature flags & tenancy provisioning tools. Rationale:
  balances cost, maintenance, and regulatory needs. ([Bytebase][6])

## Implementation details

- Always pass `tenantId` explicitly down stacks (no globals).
- Add middleware at API/Next edge that resolves `tenantId` from auth token /
  organization context and injects into Prisma client context.
- Enforce **RLS policies** in Postgres for table access where shared schema is
  used. Automate schema-per-tenant provisioning for enterprise tiers.
  ([zenstack.dev][7])

---

# 4. Next.js App Router specifics (how to use modern features)

- Use **Server Components** for data-intensive shells (case overview pages,
  document previews). This reduces client JS and speeds rendering.
  ([Next.js][1])
- Use **Route Groups** to organize by area (e.g. `(admin)/`, `(tenant)/`,
  `(public)/` ), keep URLs clean and separate layouts. ([Next.js][8])
- Use **Streaming + Suspense** for progressive load: stream case metadata first,
  then heavy widgets (analytics, AI-summaries) as they resolve. This improves
  perceived performance and allows partial hydration. ([Next.js][9])

**Example file layout (app dir, simplified)**

```
app/
├── (public)/           # marketing, landing pages
├── (tenant)/           # tenant area
│   ├── layout.tsx      # tenant shell (server comp)
│   ├── dashboard/
│   └── cases/
│       └── [caseId]/
│           ├── page.tsx   # Server Component - composes features/cases/ui
│           └── loading.tsx
```

---

# 5. Domain model (tactical DDD snippets)

## Bounded contexts

- **Cases** — aggregate root: `Case` (id, status, parties, events). Domain
  services: litigation workflow, evidence handling, case merging.
- **Documents** — aggregate root: `Document` (versions, signatures, hashes),
  includes document metadata, versioning metadata, PII flags.
- **Clients** — `Client` entity (contacts, relationships, firms)
- **Scheduling** — `Hearing` entity, calendars, court integrations.
- **AI** — `EmbeddingIndex`, `RAGSession`, `ChatSession` (agent orchestration).

## Example Prisma model (shared schema approach)

```prisma
model Tenant {
  id    String  @id @default(cuid())
  name  String
  // ...
}

model Case {
  id         String   @id @default(cuid())
  tenantId   String
  title      String
  status     String
  createdAt  DateTime @default(now())
  updatedAt  DateTime @updatedAt
  @@index([tenantId])
}

model Document {
  id        String @id @default(cuid())
  tenantId  String
  caseId    String?
  fileKey   String // S3 key
  version   Int
  hash      String // file hash (sha256)
  createdAt DateTime @default(now())
  @@index([tenantId, caseId])
}
```

> Always add `tenantId` and indexes; for shared schema, plan RLS policies in SQL
> migration scripts.

(Prisma multi-tenant patterns & examples: see community patterns).
([Medium][10])

---

# 6. AI architecture (document analysis, recommendations, chatbot)

## Core pieces

1. **Document Ingest & ETL**
   - Upload → virus/PII scan → OCR (Tesseract / cloud OCR) → text extraction →
     chunking + metadata extraction (dates, parties, doc type).
   - Compute embeddings per chunk and store embeddings + metadata in Vector DB
     (Pinecone / Weaviate). ([pinecone.io][3])

2. **Index (Vector DB)**
   - Use Pinecone (managed) or Weaviate for scalable semantic search. Index is
     tenant-aware (prefix tenant id in metadata) to isolate per-tenant vectors.
     ([pinecone.io][3])

3. **RAG & Recommender Service**
   - On query: retrieve top-k embeddings (tenant filtered) → assemble context
     with document snippets → call LLM (system + user prompt) → return
     summarized answer / ranking for recommendation.

4. **Chatbot / Agent**
   - Chat sessions managed in domain (`ChatSession`), orchestrator composes
     retrieval, chain-of-thought constraints, safety filters, and sends to LLM.
     Keep conversation history as events (not raw LLM outputs) for auditability.

5. **Model Ops & Cost Control**
   - Rate limits, quotas by tenant (AI quota stored in billing domain), LLM
     choice per tenant (cheaper vs higher-quality models), caching of recent
     answers for identical queries.

6. **Privacy**
   - Do **not** log raw PII to LLM providers unless tenant consent and
     contractual agreements; always anonymize or use private models when
     required.

**Why Vector DB?** for fast semantic retrieval enabling RAG recommendations and
similarity search across large corpora. ([pinecone.io][3])

---

# 7. API & Data access layer

## REST API (NestJS)

- **Controller-based design**: each domain service exposes REST endpoints via
  NestJS controllers. Use `HttpRepository` patterns in frontend to consume these
  APIs.
- **OpenAPI (Swagger)**: Automatically generate API documentation for easier
  frontend integration and testing.
- **Auth / Authorization**:
  - Use middleware to resolve tenant & user claims from JWT/OIDC token; enforce
    RBAC using NestJS Guards and Decorators.

## Prisma usage

- Instantiate Prisma per request with `tenantId` in context. For
  schema-per-tenant, create a prisma instance pointing to tenant schema/db
  dynamically (connection pool + caching). Use generated types for domain
  models. ([zenstack.dev][7])

---

# 8. Background processing & caching

## BullMQ (jobs & workers)

- Use BullMQ (Redis-backed) for CPU/IO heavy jobs:
  - Document OCR & embedding generation
  - Document hashing & notarization tasks
  - Long running RAG preprocessing
  - Notification/email/webhook delivery

- Workers scale horizontally; use separate worker groups for `ocr`,
  `embeddings`, `notarize`, `billing`. ([BullMQ][12])

## Redis (caching & distributed locking)

- Redis usage:
  - **Distributed cache**: response caching for REST APIs and LLM responses
    using Redis.

- **Leader election & locks**: ensure single worker executes tenant
  migrations/cron tasks
- **BullMQ backend**: Redis holds job queues
- Use TTLs and tenant namespacing in keys. ([Redis Documentation][2])

---

# 9. Document notarization (blockchain) — design concept

- Use **IPFS** for content storage and store content hash (CID) + timestamp on
  blockchain (Ethereum or private chain) as proof-of-existence / tamper-proof
  audit trail. Use optional enterprise flows to record notarization
  transactions. ([Moralis | Enterprise-Grade Web3 APIs][13])
- Keep signing keys in HSM/Secrets Manager; store only the hash on-chain (not
  the document). Maintain mapping in domain `Document` with `notarizationTx`,
  `ipfsCid`, `notarizedAt`.

**Note:** blockchain integration is optional & costly — provide it as an
enterprise feature.

---

# 10. Real-time collaboration

- Use **Yjs (CRDT)** for collaborative editing (document redlining,
  collaborative drafting). Use a server provider (WebSocket or WebRTC) that
  persists Yjs updates to a history store (append-only) and rehydrate sessions
  from document latest state. ([Yjs Docs][4])
- Respect per-tenant isolation — separate collaboration rooms by tenant + case
  id.

---

# 11. Security & Compliance (key controls)

- **Auth**: OIDC/OAuth2 (Auth0/Keycloak), support per-tenant OIDC configuration.
  Provide SCIM/IdP provisioning for enterprise. ([Auth0][5])
- **Data isolation**: tenantId everywhere + RLS for shared schemas; optional
  schema/db per enterprise tenant. ([Bytebase][6])
- **PII handling**: redact before sending to external LLMs unless consented;
  store sensitive fields encrypted (at rest & in transit), keep audit logs
  immutable.
- **Secrets & keys**: use Secrets Manager, rotate keys, store signing keys in
  HSM.
- **Network**: use mTLS between services in Kubernetes; restrict admin APIs to
  private networks.

---

# 12. Observability & reliability

- **Tracing**: OpenTelemetry traces from Next.js → API → Domain → infra
  downstream (LLM calls, vector DB).
- **Metrics**: Prometheus + Grafana dashboards (latencies per tenant, queue
  backlog, LLM tokens/costs).
- **Errors**: Sentry/Log aggregation with tenant context.
- **Health**: k8s liveness/readiness probes for web + workers.

---

# 13. Testing & QA (strategy & tools)

- **Unit tests (domain logic)**: vitest/jest for TS domain services (aggregate
  invariants).
- **Integration tests (API)**: spin up ephemeral DB (testcontainers) + Supertest
  for API endpoints.
- **E2E tests**: Playwright for core user flows (case open, doc upload, chat).
  ([Playwright][14])
- **Load testing**: k6 for API/ingest/LLM throughput scenarios; simulate heavy
  embedding ingest & RAG queries. ([Grafana Labs][15])
- **Security testing**: dependency scanning, SAST (Snyk/Trivy), pen test for
  enterprise clients.

---

# 14. Data flow diagrams (simplified)

## Document ingest -> RAG (sequence)

1. User uploads file (browser) → Next.js server component receives file and
   stores to S3 (signed URL upload).
2. API enqueues `document.process` job (BullMQ) with tenantId + fileKey.
   ([BullMQ][12])
3. Worker downloads file → OCR & text extraction → chunking → compute embeddings
   (embedding service or model) → store embeddings + metadata in VectorDB
   (tenant namespace). ([pinecone.io][3])
4. Worker updates `Document` aggregate with versions & embed status.
5. When user asks question: REST endpoint sends retrieval query (tenant
   filtered) to VectorDB → top-k results → LLM request → API returns answer.

## AI Chat Flow (CopilotKit)

```
Client --> CopilotKit (Frontend) --> AI Gateway (CopilotKit Backend)
AI Gateway --> RAG Service (retrieve embeddings -> LLM)
RAG Service --> VectorDB -> returns snippets
RAG Service --> LLM -> response
AI Gateway --> Client
```

---

# 15. Example REST API endpoints (conceptual)

```typescript
// Case management
GET /cases/:id
POST /cases/:id/documents
GET /cases/:id/timeline

// AI / RAG
POST /ai/ask
POST /ai/summarize-document/:docId

// Compliance
GET /compliance/alerts
```

Endpoint handlers enforce `tenantId` from context; results are tenant scoped.

---

# 16. Operational & deployment recommendations

- **Kubernetes** cluster (EKS/GKE/AKS) with autoscaling for web & worker
  deployments.
- Use **managed Postgres (RDS/AzureDB)** or managed CockroachDB for
  geo-distribution when needed.
- Use **managed vector DB (Pinecone)** for scale and reduced operational
  overhead. ([pinecone.io][3])
- **Redis**: clustered managed Redis (AWS Elasticache or equivalent).
- **Storage**: S3 compatible (AWS/GCP/Azure) with lifecycle, encryption.
- CI/CD: GitHub Actions / GitLab CI with infrastructure provisioning via
  Terraform; run tests, dependency checks, `dependency-cruiser` rules, SonarQube
  scan.

---

# 17. Measurable success criteria

- Maintainability: +10–20 SonarQube points after migration.
- Cyclomatic complexity: per-file threshold <= 10 and median reduction 30%.
- Latency: page TTFB < 300ms for server components (typical).
- AI cost: track tokens per tenant, set quota alerts.
- Reliability: queue backlog (jobs) under SLA; worker failure rate < 1/week.

---

# 18. Roadmap / Implementation plan (6 iterations — pilot approach)

1. **Sprint 0 — Foundation**
   - Set up monorepo / tsconfig paths / linting & dependency rules. Add
     `features/` and `domain/` skeletons. Configure Core API basic handlers.

2. **Sprint 1 — Cases pilot + AI ingest**
   - Implement `cases` domain + `documents` ingest pipeline (BullMQ worker +
     S3). Wire embeddings to a sandbox Pinecone index.

3. **Sprint 2 — REST API & Next.js**
   - REST controllers for cases & documents; Next.js case page using Server
     Component & streaming. Add route groups. ([Next.js][1])

4. **Sprint 3 — Chatbot & RAG**
   - Implement chat session domain, RAG orchestrator, LLM integration (safe
     defaults + quotas) using CopilotKit.

5. **Sprint 4 — Multi-tenant hardening**
   - Add `tenantId` propagation, RLS policies for shared schema, migration
     scripts, and tenant onboarding automation. ([Bytebase][6])

6. **Sprint 5 — Real-time & notarization**
   - Add Yjs based collaboration; optional blockchain notarization POC (IPFS +
     Ethereum). ([Yjs Docs][4])

---

# 19. Quick-start artifacts I can generate now (pick any)

I can **immediately** generate (copy-paste ready):

- `app/` recommended Next.js file skeleton (route groups + server component
  examples using Suspense / loading.tsx). ([Next.js][9])
- Prisma schema starter with tenant columns + example RLS migration SQL (for
  Postgres). ([zenstack.dev][7])
- REST API skeleton (NestJS integration) with tenant middleware.
- BullMQ worker & queue starter code + job examples. ([BullMQ][12])
- ETL worker pseudocode to compute embeddings & push to Pinecone.
  ([pinecone.io][3])

Pilih satu atau lebih artefak yang Anda mau saya buat sekarang — saya akan
langsung keluarkan file/konfigurasi lengkap untuk disalin ke repo.

---

# 20. Key references & further reading

- Next.js App Router, Server Components, Streaming & Route Groups.
  ([Next.js][1])
- Multi-tenant patterns (shared/schema/db) and tradeoffs. ([Bytebase][6])
- Pinecone (vector DB) for embeddings & RAG. ([pinecone.io][3])
- BullMQ documentation for background jobs. ([BullMQ][12])
- Yjs docs for CRDT collaboration. ([Yjs Docs][4])
- IPFS + Ethereum tutorials for notarization POC. ([Moralis | Enterprise-Grade
  Web3 APIs][13])
- Playwright & k6 for E2E and load testing. ([Playwright][14])

---

Jika Anda setuju dengan blueprint ini, sebutkan **artefak** mana yang mau dibuat
dulu (mis. “Prisma schema + RLS migration”, “Next.js server component case
page + streaming example”, “BullMQ worker + job types”, atau “RAG ETL worker +
Pinecone integration”). Saya akan langsung hasilkan file-file/config yang dapat
Anda commit.

[1]:
  https://nextjs.org/docs/app/getting-started/project-structure?utm_source=chatgpt.com
  'Getting Started: Project Structure | Next.js'
[2]:
  https://redis.io/docs/latest/develop/data-types/strings/
  'Redis Strings & Caching | Redis Documentation'
[3]:
  https://www.pinecone.io/?utm_source=chatgpt.com
  'Pinecone: The vector database to build knowledgeable AI'
[4]: https://docs.yjs.dev/?utm_source=chatgpt.com 'Yjs Docs: Introduction'
[5]:
  https://auth0.com/docs/get-started/auth0-overview/create-tenants/multi-tenant-apps-best-practices?utm_source=chatgpt.com
  'Multi-Tenant Applications Best Practices - Auth0'
[6]:
  https://www.bytebase.com/blog/multi-tenant-database-architecture-patterns-explained/?utm_source=chatgpt.com
  'Multi-Tenant Database Architecture Patterns Explained - Bytebase'
[7]:
  https://zenstack.dev/blog/multi-tenant?utm_source=chatgpt.com
  'Multi-Tenancy Implementation Approaches With Prisma and ZenStack'
[8]:
  https://nextjs.org/docs/app/api-reference/file-conventions/route-groups?utm_source=chatgpt.com
  'File-system conventions: Route Groups - Next.js'
[9]:
  https://nextjs.org/docs/14/app/building-your-application/routing/loading-ui-and-streaming?utm_source=chatgpt.com
  'Routing: Loading UI and Streaming - Next.js'
[10]:
  https://medium.com/techkoala-insights/7-advanced-prisma-schema-patterns-for-complex-database-architecture-and-multi-tenant-applications-ac81ce771ed1?utm_source=chatgpt.com
  '7 Advanced Prisma Schema Patterns for Complex Database ...'
[11]:
  https://docs.nestjs.com/controllers
  'Controllers | NestJS - A progressive Node.js framework'
[12]:
  https://bullmq.io/?utm_source=chatgpt.com
  'BullMQ - Background Jobs processing and message queue for ...'
[13]:
  https://moralis.com/ipfs-ethereum-tutorial-how-to-use-ipfs-with-ethereum/?utm_source=chatgpt.com
  'IPFS Ethereum Tutorial - How to Use IPFS with Ethereum - Moralis'
[14]:
  https://playwright.dev/?utm_source=chatgpt.com
  'Playwright: Fast and reliable end-to-end testing for modern web apps'
[15]:
  https://grafana.com/docs/k6/latest/?utm_source=chatgpt.com
  'Grafana k6 documentation'

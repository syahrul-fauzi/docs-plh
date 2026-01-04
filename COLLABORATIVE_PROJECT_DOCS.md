# Lawyers Hub Project Documentation - V2

## 1. Project Overview & Research
Proyek ini bertujuan untuk membangun platform hukum berbasis AI yang aman, skalabel, dan patuh regulasi. Berdasarkan penelitian terbaru:
- **AI Monitoring**: Implementasi menggunakan strategi "Multi-metric Gating" (Error Rate, Latency, Drift).
- **Compliance**: Mengadopsi standar UU PDP/GDPR dengan "Context-aware PII Masking".
- **Detail Teknis**: Lihat [TECHNICAL_SPEC.md](file:///home/inbox/smart-ai/lawyers-hub/docs/TECHNICAL_SPEC.md).

## 2. Distributed Agent Roles & Responsibilities

### @SOLOBuilder (Architect & Integrator)
- **Architecture**: Micro-monorepo menggunakan NPM Workspaces dan Turbo.
- **Integration**: Mengelola resolusi modul antar package (`@lawyers-hub/*`) melalui konfigurasi `tsconfig.json` yang tersentralisasi.
- **Workflow**: Optimasi pipeline build dan development menggunakan Turbopack.

### @SOLOCoder (Core Developer)
- **Frontend**: Implementasi visualisasi data menggunakan `recharts` dan optimasi komponen `MotionWrappers`.
- **Backend**: Pengembangan `AIRoutingService` dan `EmailService` untuk logika monitoring Canary.
- **Testing**: Penulisan unit test untuk logika bisnis kritikal.

### @WorldClassAgent (Expert Advisor & QA)
- **Compliance**: Memastikan fitur sesuai dengan regulasi perlindungan data (UU PDP).
- **Quality Gate**: Melakukan review terhadap hasil build, performa bundle, dan cakupan testing.
- **Strategic Guidance**: Menetapkan threshold monitoring berdasarkan standar industri (10% error rate threshold).

---

## 3. Technical Specifications

### System Architecture
```mermaid
graph TD
    User((User)) --> Web[apps/web: Next.js 16]
    Web --> API[apps/api: NestJS]
    API --> DB[(Prisma / Postgres)]
    API --> AI[AI Model Service]
    API --> Email[Nodemailer / SES]
    
    subgraph Packages
        Core[@lawyers-hub/core]
        Security[@lawyers-hub/security]
        Database[@lawyers-hub/database]
    end
    
    API -.-> Core
    API -.-> Security
    Web -.-> Core
```

- **Monorepo Structure**:
  - `apps/web`: Next.js 16.1.1 (App Router, Turbopack)
  - `apps/api`: NestJS (REST API, Prisma ORM)
  - `packages/core`, `packages/security`, `packages/database`, `packages/domain`: Shared logic & types.

### Canary Alerting Requirements
- **Threshold**: Error rate > 10%.
- **Duration**: Kontinu selama 30 menit.
- **Alert Cooldown**: 1 jam untuk menghindari spam email.
- **Recipients**: Dikonfigurasi via environment variables (`ADMIN_EMAIL`).

### Tech Stack Dependencies
- **Frontend**: `next`, `recharts`, `framer-motion`, `lucide-react`, `clerk`.
- **Backend**: `@nestjs/common`, `@nestjs/schedule`, `nodemailer`, `prisma`, `class-validator`.

---

## 4. Development Timeline & Milestones

| Milestone | Description | Status |
|-----------|-------------|--------|
| M1: Build Fixes | Resolusi isu module resolution dan build apps/web | Completed |
| M2: Canary Logic | Implementasi AIRoutingService dan EmailService | Completed |
| M3: Recharts Integration | Visualisasi data dashboard menggunakan Recharts | Completed |
| M4: Bundle Optimization | Analisis dan optimasi bundle Next.js 16 | In Progress |
| M5: Quality Gate | Full test suite execution & documentation | Pending |

---

## 5. Acceptance Criteria
- [x] `npm run build` berhasil untuk `apps/web` dan `apps/api`.
- [x] Unit tests untuk Canary alerting lulus 100%.
- [x] Laporan kompatibilitas Recharts tersedia.
- [x] Dashboard menampilkan grafik secara responsif.
- [x] Sistem email alert berfungsi saat simulasi violation.

---

## 6. Automated Operations & Advanced Compliance

### Automated Model Promotion
- **Logic**: Canary models are promoted after 48h of stability (no drift detected).
- **Rollback**: Automatic revert to previous stable version if drift > threshold occurs in Production.
- **Service**: `ComplianceScheduler` handles evaluations every 6 hours.

### Irreversible Anonymization
- **Retention**: Data older than 1 year is automatically anonymized.
- **Algorithm**: Truncated SHA-256 hashing with secure salt.
- **Verification**: Automatic pattern check for anonymized tokens.
- **Service**: `AnonymizationService`.

### User Activity Risk Scoring
- **Scoring Model**: Weighted average of Volume (40%), Sensitivity (30%), and Unmasking actions (30%).
- **Thresholds**:
  - Low (0-30): Normal activity.
  - Medium (31-70): Requires manual review.
  - High (71-100): Immediate alert and potential automated block.
- **Service**: `ComplianceService.calculateUserRiskScore`.

---

## 7. Version Management Strategy
- **Branching**: `main` (production), `develop` (integration), `feature/*` (development).
- **Commits**: Mengikuti standar Conventional Commits (misal: `feat(api): add canary alert logic`).
- **Tagging**: Menggunakan Semantic Versioning (v1.x.x).

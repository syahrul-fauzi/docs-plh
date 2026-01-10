# Production Integration & Migration Plan

**Target Version:** 1.0.0  
**Scheduled Date:** TBD  

## 1. Migration Strategy

### Database Migration
*   **Type**: Schema Update & Data Seeding
*   **Tools**: Prisma Migrate (`npx prisma migrate deploy`)
*   **Steps**:
    1. Backup existing Production DB: `pg_dump > backup_pre_v1.sql`
    2. Apply migrations: `npx prisma migrate deploy`
    3. Verify schema integrity.
*   **Rollback**:
    *   Restore from backup: `psql < backup_pre_v1.sql`

### API Versioning
*   **Current Strategy**: Path-based (`/api/v1/...` implied, currently `/api/...`).
*   **Changes**: No breaking API changes in this release. Backward compatible.

### Dependency Mapping
*   **Upstream**:
    *   Clerk Auth (Production Instance)
    *   OpenAI API (GPT-4o)
*   **Downstream**:
    *   PostgreSQL Database (v15+)
    *   Redis (for WebSocket Adapter - optional but recommended)

### Expected Downtime
*   **Scenario A (Zero Downtime)**: Rolling update. API remains available. WebSocket connections will reconnect.
*   **Scenario B (Cold Restart)**: ~30 seconds for Node.js process restart.
*   **Scenario C (Database Restore)**: ~15-30 minutes (depends on DB size).

## 2. Rollback Procedures

### Trigger Conditions
*   Error Rate > 1% over 5 minutes.
*   P95 Latency > 5s over 5 minutes.
*   Critical User Journey failure (e.g., Login or Save Draft fails).

### Manual Rollback Steps
1.  **Identify Issue**: Confirm severity via Monitoring Dashboard.
2.  **Revert Deployment**:
    *   If Docker/K8s: `kubectl rollout undo deployment/lawyers-hub-web`
    *   If Vercel/Netlify: "Instant Rollback" to previous deployment ID.
    *   If VM/VPS: Symlink switch to `releases/v0.9.9`.
3.  **Database Rollback** (If required):
    *   Stop Application.
    *   Restore DB Backup.
    *   Start Application (Old Version).
4.  **Verification**:
    *   Run Smoke Tests on rolled-back instance.
5.  **Communication**:
    *   Notify stakeholders via `#incident-response` channel.
    *   Draft Post-Mortem.

## 3. Monitoring & Alerts

### Key Metrics (APM)
*   **Throughput**: Request Count / Minute.
*   **Latency**: P50, P95, P99.
*   **Error Rate**: HTTP 5xx %.
*   **Resource Usage**: CPU, Memory.

### Alert Thresholds
*   **High Urgency (Page)**:
    *   Uptime Check Fail.
    *   Error Rate > 5%.
*   **Medium Urgency (Email/Slack)**:
    *   Latency P95 > 2s.
    *   CPU > 80%.

## 4. Change Management

### Release Notes (Draft)
**New Features**:
*   Real-time Collaborative Drafting (v1.0).
*   Case Management Dashboard.
*   AI Copilot Integration (Beta).

**Known Issues**:
*   Favicon missing in some views (Low impact).
*   Demo Mode enabled by default (Must disable for Prod).

### Deployment Checklist (Production)
- [ ] `NEXT_PUBLIC_BYPASS_CLERK` set to `false`.
- [ ] Real Database Connection String verified.
- [ ] Clerk API Keys (Production) configured.
- [ ] OpenAI API Key configured.
- [ ] Database Backup completed.

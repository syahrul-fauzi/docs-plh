# Secret Rotation Strategy: CLERK_SECRET_KEY

## 1. Objective
To implement a secure, automated, and zero-downtime rotation mechanism for the `CLERK_SECRET_KEY` and other critical credentials, integrating with HashiCorp Vault or AWS Secrets Manager.

## 2. Rotation Architecture

### 2.1. Dual-Key Support (Rolling Updates)
To avoid downtime, the application must support at least two keys simultaneously during rotation:
- **Current Key**: The active key used for signing/verifying.
- **Previous Key**: Valid for a grace period (e.g., 24h) to allow in-flight requests to complete.
- **Next Key**: Pre-staged for the next rotation cycle.

### 2.2. Infrastructure
- **Vault**: HashiCorp Vault (or AWS Secrets Manager) stores the secrets.
- **Orchestrator**: A scheduled job (GitHub Actions or Cron) triggers the rotation.
- **Application**: Consumes secrets via environment variables injected at runtime or via a sidecar/SDK.

## 3. Implementation Steps

### Phase 1: Preparation
- [ ] Update `env.ts` to support multiple keys (e.g., `CLERK_SECRET_KEY_PRIMARY`, `CLERK_SECRET_KEY_SECONDARY`).
- [ ] Refactor auth middleware to try the primary key first, then fall back to the secondary key on failure.

### Phase 2: Integration
- [ ] Set up a Vault instance (dev/prod).
- [ ] Configure the Application to fetch secrets from Vault on startup (or use an Agent Injector).

### Phase 3: Automation Logic
1.  **Generate** new key in Clerk Dashboard (via API).
2.  **Write** new key to Vault as `primary`, move old `primary` to `secondary`.
3.  **Trigger** a rolling restart of the application to pick up new secrets (if not using dynamic reload).
4.  **Verify** health check passes with new key.
5.  **Revoke** the old `secondary` key after grace period.

## 4. Operational Procedures

### Emergency Rollback
If a new key fails:
1.  Run the `rollback-secret` script.
2.  Script promotes `secondary` (old working key) back to `primary`.
3.  Application restarts immediately.

### Audit Trail
- All rotation events must be logged to the persistent Audit Log.
- Logs must include: `timestamp`, `initiator` (system/user), `key_id` (partial hash), `status`.

## 5. Security Policies
- Rotation Frequency: Every 30 days (automated).
- Access Control: Only the CI/CD pipeline and Admin role have access to the rotation scripts.

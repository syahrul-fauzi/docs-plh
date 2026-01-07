# Observability and Deployment Documentation

## 1. Monitoring Setup (Prometheus & Grafana)

The Lawyers Hub platform uses Prometheus for metric collection and Grafana for
visualization, specifically focused on compliance monitoring and system health.

### Prometheus Configuration

- **Metrics Collected**:
  - `legal_compliance_rate_ratio`: Ratio of documents passing legal compliance
    checks.
  - `rag_retrieval_latency_seconds`: Latency of document chunk retrieval.
  - `active_collaborative_sessions`: Number of active Yjs/Socket.io sessions.
- **Alerting Rules**:
  - `HighComplianceViolationRate`: Triggers if the compliance rate drops below
    85% for 5 minutes.
  - `CriticalRAGLatency`: Triggers if retrieval latency exceeds 2 seconds.
  - `ZeroExecutionsDetected`: Alerts if no compliance checks are being executed
    (system stall).

### Grafana Dashboard

- **Main Dashboard**: "Lawyers Hub - Compliance & Performance"
- **Panels**:
  - **Compliance Gauge**: Real-time compliance rate with green (>95%), yellow
    (85-95%), and red (<85%) thresholds.
  - **Latency Graph**: 95th percentile latency for RAG operations.
  - **Active Users**: Concurrent users across all tenants.

---

## 2. Deployment Procedures

### Database Row-Level Security (RLS)

Multi-tenancy isolation is enforced at the database level using PostgreSQL RLS
policies.

1. **Preparation**:
    - Ensure `DATABASE_URL` is set in the environment.
    - Ensure the database user has permissions to create policies and enable
      RLS.

2. **Execution**:

    ```bash
    npm run db:setup-rls --workspace=@lawyers-hub/database
    ```

    This script performs the following:
    - Enables RLS on all sensitive tables (`documents`, `document_chunks`,
      `cases`, `drafts`).
    - Creates policies to filter data based on `app.current_tenant` setting.
    - Verifies that policies are correctly applied to all expected tables.

3. **Post-Execution Verification**:
    - The script will output a verification summary. Ensure "Missing RLS
      policies" count is 0.
    - Manually verify by attempting to query without setting
      `app.current_tenant` (should return 0 results).

### RAG Pipeline Deployment

1. **Embedding Service**: Configure `OPENAI_API_KEY` to use
    `text-embedding-3-small`.
2. **Vector Store**: Ensure `pgvector` extension is enabled in the database.
3. **Hierarchical Chunking**: The `LegalChunker` automatically handles
    BAB/Pasal/Ayat structures for Indonesian legal documents.

---

## 3. Post-Deployment Checklist

- [ ] Execute `npm run db:setup-rls` and verify policies.
- [ ] Run `npx playwright test` to validate 5+ concurrent user collaboration.
- [ ] Verify Prometheus is scraping metrics from `/metrics` endpoint.
- [ ] Check Grafana dashboard for data flow.
- [ ] Conduct manual PII masking test on sensitive document upload.
- [ ] Obtain stakeholder sign-off on Milestone 2 (Security & RAG).

# Post-Deployment Verification Checklist: Lawyers Hub

## 1. Database & Security (RLS)
- [ ] Execute `npm run db:setup-rls` and verify 13/13 policies are active.
- [ ] Confirm `pgvector` extension is enabled in production schema.
- [ ] Verify that the `app.current_tenant` session variable is correctly set by the backend middleware.
- [ ] Test cross-tenant access: Attempt to query `document_chunks` with a mismatched `tenantId` (should return 0 results).

## 2. AI & RAG Pipeline
- [ ] Verify `OPENAI_API_KEY` is active and has sufficient quota.
- [ ] Test document indexing: Upload a 10+ page legal document and verify hierarchical chunking (BAB/Pasal/Ayat).
- [ ] Test hybrid search: Perform a query using legal terminology and verify that citations include relevant articles.
- [ ] Confirm PII masking: Verify that NIK and NPWP data are redacted in LLM request logs.

## 3. Real-time Collaboration
- [ ] Verify Socket.io connection success rate across distributed regions.
- [ ] Test concurrent editing: 5+ users editing the same draft simultaneously without CRDT conflicts.
- [ ] Verify that cursor positions and user presence colors are visible to all participants.
- [ ] Test "Save Changes" functionality and verify data persistence in PostgreSQL.

## 4. Monitoring & Observability
- [ ] Confirm Prometheus is scraping metrics from the Rules Engine.
- [ ] Verify `legal_compliance_rate_ratio` is visible in the Grafana dashboard.
- [ ] Test alert firing: Simulate a rule violation and verify that the Slack/Email alert is triggered.
- [ ] Check logs for any unhandled exceptions or rate-limiting warnings from AI providers.

## 5. Stakeholder Sign-off
- [ ] Technical Lead Approval: ____________________ Date: __________
- [ ] Legal Compliance Officer Approval: ____________________ Date: __________
- [ ] Product Owner Approval: ____________________ Date: __________

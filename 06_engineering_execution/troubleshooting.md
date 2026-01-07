---
title: Troubleshooting Guide
version: 1.0.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [troubleshooting, debug, faq, errors]
agent_context: This document provides solutions to common issues encountered during development, deployment, and runtime in the Lawyers Hub ecosystem.
---

# 🛠️ Troubleshooting Guide

## 1. Local Environment Issues

### Prisma Sync Errors
**Issue**: `PrismaClient` is out of sync with the database schema.
**Solution**:
```bash
npx turbo run db:generate
npx turbo run db:push
```

### Turbo Cache Issues
**Issue**: Build or test results are inconsistent or stale.
**Solution**: Clear the turbo cache:
```bash
rm -rf node_modules/.cache/turbo
```

## 2. Monorepo & Dependency Issues

### Package Resolution Errors
**Issue**: `Cannot find module '@lawyers-hub/shared'` after adding a new dependency.
**Solution**:
1. Run `npm install` from the root.
2. Ensure the package is correctly linked in `package.json` under `dependencies` using the `workspace:*` syntax.
3. Restart the TS Server in your IDE.

### Build Failures in CI/CD
**Issue**: Turbo build fails on GitHub Actions but works locally.
**Solution**: 
- Check for case-sensitive file naming (Linux is case-sensitive, MacOS/Windows often aren't).
- Ensure all environment variables needed for build-time (e.g., `NEXT_PUBLIC_*`) are defined in the CI secrets.

## 3. AI & RAG Issues

### PII Masking False Positives
**Issue**: The `PresidioMaskingService` is masking non-sensitive legal terminology.
**Solution**: Update the custom allowlist in `packages/security/src/pii-config.ts` to include the specific legal terms.

### Vector Search No Results
**Issue**: RAG retrieval returns empty context even for indexed documents.
**Solution**: 
1. Verify the `tenantId` metadata is correctly applied during ingestion.
2. Check the embedding model version compatibility between ingestion and retrieval.

## 3. Database & Multi-tenancy

### RLS Policy Violations
**Issue**: Queries return 0 results even when data exists.
**Solution**: Ensure the `tenantId` is being correctly set in the Postgres session:
```sql
SET app.current_tenant_id = 'your-tenant-id';
```
In the app, verify that `PrismaService.withTenant()` is being called.

## 5. Real-time Collaboration (Yjs/WebSockets)

### WebSocket Connection Refused
**Issue**: Collaborative editor shows "Disconnected" or fails to sync.
**Solution**:
1. Check if the `Socket.io` server is running on the configured port (default 4000).
2. Ensure the firewall allows incoming traffic on that port.
3. Verify that the `CORS` configuration in `main.ts` includes your frontend domain.

### CRDT State Desync
**Issue**: Two users see different versions of the same document.
**Solution**: 
- Check the Redis adapter for Yjs. Ensure all instances of the API are connected to the same Redis cluster.
- Clear the Redis cache for that specific document ID to force a re-sync from the primary database.

## 6. Deployment Issues

### Docker Build Failures
**Issue**: Out of memory errors during `turbo build`.
**Solution**: Increase Docker resource limits or use the `--no-cache` flag to start fresh.

---
*Still stuck? Create an issue in the repository or contact the @SRE-Team.*

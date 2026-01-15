# Phase 1: Parallel Beta Implementation Guide

This document outlines the infrastructure and procedures for the "Parallel Beta" phase, where the new URL-based tenant architecture runs alongside the legacy header/subdomain-based system.

## 1. Parallel Testing Infrastructure

We have established a parallel testing suite using **Playwright** to verify feature parity between the two systems.

### Parity Test Suite
Located at: `apps/web/test/e2e/parity-check.spec.ts`

This suite performs the following comparative analysis:
1.  **UI Parity**: Visits both `/dashboard` (Legacy) and `/:tenantId/dashboard` (Modern) to verify visual and content consistency.
2.  **Functional Parity**: Navigates through critical paths (Settings, etc.) in both modes.
3.  **Context Propagation**: Intercepts network requests to ensure `x-tenant-id` headers are correctly injected in both scenarios.

### Running the Tests
```bash
# Run only the parity checks
npx playwright test test/e2e/parity-check.spec.ts
```

## 2. Telemetry & Monitoring

Middleware has been enhanced to log structured JSON telemetry events for every request. This allows us to track adoption and error rates for both routing strategies.

### Log Format
```json
{
  "event": "PHASE_1_ROUTING",
  "timestamp": "2024-03-20T10:00:00Z",
  "method": "GET",
  "path": "/dashboard/cases",
  "strategy": "MODERN_URL", // or "LEGACY_SUBDOMAIN"
  "tenantId": "demo-tenant",
  "subdomain": "N/A"
}
```

### Monitoring Strategy
- **Success Rate**: Track HTTP 200 vs 500 status codes grouped by `strategy`.
- **Latency**: Compare response times between `MODERN_URL` and `LEGACY_SUBDOMAIN`.
- **Adoption**: Monitor the ratio of requests using the new URL structure.

## 3. Success Metrics

Phase 1 will be considered successful when:
- [ ] **Parity Tests**: 100% Pass rate for critical paths.
- [ ] **Error Rate**: Modern route error rate <= Legacy route error rate.
- [ ] **Performance**: Modern route latency is within 5% of Legacy route.
- [ ] **Data Integrity**: No data leakage or cross-tenant contamination observed in logs.

## 4. Integration Points

The integration between the two systems is handled at the **Middleware** layer (`apps/web/src/middleware.ts`).
- **Legacy System**: Relies on `Host` header parsing to extract subdomain.
- **Modern System**: Relies on URL path parsing (`/:tenantId`).
- **Unified Context**: Both systems ultimately inject the same `x-tenant-id` header downstream.
    - **Server-Side**: Middleware extracts `tenantId` from URL or Host and injects header.
    - **Client-Side**: `api.ts` wrapper auto-detects `tenantId` from browser URL if not explicitly provided, ensuring client-side fetches maintain context.

## 5. Comparative Analysis Report (Template)

| Metric | Legacy (Header/Subdomain) | Modern (URL-based) | Delta |
|--------|---------------------------|--------------------|-------|
| **Avg Latency (p95)** | TBD | TBD | TBD |
| **Error Rate** | TBD | TBD | TBD |
| **Test Pass Rate** | TBD | TBD | TBD |
| **User Sessions** | TBD | TBD | TBD |

*Use this template to report weekly progress during the beta phase.*

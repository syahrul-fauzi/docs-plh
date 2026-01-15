# Tenant Architecture Migration Plan: Context-based to URL-based

## 1. Executive Summary
This document outlines the strategy to refactor the current Tenant Detection mechanism from a Header/Context-based approach to a robust URL-based pattern (`/:tenantId/dashboard`). This change aims to improve caching, SEO (if applicable), shareability, and performance.

## 2. Current Architecture
- **Detection**: `TenantLayout` reads `x-tenant-id` header or `tenantId` query param (fallback).
- **State**: `TenantProvider` (Context API) holds the `tenantId`.
- **Routing**: Routes are generally `/[locale]/(tenant)/...`.

## 3. Target Architecture
- **Routing**: `/[locale]/:tenantId/...`
- **Detection**: Dynamic route segment `[tenantId]` in Next.js App Router.
- **Data Fetching**: Per-request caching tagged with `tenantId`.

## 4. Migration Phases

### Phase 1: Route Structure Preparation (Week 1-2)
- [ ] Create a new route group `(app)/[tenantId]` to test the new structure in parallel.
- [ ] Implement middleware to redirect legacy routes to new URL pattern if detected.
- [ ] Update `navigation` utilities to include `tenantId` in all internal links.

### Phase 2: Component Refactoring (Week 3-4)
- [ ] Update `TenantProvider` to initialize from route params instead of headers.
- [ ] Refactor `Sidebar` and `Navbar` links to be tenant-aware.
- [ ] Ensure `CopilotWrapper` and other providers receive the `tenantId` from params.

### Phase 3: Data Layer Optimization (Month 2)
- [ ] Implement a Caching Layer using `unstable_cache` or Redis, keyed by `tenantId`.
- [ ] Optimize Prisma queries to ensure `where: { tenantId }` is enforcing index usage.

### Phase 4: Cutover & Cleanup (Month 2)
- [ ] Deploy new routes as primary.
- [ ] Monitor 404s and redirect loops.
- [ ] Deprecate and remove header-based detection logic.

## 5. Technical Considerations
- **Middleware**: Needs to validate `tenantId` existence to prevent access to invalid tenants.
- **SSO**: Update Clerk authentication callbacks to redirect to the correct tenant URL after login.
- **SEO**: Ensure `robots.txt` prevents indexing of sensitive tenant pages if necessary.

## 6. Success Metrics
- Page Load Time < 800ms (P95).
- Zero broken links during transition.
- 100% test coverage for new route handlers.

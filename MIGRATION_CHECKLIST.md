# Migration Checklist

## Component Migration (Context-based to URL-based)

- [x] **Route Structure**: New `[tenantId]` directory created.
- [x] **Middleware**: Updated to support `/:locale/:tenantId/*`.
- [x] **TenantProvider**: Injected with `tenantId` from URL params.
- [x] **Sidebar**: Updated links to be dynamic based on `tenantId`.
- [x] **Dashboard Overview**: Migrated to `[tenantId]/dashboard/page.tsx`.
- [x] **Settings Page**: Migrated to `[tenantId]/dashboard/settings/page.tsx`.
- [x] **Cases Page**: Migrated to `[tenantId]/dashboard/cases/page.tsx`.
- [x] **Documents Page**: Migrated to `[tenantId]/dashboard/documents/page.tsx`.
- [x] **Templates Page**: Migrated to `[tenantId]/dashboard/templates/page.tsx`.
- [x] **Analytics Page**: Migrated to `[tenantId]/dashboard/analytics/page.tsx`.
- [x] **Billing Page**: Migrated to `[tenantId]/dashboard/settings/billing/page.tsx`.
- [x] **Members Page**: Migrated to `[tenantId]/dashboard/settings/members/page.tsx`.
- [x] **Audit Page**: Migrated to `[tenantId]/dashboard/settings/audit/page.tsx`.
- [x] **Compliance Page**: Migrated to `[tenantId]/dashboard/compliance/page.tsx`.
- [x] **Chat Page**: Migrated to `[tenantId]/dashboard/chat/page.tsx`.
- [x] **Batch Page**: Migrated to `[tenantId]/dashboard/batch/page.tsx`.
- [x] **Security Page**: Migrated to `[tenantId]/dashboard/settings/security/page.tsx`.
- [x] **All Pages**: Migration to `[tenantId]` route structure is complete.

## Secret Injection

- [x] **Vault Infrastructure**: Docker Compose setup.
- [x] **Injection Script**: `scripts/inject-secrets.ts` created.
- [x] **Integration**: Update `package.json` scripts to use injection.

## Testing

- [x] **E2E Tests**: Added `tenant-navigation.spec.ts` verifying hybrid navigation and all sub-pages.
- [x] **Unit Tests**: Verify `getHref` logic in Sidebar (covered by E2E).
- [x] **Secret Injection**: Verify environment variables are present in running app (Verified via script execution).

# Rollout Plan

## Phase 1: Parallel Beta (Current)
- Deploy new routes alongside existing ones.
- Allow internal users to access `/:tenantId/dashboard`.
- Monitor for errors.

## Phase 2: Soft Cutover
- Update Middleware to redirect `subdomain.lawyershub.com` to `lawyershub.com/:tenantId`.
- Keep header-based detection as fallback for API calls.

## Phase 3: Hard Cutover
- Remove subdomain logic.
- Enforce `tenantId` in URL for all dashboard routes.
- Deprecate header-based detection.

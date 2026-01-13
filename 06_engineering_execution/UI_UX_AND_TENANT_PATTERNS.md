# Engineering Standards: Tenant Access & Responsive UI

## 1. Tenant Access Patterns

### 1.1 Multi-Tenant Isolation
Lawyers Hub implements a strict multi-tenant architecture using **Row Level Security (RLS)** at the database level and **Context-Aware Guards** at the API level.

### 1.2 Authentication Flow (AI Gateway & API)
- **Clerk SDK**: Used for JWT verification. Migrated from `@clerk/clerk-sdk-node` to `@clerk/express`.
- **Tenant Header**: All requests must include `X-Tenant-ID`.
- **Guard Enforcement**:
  - `AuthGuard` verifies the JWT `sub` and extracts `email`.
  - It cross-references the `X-Tenant-ID` header.
  - In Development mode, it supports simulation via `x-user-id` and `x-tenant-id` headers if `CLERK_SECRET_KEY` is missing.

### 1.3 Best Practices for Tenant Access
- **Never** hardcode tenant IDs.
- **Always** use the `request.user.tenantId` from the `AuthGuard` in service layers.
- **Verify** user-tenant relationship for critical operations.

---

## 2. Responsive UI Standards

### 2.1 Layout Overflow Prevention
To prevent layout breakage on mobile devices, especially when using fixed-size icons or buttons within flex containers:
- **Always** apply `shrink-0` to icons (Lucide, Heroicons).
- **Always** apply `shrink-0` to fixed-width badges and buttons.
- Use `flex-wrap` for container groups that may exceed screen width.

### 2.2 Standardized Rounding
Consistent visual language is achieved through standardized Tailwind rounding:
- **Small Elements**: `rounded-lg` or `rounded-xl`.
- **Cards/Containers/Modals**:
  - **Mobile**: `rounded-3xl` (`1.5rem`).
  - **Desktop (MD+)**: `rounded-[2.5rem]` (`2.5rem`).
- **Standardized Pattern**: `rounded-3xl md:rounded-[2.5rem]`.

### 2.3 Feature-Sliced Design (FSD) Compliance
- UI components related to specific business logic must reside in the `features` layer (e.g., `apps/web/src/features/cases/ui/`).
- Shared UI primitives must reside in `shared/ui`.

---

## 3. Development Workflow Checklist
1. [ ] Check `shrink-0` on all fixed-size elements in new UI components.
2. [ ] Apply `rounded-3xl md:rounded-[2.5rem]` to new cards/containers.
3. [ ] Ensure `X-Tenant-ID` is handled in new API endpoints.
4. [ ] Verify implementation with mobile viewport testing.

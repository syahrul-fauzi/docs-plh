[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserSelect

# Type Alias: UserSelect\<ExtArgs\>

> **UserSelect**\<`ExtArgs`\> = `$Extensions.GetSelect`\<\{ `_count?`: `boolean`
> \|
> [`UserCountOutputTypeDefaultArgs`](UserCountOutputTypeDefaultArgs.md)\<`ExtArgs`\>;
> `auditLogs?`: `boolean` \|
> [`User$auditLogsArgs`](User$auditLogsArgs.md)\<`ExtArgs`\>; `comments?`:
> `boolean` \| [`User$commentsArgs`](User$commentsArgs.md)\<`ExtArgs`\>;
> `complianceReviews?`: `boolean` \|
> [`User$complianceReviewsArgs`](User$complianceReviewsArgs.md)\<`ExtArgs`\>;
> `createdAt?`: `boolean`; `email?`: `boolean`; `fullName?`: `boolean`; `id?`:
> `boolean`; `piiAuditLogs?`: `boolean` \|
> [`User$piiAuditLogsArgs`](User$piiAuditLogsArgs.md)\<`ExtArgs`\>; `role?`:
> `boolean`; `templateVersions?`: `boolean` \|
> [`User$templateVersionsArgs`](User$templateVersionsArgs.md)\<`ExtArgs`\>;
> `tenant?`: `boolean` \|
> [`TenantDefaultArgs`](TenantDefaultArgs.md)\<`ExtArgs`\>; `tenantId?`:
> `boolean`; `updatedAt?`: `boolean`; \}, `ExtArgs`\[`"result"`\]\[`"user"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:4797

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

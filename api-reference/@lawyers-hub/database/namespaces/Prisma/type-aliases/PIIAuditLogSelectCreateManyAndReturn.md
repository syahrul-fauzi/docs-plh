[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogSelectCreateManyAndReturn

# Type Alias: PIIAuditLogSelectCreateManyAndReturn\<ExtArgs\>

> **PIIAuditLogSelectCreateManyAndReturn**\<`ExtArgs`\> = `$Extensions.GetSelect`\<\{ `actionType?`: `boolean`; `document?`: `boolean` \| [`PIIAuditLog$documentArgs`](PIIAuditLog$documentArgs.md)\<`ExtArgs`\>; `documentId?`: `boolean`; `id?`: `boolean`; `isMasked?`: `boolean`; `justification?`: `boolean`; `metadata?`: `boolean`; `piiType?`: `boolean`; `riskScore?`: `boolean`; `tenant?`: `boolean` \| [`TenantDefaultArgs`](TenantDefaultArgs.md)\<`ExtArgs`\>; `tenantId?`: `boolean`; `timestamp?`: `boolean`; `user?`: `boolean` \| [`UserDefaultArgs`](UserDefaultArgs.md)\<`ExtArgs`\>; `userId?`: `boolean`; \}, `ExtArgs`\[`"result"`\]\[`"pIIAuditLog"`\]\>

Defined in: node\_modules/.prisma/client/index.d.ts:17027

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

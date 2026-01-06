[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogWhereInput

# Type Alias: AuditLogWhereInput

> **AuditLogWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:18765

## Properties

### action?

> `optional` **action**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18770

***

### AND?

> `optional` **AND**: `AuditLogWhereInput` \| `AuditLogWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18766

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"AuditLog"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18776

***

### entityId?

> `optional` **entityId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"AuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18771

***

### entityType?

> `optional` **entityType**: [`StringNullableFilter`](StringNullableFilter.md)\<`"AuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18772

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18769

***

### metadata?

> `optional` **metadata**: [`JsonNullableFilter`](JsonNullableFilter.md)\<`"AuditLog"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:18775

***

### NOT?

> `optional` **NOT**: `AuditLogWhereInput` \| `AuditLogWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18768

***

### OR?

> `optional` **OR**: `AuditLogWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18767

***

### tenant?

> `optional` **tenant**: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18777

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18774

***

### user?

> `optional` **user**: [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md), [`UserWhereInput`](UserWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18778

***

### userId?

> `optional` **userId**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18773

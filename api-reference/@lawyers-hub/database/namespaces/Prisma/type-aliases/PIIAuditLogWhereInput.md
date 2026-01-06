[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogWhereInput

# Type Alias: PIIAuditLogWhereInput

> **PIIAuditLogWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:19307

## Properties

### actionType?

> `optional` **actionType**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19314

***

### AND?

> `optional` **AND**: `PIIAuditLogWhereInput` \| `PIIAuditLogWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:19308

***

### document?

> `optional` **document**: [`XOR`](XOR.md)\<[`DocumentNullableRelationFilter`](DocumentNullableRelationFilter.md), [`DocumentWhereInput`](DocumentWhereInput.md)\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:19322

***

### documentId?

> `optional` **documentId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:19319

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19311

***

### isMasked?

> `optional` **isMasked**: [`BoolFilter`](BoolFilter.md)\<`"PIIAuditLog"`\> \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:19316

***

### justification?

> `optional` **justification**: [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:19318

***

### metadata?

> `optional` **metadata**: [`JsonNullableFilter`](JsonNullableFilter.md)\<`"PIIAuditLog"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:19320

***

### NOT?

> `optional` **NOT**: `PIIAuditLogWhereInput` \| `PIIAuditLogWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:19310

***

### OR?

> `optional` **OR**: `PIIAuditLogWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:19309

***

### piiType?

> `optional` **piiType**: [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:19315

***

### riskScore?

> `optional` **riskScore**: [`IntFilter`](IntFilter.md)\<`"PIIAuditLog"`\> \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:19317

***

### tenant?

> `optional` **tenant**: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:19323

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19321

***

### timestamp?

> `optional` **timestamp**: [`DateTimeFilter`](DateTimeFilter.md)\<`"PIIAuditLog"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19312

***

### user?

> `optional` **user**: [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md), [`UserWhereInput`](UserWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:19324

***

### userId?

> `optional` **userId**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19313

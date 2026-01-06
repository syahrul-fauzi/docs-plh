[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogScalarWhereInput

# Type Alias: PIIAuditLogScalarWhereInput

> **PIIAuditLogScalarWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:23839

## Properties

### actionType?

> `optional` **actionType**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:23846

***

### AND?

> `optional` **AND**: `PIIAuditLogScalarWhereInput` \| `PIIAuditLogScalarWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:23840

***

### documentId?

> `optional` **documentId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:23851

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:23843

***

### isMasked?

> `optional` **isMasked**: [`BoolFilter`](BoolFilter.md)\<`"PIIAuditLog"`\> \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:23848

***

### justification?

> `optional` **justification**: [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:23850

***

### metadata?

> `optional` **metadata**: [`JsonNullableFilter`](JsonNullableFilter.md)\<`"PIIAuditLog"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:23852

***

### NOT?

> `optional` **NOT**: `PIIAuditLogScalarWhereInput` \| `PIIAuditLogScalarWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:23842

***

### OR?

> `optional` **OR**: `PIIAuditLogScalarWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:23841

***

### piiType?

> `optional` **piiType**: [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:23847

***

### riskScore?

> `optional` **riskScore**: [`IntFilter`](IntFilter.md)\<`"PIIAuditLog"`\> \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:23849

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:23853

***

### timestamp?

> `optional` **timestamp**: [`DateTimeFilter`](DateTimeFilter.md)\<`"PIIAuditLog"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:23844

***

### userId?

> `optional` **userId**: [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:23845

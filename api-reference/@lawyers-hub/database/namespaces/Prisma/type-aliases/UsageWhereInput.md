[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UsageWhereInput

# Type Alias: UsageWhereInput

> **UsageWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:18838

## Properties

### amount?

> `optional` **amount**: [`IntFilter`](IntFilter.md)\<`"Usage"`\> \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:18844

***

### AND?

> `optional` **AND**: `UsageWhereInput` \| `UsageWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18839

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Usage"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18847

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"Usage"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18842

***

### metadata?

> `optional` **metadata**: [`JsonNullableFilter`](JsonNullableFilter.md)\<`"Usage"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:18846

***

### NOT?

> `optional` **NOT**: `UsageWhereInput` \| `UsageWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18841

***

### OR?

> `optional` **OR**: `UsageWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18840

***

### tenant?

> `optional` **tenant**: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18848

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"Usage"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18845

***

### type?

> `optional` **type**: [`StringFilter`](StringFilter.md)\<`"Usage"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18843

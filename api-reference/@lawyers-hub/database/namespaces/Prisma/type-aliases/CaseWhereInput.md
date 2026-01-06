[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CaseWhereInput

# Type Alias: CaseWhereInput

> **CaseWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:18450

## Properties

### AND?

> `optional` **AND**: `CaseWhereInput` \| `CaseWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18451

***

### comments?

> `optional` **comments**: [`CommentListRelationFilter`](CommentListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18462

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Case"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18459

***

### description?

> `optional` **description**: [`StringNullableFilter`](StringNullableFilter.md)\<`"Case"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18456

***

### documents?

> `optional` **documents**: [`DocumentListRelationFilter`](DocumentListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18463

***

### drafts?

> `optional` **drafts**: [`DraftListRelationFilter`](DraftListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18464

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18454

***

### NOT?

> `optional` **NOT**: `CaseWhereInput` \| `CaseWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18453

***

### OR?

> `optional` **OR**: `CaseWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18452

***

### status?

> `optional` **status**: [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18457

***

### tenant?

> `optional` **tenant**: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18461

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18458

***

### title?

> `optional` **title**: [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18455

***

### updatedAt?

> `optional` **updatedAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Case"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18460

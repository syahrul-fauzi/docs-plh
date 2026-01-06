[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentWhereInput

# Type Alias: CommentWhereInput

> **CommentWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:18686

## Properties

### AND?

> `optional` **AND**: `CommentWhereInput` \| `CommentWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18687

***

### case?

> `optional` **case**: [`XOR`](XOR.md)\<[`CaseNullableRelationFilter`](CaseNullableRelationFilter.md), [`CaseWhereInput`](CaseWhereInput.md)\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18698

***

### caseId?

> `optional` **caseId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"Comment"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18694

***

### content?

> `optional` **content**: [`StringFilter`](StringFilter.md)\<`"Comment"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18691

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Comment"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18696

***

### draft?

> `optional` **draft**: [`XOR`](XOR.md)\<[`DraftNullableRelationFilter`](DraftNullableRelationFilter.md), [`DraftWhereInput`](DraftWhereInput.md)\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18699

***

### draftId?

> `optional` **draftId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"Comment"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18693

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"Comment"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18690

***

### NOT?

> `optional` **NOT**: `CommentWhereInput` \| `CommentWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18689

***

### OR?

> `optional` **OR**: `CommentWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18688

***

### tenant?

> `optional` **tenant**: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18700

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"Comment"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18695

***

### updatedAt?

> `optional` **updatedAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Comment"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18697

***

### user?

> `optional` **user**: [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md), [`UserWhereInput`](UserWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18701

***

### userId?

> `optional` **userId**: [`StringFilter`](StringFilter.md)\<`"Comment"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18692

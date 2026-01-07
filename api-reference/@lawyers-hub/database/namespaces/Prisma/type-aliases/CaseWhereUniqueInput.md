[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseWhereUniqueInput

# Type Alias: CaseWhereUniqueInput

> **CaseWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`CaseWhereInput`](CaseWhereInput.md) \|
> [`CaseWhereInput`](CaseWhereInput.md)[]; `comments?`:
> [`CommentListRelationFilter`](CommentListRelationFilter.md); `createdAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"Case"`\> \| `Date` \| `string`;
> `description?`: [`StringNullableFilter`](StringNullableFilter.md)\<`"Case"`\>
> \| `string` \| `null`; `documents?`:
> [`DocumentListRelationFilter`](DocumentListRelationFilter.md); `drafts?`:
> [`DraftListRelationFilter`](DraftListRelationFilter.md); `id?`: `string`;
> `NOT?`: [`CaseWhereInput`](CaseWhereInput.md) \|
> [`CaseWhereInput`](CaseWhereInput.md)[]; `OR?`:
> [`CaseWhereInput`](CaseWhereInput.md)[]; `status?`:
> [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`; `tenant?`:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`:
> [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`; `title?`:
> [`StringFilter`](StringFilter.md)\<`"Case"`\> \| `string`; `updatedAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"Case"`\> \| `Date` \| `string`; \},
> `"id"`\>

Defined in: node_modules/.prisma/client/index.d.ts:18481

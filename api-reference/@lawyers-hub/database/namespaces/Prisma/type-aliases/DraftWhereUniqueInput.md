[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DraftWhereUniqueInput

# Type Alias: DraftWhereUniqueInput

> **DraftWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`DraftWhereInput`](DraftWhereInput.md) \|
> [`DraftWhereInput`](DraftWhereInput.md)[]; `case?`:
> [`XOR`](XOR.md)\<[`CaseNullableRelationFilter`](CaseNullableRelationFilter.md),
> [`CaseWhereInput`](CaseWhereInput.md)\> \| `null`; `caseId?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"Draft"`\> \| `string` \|
> `null`; `comments?`:
> [`CommentListRelationFilter`](CommentListRelationFilter.md); `content?`:
> [`StringFilter`](StringFilter.md)\<`"Draft"`\> \| `string`; `createdAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"Draft"`\> \| `Date` \| `string`;
> `id?`: `string`; `metadata?`:
> [`JsonNullableFilter`](JsonNullableFilter.md)\<`"Draft"`\>; `NOT?`:
> [`DraftWhereInput`](DraftWhereInput.md) \|
> [`DraftWhereInput`](DraftWhereInput.md)[]; `OR?`:
> [`DraftWhereInput`](DraftWhereInput.md)[]; `status?`:
> [`StringFilter`](StringFilter.md)\<`"Draft"`\> \| `string`; `templateType?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"Draft"`\> \| `string` \|
> `null`; `tenant?`:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`:
> [`StringFilter`](StringFilter.md)\<`"Draft"`\> \| `string`; `title?`:
> [`StringFilter`](StringFilter.md)\<`"Draft"`\> \| `string`; `updatedAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"Draft"`\> \| `Date` \| `string`; \},
> `"id"`\>

Defined in: node_modules/.prisma/client/index.d.ts:18635

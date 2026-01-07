[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CommentWhereUniqueInput

# Type Alias: CommentWhereUniqueInput

> **CommentWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`CommentWhereInput`](CommentWhereInput.md) \|
> [`CommentWhereInput`](CommentWhereInput.md)[]; `case?`:
> [`XOR`](XOR.md)\<[`CaseNullableRelationFilter`](CaseNullableRelationFilter.md),
> [`CaseWhereInput`](CaseWhereInput.md)\> \| `null`; `caseId?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"Comment"`\> \| `string`
> \| `null`; `content?`: [`StringFilter`](StringFilter.md)\<`"Comment"`\> \|
> `string`; `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Comment"`\>
> \| `Date` \| `string`; `draft?`:
> [`XOR`](XOR.md)\<[`DraftNullableRelationFilter`](DraftNullableRelationFilter.md),
> [`DraftWhereInput`](DraftWhereInput.md)\> \| `null`; `draftId?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"Comment"`\> \| `string`
> \| `null`; `id?`: `string`; `NOT?`:
> [`CommentWhereInput`](CommentWhereInput.md) \|
> [`CommentWhereInput`](CommentWhereInput.md)[]; `OR?`:
> [`CommentWhereInput`](CommentWhereInput.md)[]; `tenant?`:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`:
> [`StringFilter`](StringFilter.md)\<`"Comment"`\> \| `string`; `updatedAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"Comment"`\> \| `Date` \| `string`;
> `user?`: [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md),
> [`UserWhereInput`](UserWhereInput.md)\>; `userId?`:
> [`StringFilter`](StringFilter.md)\<`"Comment"`\> \| `string`; \}, `"id"`\>

Defined in: node_modules/.prisma/client/index.d.ts:18719

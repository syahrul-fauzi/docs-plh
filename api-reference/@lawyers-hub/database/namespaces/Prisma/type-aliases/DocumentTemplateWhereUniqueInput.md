[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentTemplateWhereUniqueInput

# Type Alias: DocumentTemplateWhereUniqueInput

> **DocumentTemplateWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md) \|
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)[]; `category?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"DocumentTemplate"`\> \|
> `string` \| `null`; `content?`:
> [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\> \| `string`;
> `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"DocumentTemplate"`\> \|
> `Date` \| `string`; `id?`: `string`; `name?`:
> [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\> \| `string`; `NOT?`:
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md) \|
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)[]; `OR?`:
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)[]; `tenant?`:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`:
> [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\> \| `string`;
> `updatedAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"DocumentTemplate"`\> \|
> `Date` \| `string`; `versions?`:
> [`TemplateVersionListRelationFilter`](TemplateVersionListRelationFilter.md);
> \}, `"id"`\>

Defined in: node_modules/.prisma/client/index.d.ts:19002

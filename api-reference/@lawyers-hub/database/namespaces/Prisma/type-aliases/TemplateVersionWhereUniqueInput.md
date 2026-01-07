[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TemplateVersionWhereUniqueInput

# Type Alias: TemplateVersionWhereUniqueInput

> **TemplateVersionWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md) \|
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md)[]; `changeLog?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"TemplateVersion"`\> \|
> `string` \| `null`; `content?`:
> [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \| `string`;
> `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"TemplateVersion"`\> \|
> `Date` \| `string`; `id?`: `string`; `NOT?`:
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md) \|
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md)[]; `OR?`:
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md)[]; `template?`:
> [`XOR`](XOR.md)\<[`DocumentTemplateRelationFilter`](DocumentTemplateRelationFilter.md),
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)\>;
> `templateId?`: [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \|
> `string`; `user?`:
> [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md),
> [`UserWhereInput`](UserWhereInput.md)\>; `userId?`:
> [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \| `string`;
> `version?`: [`IntFilter`](IntFilter.md)\<`"TemplateVersion"`\> \| `number`;
> \}, `"id"`\>

Defined in: node_modules/.prisma/client/index.d.ts:19070

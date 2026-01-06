[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TemplateVersionWhereInput

# Type Alias: TemplateVersionWhereInput

> **TemplateVersionWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:19043

## Properties

### AND?

> `optional` **AND**: `TemplateVersionWhereInput` \| `TemplateVersionWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:19044

***

### changeLog?

> `optional` **changeLog**: [`StringNullableFilter`](StringNullableFilter.md)\<`"TemplateVersion"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:19051

***

### content?

> `optional` **content**: [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19049

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"TemplateVersion"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19053

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19047

***

### NOT?

> `optional` **NOT**: `TemplateVersionWhereInput` \| `TemplateVersionWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:19046

***

### OR?

> `optional` **OR**: `TemplateVersionWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:19045

***

### template?

> `optional` **template**: [`XOR`](XOR.md)\<[`DocumentTemplateRelationFilter`](DocumentTemplateRelationFilter.md), [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:19054

***

### templateId?

> `optional` **templateId**: [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19048

***

### user?

> `optional` **user**: [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md), [`UserWhereInput`](UserWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:19055

***

### userId?

> `optional` **userId**: [`StringFilter`](StringFilter.md)\<`"TemplateVersion"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19052

***

### version?

> `optional` **version**: [`IntFilter`](IntFilter.md)\<`"TemplateVersion"`\> \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:19050

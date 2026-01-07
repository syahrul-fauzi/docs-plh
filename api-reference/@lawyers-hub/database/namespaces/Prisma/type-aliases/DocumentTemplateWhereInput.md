[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentTemplateWhereInput

# Type Alias: DocumentTemplateWhereInput

> **DocumentTemplateWhereInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:18975

## Properties

### AND?

> `optional` **AND**: `DocumentTemplateWhereInput` \|
> `DocumentTemplateWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:18976

---

### category?

> `optional` **category**:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"DocumentTemplate"`\> \|
> `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:18982

---

### content?

> `optional` **content**:
> [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18981

---

### createdAt?

> `optional` **createdAt**:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"DocumentTemplate"`\> \| `Date` \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:18984

---

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18979

---

### name?

> `optional` **name**: [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18980

---

### NOT?

> `optional` **NOT**: `DocumentTemplateWhereInput` \|
> `DocumentTemplateWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:18978

---

### OR?

> `optional` **OR**: `DocumentTemplateWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:18977

---

### tenant?

> `optional` **tenant**:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:18986

---

### tenantId?

> `optional` **tenantId**:
> [`StringFilter`](StringFilter.md)\<`"DocumentTemplate"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18983

---

### updatedAt?

> `optional` **updatedAt**:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"DocumentTemplate"`\> \| `Date` \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:18985

---

### versions?

> `optional` **versions**:
> [`TemplateVersionListRelationFilter`](TemplateVersionListRelationFilter.md)

Defined in: node_modules/.prisma/client/index.d.ts:18987

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseCreateWithoutCommentsInput

# Type Alias: CaseCreateWithoutCommentsInput

> **CaseCreateWithoutCommentsInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:25059

## Properties

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25064

---

### description?

> `optional` **description**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:25062

---

### documents?

> `optional` **documents**:
> [`DocumentCreateNestedManyWithoutCaseInput`](DocumentCreateNestedManyWithoutCaseInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25067

---

### drafts?

> `optional` **drafts**:
> [`DraftCreateNestedManyWithoutCaseInput`](DraftCreateNestedManyWithoutCaseInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25068

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25060

---

### status?

> `optional` **status**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25063

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutCasesInput`](TenantCreateNestedOneWithoutCasesInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25066

---

### title

> **title**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25061

---

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25065

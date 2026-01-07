[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AuditLogScalarWhereInput

# Type Alias: AuditLogScalarWhereInput

> **AuditLogScalarWhereInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:23592

## Properties

### action?

> `optional` **action**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:23597

---

### AND?

> `optional` **AND**: `AuditLogScalarWhereInput` \| `AuditLogScalarWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:23593

---

### createdAt?

> `optional` **createdAt**:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"AuditLog"`\> \| `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:23603

---

### entityId?

> `optional` **entityId**:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"AuditLog"`\> \| `string`
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:23598

---

### entityType?

> `optional` **entityType**:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"AuditLog"`\> \| `string`
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:23599

---

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:23596

---

### metadata?

> `optional` **metadata**:
> [`JsonNullableFilter`](JsonNullableFilter.md)\<`"AuditLog"`\>

Defined in: node_modules/.prisma/client/index.d.ts:23602

---

### NOT?

> `optional` **NOT**: `AuditLogScalarWhereInput` \| `AuditLogScalarWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:23595

---

### OR?

> `optional` **OR**: `AuditLogScalarWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:23594

---

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:23601

---

### userId?

> `optional` **userId**: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:23600

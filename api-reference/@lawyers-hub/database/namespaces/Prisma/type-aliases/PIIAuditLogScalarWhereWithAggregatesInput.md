[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogScalarWhereWithAggregatesInput

# Type Alias: PIIAuditLogScalarWhereWithAggregatesInput

> **PIIAuditLogScalarWhereWithAggregatesInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:19383

## Properties

### actionType?

> `optional` **actionType**:
> [`StringWithAggregatesFilter`](StringWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19390

---

### AND?

> `optional` **AND**: `PIIAuditLogScalarWhereWithAggregatesInput` \|
> `PIIAuditLogScalarWhereWithAggregatesInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:19384

---

### documentId?

> `optional` **documentId**:
> [`StringNullableWithAggregatesFilter`](StringNullableWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:19395

---

### id?

> `optional` **id**:
> [`StringWithAggregatesFilter`](StringWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19387

---

### isMasked?

> `optional` **isMasked**:
> [`BoolWithAggregatesFilter`](BoolWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:19392

---

### justification?

> `optional` **justification**:
> [`StringNullableWithAggregatesFilter`](StringNullableWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:19394

---

### metadata?

> `optional` **metadata**:
> [`JsonNullableWithAggregatesFilter`](JsonNullableWithAggregatesFilter.md)\<`"PIIAuditLog"`\>

Defined in: node_modules/.prisma/client/index.d.ts:19396

---

### NOT?

> `optional` **NOT**: `PIIAuditLogScalarWhereWithAggregatesInput` \|
> `PIIAuditLogScalarWhereWithAggregatesInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:19386

---

### OR?

> `optional` **OR**: `PIIAuditLogScalarWhereWithAggregatesInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:19385

---

### piiType?

> `optional` **piiType**:
> [`StringNullableWithAggregatesFilter`](StringNullableWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:19391

---

### riskScore?

> `optional` **riskScore**:
> [`IntWithAggregatesFilter`](IntWithAggregatesFilter.md)\<`"PIIAuditLog"`\> \|
> `number`

Defined in: node_modules/.prisma/client/index.d.ts:19393

---

### tenantId?

> `optional` **tenantId**:
> [`StringWithAggregatesFilter`](StringWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19397

---

### timestamp?

> `optional` **timestamp**:
> [`DateTimeWithAggregatesFilter`](DateTimeWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19388

---

### userId?

> `optional` **userId**:
> [`StringWithAggregatesFilter`](StringWithAggregatesFilter.md)\<`"PIIAuditLog"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19389

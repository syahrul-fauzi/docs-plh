[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
ComplianceReviewWhereInput

# Type Alias: ComplianceReviewWhereInput

> **ComplianceReviewWhereInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:19202

## Properties

### AND?

> `optional` **AND**: `ComplianceReviewWhereInput` \|
> `ComplianceReviewWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:19203

---

### confidenceScore?

> `optional` **confidenceScore**:
> [`FloatFilter`](FloatFilter.md)\<`"ComplianceReview"`\> \| `number`

Defined in: node_modules/.prisma/client/index.d.ts:19214

---

### correctedValue?

> `optional` **correctedValue**:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"ComplianceReview"`\> \|
> `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:19213

---

### createdAt?

> `optional` **createdAt**:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"ComplianceReview"`\> \| `Date` \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:19218

---

### entityId?

> `optional` **entityId**:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"ComplianceReview"`\> \|
> `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:19209

---

### entityType?

> `optional` **entityType**:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"ComplianceReview"`\> \|
> `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:19210

---

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"ComplianceReview"`\>
> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19206

---

### isProcessed?

> `optional` **isProcessed**:
> [`BoolFilter`](BoolFilter.md)\<`"ComplianceReview"`\> \| `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:19216

---

### metadata?

> `optional` **metadata**:
> [`JsonNullableFilter`](JsonNullableFilter.md)\<`"ComplianceReview"`\>

Defined in: node_modules/.prisma/client/index.d.ts:19217

---

### NOT?

> `optional` **NOT**: `ComplianceReviewWhereInput` \|
> `ComplianceReviewWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:19205

---

### OR?

> `optional` **OR**: `ComplianceReviewWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:19204

---

### originalValue?

> `optional` **originalValue**:
> [`StringFilter`](StringFilter.md)\<`"ComplianceReview"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19212

---

### piiType?

> `optional` **piiType**:
> [`StringFilter`](StringFilter.md)\<`"ComplianceReview"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19211

---

### reviewer?

> `optional` **reviewer**:
> [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md),
> [`UserWhereInput`](UserWhereInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:19220

---

### reviewerId?

> `optional` **reviewerId**:
> [`StringFilter`](StringFilter.md)\<`"ComplianceReview"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19208

---

### status?

> `optional` **status**:
> [`StringFilter`](StringFilter.md)\<`"ComplianceReview"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19215

---

### tenant?

> `optional` **tenant**:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:19221

---

### tenantId?

> `optional` **tenantId**:
> [`StringFilter`](StringFilter.md)\<`"ComplianceReview"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:19207

---

### updatedAt?

> `optional` **updatedAt**:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"ComplianceReview"`\> \| `Date` \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:19219

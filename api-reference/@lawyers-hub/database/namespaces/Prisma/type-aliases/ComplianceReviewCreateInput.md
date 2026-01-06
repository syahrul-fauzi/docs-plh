[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewCreateInput

# Type Alias: ComplianceReviewCreateInput

> **ComplianceReviewCreateInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:20482

## Properties

### confidenceScore

> **confidenceScore**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:20489

***

### correctedValue?

> `optional` **correctedValue**: `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20488

***

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20493

***

### entityId?

> `optional` **entityId**: `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20484

***

### entityType?

> `optional` **entityType**: `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20485

***

### id?

> `optional` **id**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20483

***

### isProcessed?

> `optional` **isProcessed**: `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:20491

***

### metadata?

> `optional` **metadata**: [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \| [`InputJsonValue`](InputJsonValue.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20492

***

### originalValue

> **originalValue**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20487

***

### piiType

> **piiType**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20486

***

### reviewer

> **reviewer**: [`UserCreateNestedOneWithoutComplianceReviewsInput`](UserCreateNestedOneWithoutComplianceReviewsInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20495

***

### status

> **status**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20490

***

### tenant

> **tenant**: [`TenantCreateNestedOneWithoutComplianceReviewsInput`](TenantCreateNestedOneWithoutComplianceReviewsInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20496

***

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20494

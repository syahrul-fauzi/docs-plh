[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewUpdateInput

# Type Alias: ComplianceReviewUpdateInput

> **ComplianceReviewUpdateInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:20516

## Properties

### confidenceScore?

> `optional` **confidenceScore**: [`FloatFieldUpdateOperationsInput`](FloatFieldUpdateOperationsInput.md) \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:20523

***

### correctedValue?

> `optional` **correctedValue**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20522

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md) \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20527

***

### entityId?

> `optional` **entityId**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20518

***

### entityType?

> `optional` **entityType**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20519

***

### id?

> `optional` **id**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20517

***

### isProcessed?

> `optional` **isProcessed**: [`BoolFieldUpdateOperationsInput`](BoolFieldUpdateOperationsInput.md) \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:20525

***

### metadata?

> `optional` **metadata**: [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \| [`InputJsonValue`](InputJsonValue.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20526

***

### originalValue?

> `optional` **originalValue**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20521

***

### piiType?

> `optional` **piiType**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20520

***

### reviewer?

> `optional` **reviewer**: [`UserUpdateOneRequiredWithoutComplianceReviewsNestedInput`](UserUpdateOneRequiredWithoutComplianceReviewsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20529

***

### status?

> `optional` **status**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20524

***

### tenant?

> `optional` **tenant**: [`TenantUpdateOneRequiredWithoutComplianceReviewsNestedInput`](TenantUpdateOneRequiredWithoutComplianceReviewsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20530

***

### updatedAt?

> `optional` **updatedAt**: [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md) \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20528

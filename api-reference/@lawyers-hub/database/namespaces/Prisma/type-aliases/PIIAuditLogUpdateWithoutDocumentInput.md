[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogUpdateWithoutDocumentInput

# Type Alias: PIIAuditLogUpdateWithoutDocumentInput

> **PIIAuditLogUpdateWithoutDocumentInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:27250

## Properties

### actionType?

> `optional` **actionType**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:27253

***

### id?

> `optional` **id**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:27251

***

### isMasked?

> `optional` **isMasked**: [`BoolFieldUpdateOperationsInput`](BoolFieldUpdateOperationsInput.md) \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:27255

***

### justification?

> `optional` **justification**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:27257

***

### metadata?

> `optional` **metadata**: [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \| [`InputJsonValue`](InputJsonValue.md)

Defined in: node\_modules/.prisma/client/index.d.ts:27258

***

### piiType?

> `optional` **piiType**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:27254

***

### riskScore?

> `optional` **riskScore**: [`IntFieldUpdateOperationsInput`](IntFieldUpdateOperationsInput.md) \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:27256

***

### tenant?

> `optional` **tenant**: [`TenantUpdateOneRequiredWithoutPiiAuditLogsNestedInput`](TenantUpdateOneRequiredWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:27259

***

### timestamp?

> `optional` **timestamp**: [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md) \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:27252

***

### user?

> `optional` **user**: [`UserUpdateOneRequiredWithoutPiiAuditLogsNestedInput`](UserUpdateOneRequiredWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:27260

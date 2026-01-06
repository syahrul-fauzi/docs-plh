[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogUpdateInput

# Type Alias: PIIAuditLogUpdateInput

> **PIIAuditLogUpdateInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:20627

## Properties

### actionType?

> `optional` **actionType**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20630

***

### document?

> `optional` **document**: [`DocumentUpdateOneWithoutPiiAuditLogsNestedInput`](DocumentUpdateOneWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20636

***

### id?

> `optional` **id**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20628

***

### isMasked?

> `optional` **isMasked**: [`BoolFieldUpdateOperationsInput`](BoolFieldUpdateOperationsInput.md) \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:20632

***

### justification?

> `optional` **justification**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20634

***

### metadata?

> `optional` **metadata**: [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \| [`InputJsonValue`](InputJsonValue.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20635

***

### piiType?

> `optional` **piiType**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:20631

***

### riskScore?

> `optional` **riskScore**: [`IntFieldUpdateOperationsInput`](IntFieldUpdateOperationsInput.md) \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:20633

***

### tenant?

> `optional` **tenant**: [`TenantUpdateOneRequiredWithoutPiiAuditLogsNestedInput`](TenantUpdateOneRequiredWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20637

***

### timestamp?

> `optional` **timestamp**: [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md) \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:20629

***

### user?

> `optional` **user**: [`UserUpdateOneRequiredWithoutPiiAuditLogsNestedInput`](UserUpdateOneRequiredWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:20638

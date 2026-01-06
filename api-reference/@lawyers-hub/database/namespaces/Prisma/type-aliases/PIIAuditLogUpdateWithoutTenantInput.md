[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogUpdateWithoutTenantInput

# Type Alias: PIIAuditLogUpdateWithoutTenantInput

> **PIIAuditLogUpdateWithoutTenantInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:26773

## Properties

### actionType?

> `optional` **actionType**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:26776

***

### document?

> `optional` **document**: [`DocumentUpdateOneWithoutPiiAuditLogsNestedInput`](DocumentUpdateOneWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:26782

***

### id?

> `optional` **id**: [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:26774

***

### isMasked?

> `optional` **isMasked**: [`BoolFieldUpdateOperationsInput`](BoolFieldUpdateOperationsInput.md) \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:26778

***

### justification?

> `optional` **justification**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:26780

***

### metadata?

> `optional` **metadata**: [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \| [`InputJsonValue`](InputJsonValue.md)

Defined in: node\_modules/.prisma/client/index.d.ts:26781

***

### piiType?

> `optional` **piiType**: [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md) \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:26777

***

### riskScore?

> `optional` **riskScore**: [`IntFieldUpdateOperationsInput`](IntFieldUpdateOperationsInput.md) \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:26779

***

### timestamp?

> `optional` **timestamp**: [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md) \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:26775

***

### user?

> `optional` **user**: [`UserUpdateOneRequiredWithoutPiiAuditLogsNestedInput`](UserUpdateOneRequiredWithoutPiiAuditLogsNestedInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:26783

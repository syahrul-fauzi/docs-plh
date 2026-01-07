[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogUpdateWithoutUserInput

# Type Alias: PIIAuditLogUpdateWithoutUserInput

> **PIIAuditLogUpdateWithoutUserInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:27039

## Properties

### actionType?

> `optional` **actionType**:
> [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:27042

---

### document?

> `optional` **document**:
> [`DocumentUpdateOneWithoutPiiAuditLogsNestedInput`](DocumentUpdateOneWithoutPiiAuditLogsNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:27048

---

### id?

> `optional` **id**:
> [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:27040

---

### isMasked?

> `optional` **isMasked**:
> [`BoolFieldUpdateOperationsInput`](BoolFieldUpdateOperationsInput.md) \|
> `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:27044

---

### justification?

> `optional` **justification**:
> [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md)
> \| `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:27046

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:27047

---

### piiType?

> `optional` **piiType**:
> [`NullableStringFieldUpdateOperationsInput`](NullableStringFieldUpdateOperationsInput.md)
> \| `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:27043

---

### riskScore?

> `optional` **riskScore**:
> [`IntFieldUpdateOperationsInput`](IntFieldUpdateOperationsInput.md) \|
> `number`

Defined in: node_modules/.prisma/client/index.d.ts:27045

---

### tenant?

> `optional` **tenant**:
> [`TenantUpdateOneRequiredWithoutPiiAuditLogsNestedInput`](TenantUpdateOneRequiredWithoutPiiAuditLogsNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:27049

---

### timestamp?

> `optional` **timestamp**:
> [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md)
> \| `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:27041

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogCreateWithoutUserInput

# Type Alias: PIIAuditLogCreateWithoutUserInput

> **PIIAuditLogCreateWithoutUserInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:24146

## Properties

### actionType

> **actionType**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:24149

---

### document?

> `optional` **document**:
> [`DocumentCreateNestedOneWithoutPiiAuditLogsInput`](DocumentCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:24155

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:24147

---

### isMasked?

> `optional` **isMasked**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:24151

---

### justification?

> `optional` **justification**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:24153

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:24154

---

### piiType?

> `optional` **piiType**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:24150

---

### riskScore?

> `optional` **riskScore**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:24152

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutPiiAuditLogsInput`](TenantCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:24156

---

### timestamp?

> `optional` **timestamp**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:24148

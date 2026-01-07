[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogCreateWithoutDocumentInput

# Type Alias: PIIAuditLogCreateWithoutDocumentInput

> **PIIAuditLogCreateWithoutDocumentInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:24715

## Properties

### actionType

> **actionType**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:24718

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:24716

---

### isMasked?

> `optional` **isMasked**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:24720

---

### justification?

> `optional` **justification**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:24722

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:24723

---

### piiType?

> `optional` **piiType**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:24719

---

### riskScore?

> `optional` **riskScore**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:24721

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutPiiAuditLogsInput`](TenantCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:24724

---

### timestamp?

> `optional` **timestamp**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:24717

---

### user

> **user**:
> [`UserCreateNestedOneWithoutPiiAuditLogsInput`](UserCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:24725

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogCreateWithoutTenantInput

# Type Alias: PIIAuditLogCreateWithoutTenantInput

> **PIIAuditLogCreateWithoutTenantInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:23447

## Properties

### actionType

> **actionType**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:23450

---

### document?

> `optional` **document**:
> [`DocumentCreateNestedOneWithoutPiiAuditLogsInput`](DocumentCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:23456

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:23448

---

### isMasked?

> `optional` **isMasked**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:23452

---

### justification?

> `optional` **justification**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:23454

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:23455

---

### piiType?

> `optional` **piiType**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:23451

---

### riskScore?

> `optional` **riskScore**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:23453

---

### timestamp?

> `optional` **timestamp**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:23449

---

### user

> **user**:
> [`UserCreateNestedOneWithoutPiiAuditLogsInput`](UserCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:23457

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogCreateInput

# Type Alias: PIIAuditLogCreateInput

> **PIIAuditLogCreateInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:20599

## Properties

### actionType

> **actionType**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:20602

---

### document?

> `optional` **document**:
> [`DocumentCreateNestedOneWithoutPiiAuditLogsInput`](DocumentCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:20608

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:20600

---

### isMasked?

> `optional` **isMasked**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:20604

---

### justification?

> `optional` **justification**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:20606

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:20607

---

### piiType?

> `optional` **piiType**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:20603

---

### riskScore?

> `optional` **riskScore**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:20605

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutPiiAuditLogsInput`](TenantCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:20609

---

### timestamp?

> `optional` **timestamp**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:20601

---

### user

> **user**:
> [`UserCreateNestedOneWithoutPiiAuditLogsInput`](UserCreateNestedOneWithoutPiiAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:20610

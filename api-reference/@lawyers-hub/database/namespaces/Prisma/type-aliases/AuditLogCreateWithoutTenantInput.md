[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AuditLogCreateWithoutTenantInput

# Type Alias: AuditLogCreateWithoutTenantInput

> **AuditLogCreateWithoutTenantInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:23181

## Properties

### action

> **action**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:23183

---

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:23187

---

### entityId?

> `optional` **entityId**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:23184

---

### entityType?

> `optional` **entityType**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:23185

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:23182

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:23186

---

### user

> **user**:
> [`UserCreateNestedOneWithoutAuditLogsInput`](UserCreateNestedOneWithoutAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:23188

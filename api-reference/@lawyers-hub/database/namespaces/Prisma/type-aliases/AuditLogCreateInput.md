[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AuditLogCreateInput

# Type Alias: AuditLogCreateInput

> **AuditLogCreateInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:20016

## Properties

### action

> **action**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:20018

---

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:20022

---

### entityId?

> `optional` **entityId**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:20019

---

### entityType?

> `optional` **entityType**: `string` \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:20020

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:20017

---

### metadata?

> `optional` **metadata**:
> [`NullableJsonNullValueInput`](NullableJsonNullValueInput.md) \|
> [`InputJsonValue`](InputJsonValue.md)

Defined in: node_modules/.prisma/client/index.d.ts:20021

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutAuditLogsInput`](TenantCreateNestedOneWithoutAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:20023

---

### user

> **user**:
> [`UserCreateNestedOneWithoutAuditLogsInput`](UserCreateNestedOneWithoutAuditLogsInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:20024

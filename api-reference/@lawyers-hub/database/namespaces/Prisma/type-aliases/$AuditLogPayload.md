[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$AuditLogPayload

# Type Alias: $AuditLogPayload\<ExtArgs\>

> **$AuditLogPayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:10025

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:10041

---

### name

> **name**: `"AuditLog"`

Defined in: node_modules/.prisma/client/index.d.ts:10026

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:10027

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

#### user

> **user**: [`$UserPayload`]($UserPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `action`: `string`;
> `createdAt`: `Date`; `entityId`: `string` \| `null`; `entityType`: `string` \|
> `null`; `id`: `string`; `metadata`: [`JsonValue`](JsonValue.md) \| `null`;
> `tenantId`: `string`; `userId`: `string`; \},
> `ExtArgs`\[`"result"`\]\[`"auditLog"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:10031

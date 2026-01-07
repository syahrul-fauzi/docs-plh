[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$PIIAuditLogPayload

# Type Alias: $PIIAuditLogPayload\<ExtArgs\>

> **$PIIAuditLogPayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17069

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:17089

---

### name

> **name**: `"PIIAuditLog"`

Defined in: node_modules/.prisma/client/index.d.ts:17070

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:17071

#### document

> **document**: [`$DocumentPayload`]($DocumentPayload.md)\<`ExtArgs`\> \| `null`

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

#### user

> **user**: [`$UserPayload`]($UserPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `actionType`: `string`;
> `documentId`: `string` \| `null`; `id`: `string`; `isMasked`: `boolean`;
> `justification`: `string` \| `null`; `metadata`: [`JsonValue`](JsonValue.md)
> \| `null`; `piiType`: `string` \| `null`; `riskScore`: `number`; `tenantId`:
> `string`; `timestamp`: `Date`; `userId`: `string`; \},
> `ExtArgs`\[`"result"`\]\[`"pIIAuditLog"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:17076

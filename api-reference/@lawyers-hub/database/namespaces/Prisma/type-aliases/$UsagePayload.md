[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$UsagePayload

# Type Alias: $UsagePayload\<ExtArgs\>

> **$UsagePayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:11006

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:11019

---

### name

> **name**: `"Usage"`

Defined in: node_modules/.prisma/client/index.d.ts:11007

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:11008

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `amount`: `number`;
> `createdAt`: `Date`; `id`: `string`; `metadata`: [`JsonValue`](JsonValue.md)
> \| `null`; `tenantId`: `string`; `type`: `string`; \},
> `ExtArgs`\[`"result"`\]\[`"usage"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:11011

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$InvitationPayload

# Type Alias: $InvitationPayload\<ExtArgs\>

> **$InvitationPayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:11981

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:11997

---

### name

> **name**: `"Invitation"`

Defined in: node_modules/.prisma/client/index.d.ts:11982

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:11983

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `createdAt`: `Date`; `email`:
> `string`; `expiresAt`: `Date`; `id`: `string`; `role`: `string`; `status`:
> `string`; `tenantId`: `string`; `token`: `string`; `updatedAt`: `Date`; \},
> `ExtArgs`\[`"result"`\]\[`"invitation"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:11986

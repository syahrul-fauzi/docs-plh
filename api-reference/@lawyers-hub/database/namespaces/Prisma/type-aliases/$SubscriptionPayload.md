[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$SubscriptionPayload

# Type Alias: $SubscriptionPayload\<ExtArgs\>

> **$SubscriptionPayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3873

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:3890

---

### name

> **name**: `"Subscription"`

Defined in: node_modules/.prisma/client/index.d.ts:3874

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:3875

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `createdAt`: `Date`;
> `currentPeriodEnd`: `Date` \| `null`; `id`: `string`; `plan`: `string`;
> `quantity`: `number`; `status`: `string`; `stripeCustomerId`: `string` \|
> `null`; `stripePriceId`: `string` \| `null`; `tenantId`: `string`;
> `updatedAt`: `Date`; \}, `ExtArgs`\[`"result"`\]\[`"subscription"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:3878

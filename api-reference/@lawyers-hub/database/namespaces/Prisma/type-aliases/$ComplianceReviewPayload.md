[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$ComplianceReviewPayload

# Type Alias: $ComplianceReviewPayload\<ExtArgs\>

> **$ComplianceReviewPayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:16018

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:16040

---

### name

> **name**: `"ComplianceReview"`

Defined in: node_modules/.prisma/client/index.d.ts:16019

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:16020

#### reviewer

> **reviewer**: [`$UserPayload`]($UserPayload.md)\<`ExtArgs`\>

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `confidenceScore`: `number`;
> `correctedValue`: `string` \| `null`; `createdAt`: `Date`; `entityId`:
> `string` \| `null`; `entityType`: `string` \| `null`; `id`: `string`;
> `isProcessed`: `boolean`; `metadata`: [`JsonValue`](JsonValue.md) \| `null`;
> `originalValue`: `string`; `piiType`: `string`; `reviewerId`: `string`;
> `status`: `string`; `tenantId`: `string`; `updatedAt`: `Date`; \},
> `ExtArgs`\[`"result"`\]\[`"complianceReview"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:16024

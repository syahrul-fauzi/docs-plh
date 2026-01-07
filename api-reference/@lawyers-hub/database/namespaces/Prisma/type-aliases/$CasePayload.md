[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$CasePayload

# Type Alias: $CasePayload\<ExtArgs\>

> **$CasePayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5923

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:5940

---

### name

> **name**: `"Case"`

Defined in: node_modules/.prisma/client/index.d.ts:5924

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:5925

#### comments

> **comments**: [`$CommentPayload`]($CommentPayload.md)\<`ExtArgs`\>[]

#### documents

> **documents**: [`$DocumentPayload`]($DocumentPayload.md)\<`ExtArgs`\>[]

#### drafts

> **drafts**: [`$DraftPayload`]($DraftPayload.md)\<`ExtArgs`\>[]

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `createdAt`: `Date`;
> `description`: `string` \| `null`; `id`: `string`; `status`: `string`;
> `tenantId`: `string`; `title`: `string`; `updatedAt`: `Date`; \},
> `ExtArgs`\[`"result"`\]\[`"case"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:5931

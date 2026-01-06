[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / $DraftPayload

# Type Alias: $DraftPayload\<ExtArgs\>

> **$DraftPayload**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:7996

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:8015

***

### name

> **name**: `"Draft"`

Defined in: node\_modules/.prisma/client/index.d.ts:7997

***

### objects

> **objects**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:7998

#### case

> **case**: [`$CasePayload`]($CasePayload.md)\<`ExtArgs`\> \| `null`

#### comments

> **comments**: [`$CommentPayload`]($CommentPayload.md)\<`ExtArgs`\>[]

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

***

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `caseId`: `string` \| `null`; `content`: `string`; `createdAt`: `Date`; `id`: `string`; `metadata`: [`JsonValue`](JsonValue.md) \| `null`; `status`: `string`; `templateType`: `string` \| `null`; `tenantId`: `string`; `title`: `string`; `updatedAt`: `Date`; \}, `ExtArgs`\[`"result"`\]\[`"draft"`\]\>

Defined in: node\_modules/.prisma/client/index.d.ts:8003

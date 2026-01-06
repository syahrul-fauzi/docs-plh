[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / $CommentPayload

# Type Alias: $CommentPayload\<ExtArgs\>

> **$CommentPayload**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9020

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9038

***

### name

> **name**: `"Comment"`

Defined in: node\_modules/.prisma/client/index.d.ts:9021

***

### objects

> **objects**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9022

#### case

> **case**: [`$CasePayload`]($CasePayload.md)\<`ExtArgs`\> \| `null`

#### draft

> **draft**: [`$DraftPayload`]($DraftPayload.md)\<`ExtArgs`\> \| `null`

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

#### user

> **user**: [`$UserPayload`]($UserPayload.md)\<`ExtArgs`\>

***

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `caseId`: `string` \| `null`; `content`: `string`; `createdAt`: `Date`; `draftId`: `string` \| `null`; `id`: `string`; `tenantId`: `string`; `updatedAt`: `Date`; `userId`: `string`; \}, `ExtArgs`\[`"result"`\]\[`"comment"`\]\>

Defined in: node\_modules/.prisma/client/index.d.ts:9028

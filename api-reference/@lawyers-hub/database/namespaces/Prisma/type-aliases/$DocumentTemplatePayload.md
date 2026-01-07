[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$DocumentTemplatePayload

# Type Alias: $DocumentTemplatePayload\<ExtArgs\>

> **$DocumentTemplatePayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:12946

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:12961

---

### name

> **name**: `"DocumentTemplate"`

Defined in: node_modules/.prisma/client/index.d.ts:12947

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:12948

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

#### versions

> **versions**:
> [`$TemplateVersionPayload`]($TemplateVersionPayload.md)\<`ExtArgs`\>[]

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `category`: `string` \|
> `null`; `content`: `string`; `createdAt`: `Date`; `id`: `string`; `name`:
> `string`; `tenantId`: `string`; `updatedAt`: `Date`; \},
> `ExtArgs`\[`"result"`\]\[`"documentTemplate"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:12952

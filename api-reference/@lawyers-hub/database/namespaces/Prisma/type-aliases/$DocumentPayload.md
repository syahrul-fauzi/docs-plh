[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
$DocumentPayload

# Type Alias: $DocumentPayload\<ExtArgs\>

> **$DocumentPayload**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:6964

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:6981

---

### name

> **name**: `"Document"`

Defined in: node_modules/.prisma/client/index.d.ts:6965

---

### objects

> **objects**: `object`

Defined in: node_modules/.prisma/client/index.d.ts:6966

#### case

> **case**: [`$CasePayload`]($CasePayload.md)\<`ExtArgs`\> \| `null`

#### piiAuditLogs

> **piiAuditLogs**:
> [`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\<`ExtArgs`\>[]

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

---

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `caseId`: `string` \| `null`;
> `content`: `string`; `createdAt`: `Date`; `id`: `string`; `status`: `string`;
> `tenantId`: `string`; `title`: `string`; `updatedAt`: `Date`; \},
> `ExtArgs`\[`"result"`\]\[`"document"`\]\>

Defined in: node_modules/.prisma/client/index.d.ts:6971

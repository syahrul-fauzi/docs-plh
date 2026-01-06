[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / $UserPayload

# Type Alias: $UserPayload\<ExtArgs\>

> **$UserPayload**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4848

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4867

***

### name

> **name**: `"User"`

Defined in: node\_modules/.prisma/client/index.d.ts:4849

***

### objects

> **objects**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4850

#### auditLogs

> **auditLogs**: [`$AuditLogPayload`]($AuditLogPayload.md)\<`ExtArgs`\>[]

#### comments

> **comments**: [`$CommentPayload`]($CommentPayload.md)\<`ExtArgs`\>[]

#### complianceReviews

> **complianceReviews**: [`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\<`ExtArgs`\>[]

#### piiAuditLogs

> **piiAuditLogs**: [`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\<`ExtArgs`\>[]

#### templateVersions

> **templateVersions**: [`$TemplateVersionPayload`]($TemplateVersionPayload.md)\<`ExtArgs`\>[]

#### tenant

> **tenant**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

***

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `createdAt`: `Date`; `email`: `string`; `fullName`: `string`; `id`: `string`; `role`: `string`; `tenantId`: `string`; `updatedAt`: `Date`; \}, `ExtArgs`\[`"result"`\]\[`"user"`\]\>

Defined in: node\_modules/.prisma/client/index.d.ts:4858

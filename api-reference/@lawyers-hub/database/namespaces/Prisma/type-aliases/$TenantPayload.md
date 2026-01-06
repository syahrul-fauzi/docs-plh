[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / $TenantPayload

# Type Alias: $TenantPayload\<ExtArgs\>

> **$TenantPayload**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:2601

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### composites

> **composites**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:2625

***

### name

> **name**: `"Tenant"`

Defined in: node\_modules/.prisma/client/index.d.ts:2602

***

### objects

> **objects**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:2603

#### auditLogs

> **auditLogs**: [`$AuditLogPayload`]($AuditLogPayload.md)\<`ExtArgs`\>[]

#### cases

> **cases**: [`$CasePayload`]($CasePayload.md)\<`ExtArgs`\>[]

#### comments

> **comments**: [`$CommentPayload`]($CommentPayload.md)\<`ExtArgs`\>[]

#### complianceReviews

> **complianceReviews**: [`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\<`ExtArgs`\>[]

#### documents

> **documents**: [`$DocumentPayload`]($DocumentPayload.md)\<`ExtArgs`\>[]

#### documentTemplates

> **documentTemplates**: [`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\<`ExtArgs`\>[]

#### drafts

> **drafts**: [`$DraftPayload`]($DraftPayload.md)\<`ExtArgs`\>[]

#### invitations

> **invitations**: [`$InvitationPayload`]($InvitationPayload.md)\<`ExtArgs`\>[]

#### piiAuditLogs

> **piiAuditLogs**: [`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\<`ExtArgs`\>[]

#### subscription

> **subscription**: [`$SubscriptionPayload`]($SubscriptionPayload.md)\<`ExtArgs`\> \| `null`

#### usageRecords

> **usageRecords**: [`$UsagePayload`]($UsagePayload.md)\<`ExtArgs`\>[]

#### users

> **users**: [`$UserPayload`]($UserPayload.md)\<`ExtArgs`\>[]

***

### scalars

> **scalars**: `$Extensions.GetPayloadResult`\<\{ `createdAt`: `Date`; `id`: `string`; `isActive`: `boolean`; `name`: `string`; `slug`: `string`; `updatedAt`: `Date`; \}, `ExtArgs`\[`"result"`\]\[`"tenant"`\]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2617

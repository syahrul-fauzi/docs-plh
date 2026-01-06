[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantWhereInput

# Type Alias: TenantWhereInput

> **TenantWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:18195

Deep Input Types

## Properties

### AND?

> `optional` **AND**: `TenantWhereInput` \| `TenantWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18196

***

### auditLogs?

> `optional` **auditLogs**: [`AuditLogListRelationFilter`](AuditLogListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18205

***

### cases?

> `optional` **cases**: [`CaseListRelationFilter`](CaseListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18206

***

### comments?

> `optional` **comments**: [`CommentListRelationFilter`](CommentListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18207

***

### complianceReviews?

> `optional` **complianceReviews**: [`ComplianceReviewListRelationFilter`](ComplianceReviewListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18208

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Tenant"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18203

***

### documents?

> `optional` **documents**: [`DocumentListRelationFilter`](DocumentListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18210

***

### documentTemplates?

> `optional` **documentTemplates**: [`DocumentTemplateListRelationFilter`](DocumentTemplateListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18209

***

### drafts?

> `optional` **drafts**: [`DraftListRelationFilter`](DraftListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18211

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"Tenant"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18199

***

### invitations?

> `optional` **invitations**: [`InvitationListRelationFilter`](InvitationListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18212

***

### isActive?

> `optional` **isActive**: [`BoolFilter`](BoolFilter.md)\<`"Tenant"`\> \| `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:18202

***

### name?

> `optional` **name**: [`StringFilter`](StringFilter.md)\<`"Tenant"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18200

***

### NOT?

> `optional` **NOT**: `TenantWhereInput` \| `TenantWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18198

***

### OR?

> `optional` **OR**: `TenantWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18197

***

### piiAuditLogs?

> `optional` **piiAuditLogs**: [`PIIAuditLogListRelationFilter`](PIIAuditLogListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18213

***

### slug?

> `optional` **slug**: [`StringFilter`](StringFilter.md)\<`"Tenant"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18201

***

### subscription?

> `optional` **subscription**: [`XOR`](XOR.md)\<[`SubscriptionNullableRelationFilter`](SubscriptionNullableRelationFilter.md), [`SubscriptionWhereInput`](SubscriptionWhereInput.md)\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18214

***

### updatedAt?

> `optional` **updatedAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Tenant"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18204

***

### usageRecords?

> `optional` **usageRecords**: [`UsageListRelationFilter`](UsageListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18215

***

### users?

> `optional` **users**: [`UserListRelationFilter`](UserListRelationFilter.md)

Defined in: node\_modules/.prisma/client/index.d.ts:18216

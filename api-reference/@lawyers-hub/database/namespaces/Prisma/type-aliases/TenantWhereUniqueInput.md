[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TenantWhereUniqueInput

# Type Alias: TenantWhereUniqueInput

> **TenantWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`TenantWhereInput`](TenantWhereInput.md) \|
> [`TenantWhereInput`](TenantWhereInput.md)[]; `auditLogs?`:
> [`AuditLogListRelationFilter`](AuditLogListRelationFilter.md); `cases?`:
> [`CaseListRelationFilter`](CaseListRelationFilter.md); `comments?`:
> [`CommentListRelationFilter`](CommentListRelationFilter.md);
> `complianceReviews?`:
> [`ComplianceReviewListRelationFilter`](ComplianceReviewListRelationFilter.md);
> `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Tenant"`\> \| `Date` \|
> `string`; `documents?`:
> [`DocumentListRelationFilter`](DocumentListRelationFilter.md);
> `documentTemplates?`:
> [`DocumentTemplateListRelationFilter`](DocumentTemplateListRelationFilter.md);
> `drafts?`: [`DraftListRelationFilter`](DraftListRelationFilter.md); `id?`:
> `string`; `invitations?`:
> [`InvitationListRelationFilter`](InvitationListRelationFilter.md);
> `isActive?`: [`BoolFilter`](BoolFilter.md)\<`"Tenant"`\> \| `boolean`;
> `name?`: [`StringFilter`](StringFilter.md)\<`"Tenant"`\> \| `string`; `NOT?`:
> [`TenantWhereInput`](TenantWhereInput.md) \|
> [`TenantWhereInput`](TenantWhereInput.md)[]; `OR?`:
> [`TenantWhereInput`](TenantWhereInput.md)[]; `piiAuditLogs?`:
> [`PIIAuditLogListRelationFilter`](PIIAuditLogListRelationFilter.md); `slug?`:
> `string`; `subscription?`:
> [`XOR`](XOR.md)\<[`SubscriptionNullableRelationFilter`](SubscriptionNullableRelationFilter.md),
> [`SubscriptionWhereInput`](SubscriptionWhereInput.md)\> \| `null`;
> `updatedAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Tenant"`\> \| `Date` \|
> `string`; `usageRecords?`:
> [`UsageListRelationFilter`](UsageListRelationFilter.md); `users?`:
> [`UserListRelationFilter`](UserListRelationFilter.md); \}, `"id"` \|
> `"slug"`\>

Defined in: node_modules/.prisma/client/index.d.ts:18240

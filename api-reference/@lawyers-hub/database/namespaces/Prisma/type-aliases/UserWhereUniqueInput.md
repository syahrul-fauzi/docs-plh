[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserWhereUniqueInput

# Type Alias: UserWhereUniqueInput

> **UserWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`UserWhereInput`](UserWhereInput.md) \|
> [`UserWhereInput`](UserWhereInput.md)[]; `auditLogs?`:
> [`AuditLogListRelationFilter`](AuditLogListRelationFilter.md); `comments?`:
> [`CommentListRelationFilter`](CommentListRelationFilter.md);
> `complianceReviews?`:
> [`ComplianceReviewListRelationFilter`](ComplianceReviewListRelationFilter.md);
> `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"User"`\> \| `Date` \|
> `string`; `email?`: `string`; `fullName?`:
> [`StringFilter`](StringFilter.md)\<`"User"`\> \| `string`; `id?`: `string`;
> `NOT?`: [`UserWhereInput`](UserWhereInput.md) \|
> [`UserWhereInput`](UserWhereInput.md)[]; `OR?`:
> [`UserWhereInput`](UserWhereInput.md)[]; `piiAuditLogs?`:
> [`PIIAuditLogListRelationFilter`](PIIAuditLogListRelationFilter.md); `role?`:
> [`StringFilter`](StringFilter.md)\<`"User"`\> \| `string`;
> `templateVersions?`:
> [`TemplateVersionListRelationFilter`](TemplateVersionListRelationFilter.md);
> `tenant?`: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`:
> [`StringFilter`](StringFilter.md)\<`"User"`\> \| `string`; `updatedAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"User"`\> \| `Date` \| `string`; \},
> `"id"` \| `"email"`\>

Defined in: node_modules/.prisma/client/index.d.ts:18405

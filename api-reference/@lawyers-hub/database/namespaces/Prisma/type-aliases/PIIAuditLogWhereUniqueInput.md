[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogWhereUniqueInput

# Type Alias: PIIAuditLogWhereUniqueInput

> **PIIAuditLogWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `actionType?`:
> [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`; `AND?`:
> [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md) \|
> [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)[]; `document?`:
> [`XOR`](XOR.md)\<[`DocumentNullableRelationFilter`](DocumentNullableRelationFilter.md),
> [`DocumentWhereInput`](DocumentWhereInput.md)\> \| `null`; `documentId?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \|
> `string` \| `null`; `id?`: `string`; `isMasked?`:
> [`BoolFilter`](BoolFilter.md)\<`"PIIAuditLog"`\> \| `boolean`;
> `justification?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \|
> `string` \| `null`; `metadata?`:
> [`JsonNullableFilter`](JsonNullableFilter.md)\<`"PIIAuditLog"`\>; `NOT?`:
> [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md) \|
> [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)[]; `OR?`:
> [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)[]; `piiType?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"PIIAuditLog"`\> \|
> `string` \| `null`; `riskScore?`:
> [`IntFilter`](IntFilter.md)\<`"PIIAuditLog"`\> \| `number`; `tenant?`:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`:
> [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`;
> `timestamp?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"PIIAuditLog"`\> \|
> `Date` \| `string`; `user?`:
> [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md),
> [`UserWhereInput`](UserWhereInput.md)\>; `userId?`:
> [`StringFilter`](StringFilter.md)\<`"PIIAuditLog"`\> \| `string`; \}, `"id"`\>

Defined in: node_modules/.prisma/client/index.d.ts:19344

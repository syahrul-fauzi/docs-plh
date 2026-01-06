[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogWhereUniqueInput

# Type Alias: AuditLogWhereUniqueInput

> **AuditLogWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `action?`: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`; `AND?`: [`AuditLogWhereInput`](AuditLogWhereInput.md) \| [`AuditLogWhereInput`](AuditLogWhereInput.md)[]; `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"AuditLog"`\> \| `Date` \| `string`; `entityId?`: [`StringNullableFilter`](StringNullableFilter.md)\<`"AuditLog"`\> \| `string` \| `null`; `entityType?`: [`StringNullableFilter`](StringNullableFilter.md)\<`"AuditLog"`\> \| `string` \| `null`; `id?`: `string`; `metadata?`: [`JsonNullableFilter`](JsonNullableFilter.md)\<`"AuditLog"`\>; `NOT?`: [`AuditLogWhereInput`](AuditLogWhereInput.md) \| [`AuditLogWhereInput`](AuditLogWhereInput.md)[]; `OR?`: [`AuditLogWhereInput`](AuditLogWhereInput.md)[]; `tenant?`: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`; `user?`: [`XOR`](XOR.md)\<[`UserRelationFilter`](UserRelationFilter.md), [`UserWhereInput`](UserWhereInput.md)\>; `userId?`: [`StringFilter`](StringFilter.md)\<`"AuditLog"`\> \| `string`; \}, `"id"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:18794

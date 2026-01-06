[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentWhereUniqueInput

# Type Alias: DocumentWhereUniqueInput

> **DocumentWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`: [`DocumentWhereInput`](DocumentWhereInput.md) \| [`DocumentWhereInput`](DocumentWhereInput.md)[]; `case?`: [`XOR`](XOR.md)\<[`CaseNullableRelationFilter`](CaseNullableRelationFilter.md), [`CaseWhereInput`](CaseWhereInput.md)\> \| `null`; `caseId?`: [`StringNullableFilter`](StringNullableFilter.md)\<`"Document"`\> \| `string` \| `null`; `content?`: [`StringFilter`](StringFilter.md)\<`"Document"`\> \| `string`; `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Document"`\> \| `Date` \| `string`; `id?`: `string`; `NOT?`: [`DocumentWhereInput`](DocumentWhereInput.md) \| [`DocumentWhereInput`](DocumentWhereInput.md)[]; `OR?`: [`DocumentWhereInput`](DocumentWhereInput.md)[]; `piiAuditLogs?`: [`PIIAuditLogListRelationFilter`](PIIAuditLogListRelationFilter.md); `status?`: [`StringFilter`](StringFilter.md)\<`"Document"`\> \| `string`; `tenant?`: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`: [`StringFilter`](StringFilter.md)\<`"Document"`\> \| `string`; `title?`: [`StringFilter`](StringFilter.md)\<`"Document"`\> \| `string`; `updatedAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Document"`\> \| `Date` \| `string`; \}, `"id"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:18555

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / InvitationWhereUniqueInput

# Type Alias: InvitationWhereUniqueInput

> **InvitationWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`: [`InvitationWhereInput`](InvitationWhereInput.md) \| [`InvitationWhereInput`](InvitationWhereInput.md)[]; `createdAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Invitation"`\> \| `Date` \| `string`; `email?`: [`StringFilter`](StringFilter.md)\<`"Invitation"`\> \| `string`; `expiresAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Invitation"`\> \| `Date` \| `string`; `id?`: `string`; `NOT?`: [`InvitationWhereInput`](InvitationWhereInput.md) \| [`InvitationWhereInput`](InvitationWhereInput.md)[]; `OR?`: [`InvitationWhereInput`](InvitationWhereInput.md)[]; `role?`: [`StringFilter`](StringFilter.md)\<`"Invitation"`\> \| `string`; `status?`: [`StringFilter`](StringFilter.md)\<`"Invitation"`\> \| `string`; `tenant?`: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`: [`StringFilter`](StringFilter.md)\<`"Invitation"`\> \| `string`; `token?`: `string`; `updatedAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Invitation"`\> \| `Date` \| `string`; \}, `"id"` \| `"token"`\>

Defined in: node\_modules/.prisma/client/index.d.ts:18929

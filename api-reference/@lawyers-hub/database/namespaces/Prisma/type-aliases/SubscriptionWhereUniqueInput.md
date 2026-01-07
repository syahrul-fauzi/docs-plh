[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SubscriptionWhereUniqueInput

# Type Alias: SubscriptionWhereUniqueInput

> **SubscriptionWhereUniqueInput** = [`AtLeast`](AtLeast.md)\<\{ `AND?`:
> [`SubscriptionWhereInput`](SubscriptionWhereInput.md) \|
> [`SubscriptionWhereInput`](SubscriptionWhereInput.md)[]; `createdAt?`:
> [`DateTimeFilter`](DateTimeFilter.md)\<`"Subscription"`\> \| `Date` \|
> `string`; `currentPeriodEnd?`:
> [`DateTimeNullableFilter`](DateTimeNullableFilter.md)\<`"Subscription"`\> \|
> `Date` \| `string` \| `null`; `id?`: `string`; `NOT?`:
> [`SubscriptionWhereInput`](SubscriptionWhereInput.md) \|
> [`SubscriptionWhereInput`](SubscriptionWhereInput.md)[]; `OR?`:
> [`SubscriptionWhereInput`](SubscriptionWhereInput.md)[]; `plan?`:
> [`StringFilter`](StringFilter.md)\<`"Subscription"`\> \| `string`;
> `quantity?`: [`IntFilter`](IntFilter.md)\<`"Subscription"`\> \| `number`;
> `status?`: [`StringFilter`](StringFilter.md)\<`"Subscription"`\> \| `string`;
> `stripeCustomerId?`: `string`; `stripePriceId?`:
> [`StringNullableFilter`](StringNullableFilter.md)\<`"Subscription"`\> \|
> `string` \| `null`; `tenant?`:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>; `tenantId?`: `string`;
> `updatedAt?`: [`DateTimeFilter`](DateTimeFilter.md)\<`"Subscription"`\> \|
> `Date` \| `string`; \}, `"id"` \| `"tenantId"` \| `"stripeCustomerId"`\>

Defined in: node_modules/.prisma/client/index.d.ts:18319

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / SubscriptionWhereInput

# Type Alias: SubscriptionWhereInput

> **SubscriptionWhereInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:18288

## Properties

### AND?

> `optional` **AND**: `SubscriptionWhereInput` \| `SubscriptionWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18289

***

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Subscription"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18300

***

### currentPeriodEnd?

> `optional` **currentPeriodEnd**: [`DateTimeNullableFilter`](DateTimeNullableFilter.md)\<`"Subscription"`\> \| `Date` \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18299

***

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"Subscription"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18292

***

### NOT?

> `optional` **NOT**: `SubscriptionWhereInput` \| `SubscriptionWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18291

***

### OR?

> `optional` **OR**: `SubscriptionWhereInput`[]

Defined in: node\_modules/.prisma/client/index.d.ts:18290

***

### plan?

> `optional` **plan**: [`StringFilter`](StringFilter.md)\<`"Subscription"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18297

***

### quantity?

> `optional` **quantity**: [`IntFilter`](IntFilter.md)\<`"Subscription"`\> \| `number`

Defined in: node\_modules/.prisma/client/index.d.ts:18298

***

### status?

> `optional` **status**: [`StringFilter`](StringFilter.md)\<`"Subscription"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18296

***

### stripeCustomerId?

> `optional` **stripeCustomerId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"Subscription"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18294

***

### stripePriceId?

> `optional` **stripePriceId**: [`StringNullableFilter`](StringNullableFilter.md)\<`"Subscription"`\> \| `string` \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:18295

***

### tenant?

> `optional` **tenant**: [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md), [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:18302

***

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"Subscription"`\> \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18293

***

### updatedAt?

> `optional` **updatedAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"Subscription"`\> \| `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:18301

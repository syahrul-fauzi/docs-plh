[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / SubscriptionCreateArgs

# Type Alias: SubscriptionCreateArgs\<ExtArgs\>

> **SubscriptionCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4475

Subscription create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`SubscriptionCreateInput`](SubscriptionCreateInput.md), [`SubscriptionUncheckedCreateInput`](SubscriptionUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:4487

The data needed to create a Subscription.

***

### include?

> `optional` **include**: [`SubscriptionInclude`](SubscriptionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:4483

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`SubscriptionSelect`](SubscriptionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:4479

Select specific fields to fetch from the Subscription

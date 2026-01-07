[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SubscriptionUpdateArgs

# Type Alias: SubscriptionUpdateArgs\<ExtArgs\>

> **SubscriptionUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:4523

Subscription update

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`SubscriptionUpdateInput`](SubscriptionUpdateInput.md),
> [`SubscriptionUncheckedUpdateInput`](SubscriptionUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:4535

The data needed to update a Subscription.

---

### include?

> `optional` **include**:
> [`SubscriptionInclude`](SubscriptionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:4531

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`SubscriptionSelect`](SubscriptionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:4527

Select specific fields to fetch from the Subscription

---

### where

> **where**: [`SubscriptionWhereUniqueInput`](SubscriptionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:4539

Choose, which Subscription to update.

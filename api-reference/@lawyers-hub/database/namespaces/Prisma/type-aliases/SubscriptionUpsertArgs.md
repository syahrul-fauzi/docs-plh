[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SubscriptionUpsertArgs

# Type Alias: SubscriptionUpsertArgs\<ExtArgs\>

> **SubscriptionUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:4559

Subscription upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**:
> [`XOR`](XOR.md)\<[`SubscriptionCreateInput`](SubscriptionCreateInput.md),
> [`SubscriptionUncheckedCreateInput`](SubscriptionUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:4575

In case the Subscription found by the `where` argument doesn't exist, create a
new Subscription with this data.

---

### include?

> `optional` **include**:
> [`SubscriptionInclude`](SubscriptionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:4567

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`SubscriptionSelect`](SubscriptionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:4563

Select specific fields to fetch from the Subscription

---

### update

> **update**:
> [`XOR`](XOR.md)\<[`SubscriptionUpdateInput`](SubscriptionUpdateInput.md),
> [`SubscriptionUncheckedUpdateInput`](SubscriptionUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:4579

In case the Subscription was found with the provided `where` argument, update it
with this data.

---

### where

> **where**: [`SubscriptionWhereUniqueInput`](SubscriptionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:4571

The filter to search for the Subscription to update in case it exists.

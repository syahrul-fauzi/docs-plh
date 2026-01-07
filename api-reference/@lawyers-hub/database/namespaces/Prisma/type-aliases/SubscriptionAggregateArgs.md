[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SubscriptionAggregateArgs

# Type Alias: SubscriptionAggregateArgs\<ExtArgs\>

> **SubscriptionAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3707

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_avg?

> `optional` **\_avg**:
> [`SubscriptionAvgAggregateInputType`](SubscriptionAvgAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:3747

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to average

---

### \_count?

> `optional` **\_count**: `true` \|
> [`SubscriptionCountAggregateInputType`](SubscriptionCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:3741

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Subscriptions

---

### \_max?

> `optional` **\_max**:
> [`SubscriptionMaxAggregateInputType`](SubscriptionMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:3765

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`SubscriptionMinAggregateInputType`](SubscriptionMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:3759

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### \_sum?

> `optional` **\_sum**:
> [`SubscriptionSumAggregateInputType`](SubscriptionSumAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:3753

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to sum

---

### cursor?

> `optional` **cursor**:
> [`SubscriptionWhereUniqueInput`](SubscriptionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3723

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md)
> \|
> [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3717

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Subscriptions to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3735

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Subscriptions.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3729

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Subscriptions from the position of the cursor.

---

### where?

> `optional` **where**: [`SubscriptionWhereInput`](SubscriptionWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3711

Filter which Subscription to aggregate.

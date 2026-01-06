[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / SubscriptionFindManyArgs

# Type Alias: SubscriptionFindManyArgs\<ExtArgs\>

> **SubscriptionFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4432

Subscription findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`SubscriptionWhereUniqueInput`](SubscriptionWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4456

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Subscriptions.

***

### distinct?

> `optional` **distinct**: [`SubscriptionScalarFieldEnum`](SubscriptionScalarFieldEnum.md) \| [`SubscriptionScalarFieldEnum`](SubscriptionScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:4469

***

### include?

> `optional` **include**: [`SubscriptionInclude`](SubscriptionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:4440

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md) \| [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:4450

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Subscriptions to fetch.

***

### select?

> `optional` **select**: [`SubscriptionSelect`](SubscriptionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:4436

Select specific fields to fetch from the Subscription

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:4468

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Subscriptions.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:4462

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Subscriptions from the position of the cursor.

***

### where?

> `optional` **where**: [`SubscriptionWhereInput`](SubscriptionWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4444

Filter, which Subscriptions to fetch.

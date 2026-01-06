[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / SubscriptionFindFirstArgs

# Type Alias: SubscriptionFindFirstArgs\<ExtArgs\>

> **SubscriptionFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4336

Subscription findFirst

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`SubscriptionWhereUniqueInput`](SubscriptionWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4360

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Subscriptions.

***

### distinct?

> `optional` **distinct**: [`SubscriptionScalarFieldEnum`](SubscriptionScalarFieldEnum.md) \| [`SubscriptionScalarFieldEnum`](SubscriptionScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:4378

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Subscriptions.

***

### include?

> `optional` **include**: [`SubscriptionInclude`](SubscriptionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:4344

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md) \| [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:4354

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Subscriptions to fetch.

***

### select?

> `optional` **select**: [`SubscriptionSelect`](SubscriptionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:4340

Select specific fields to fetch from the Subscription

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:4372

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Subscriptions.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:4366

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Subscriptions from the position of the cursor.

***

### where?

> `optional` **where**: [`SubscriptionWhereInput`](SubscriptionWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4348

Filter, which Subscription to fetch.

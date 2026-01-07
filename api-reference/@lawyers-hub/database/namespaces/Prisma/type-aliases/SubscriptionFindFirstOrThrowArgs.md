[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SubscriptionFindFirstOrThrowArgs

# Type Alias: SubscriptionFindFirstOrThrowArgs\<ExtArgs\>

> **SubscriptionFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:4384

Subscription findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`SubscriptionWhereUniqueInput`](SubscriptionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:4408

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Subscriptions.

---

### distinct?

> `optional` **distinct**:
> [`SubscriptionScalarFieldEnum`](SubscriptionScalarFieldEnum.md) \|
> [`SubscriptionScalarFieldEnum`](SubscriptionScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:4426

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Subscriptions.

---

### include?

> `optional` **include**:
> [`SubscriptionInclude`](SubscriptionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:4392

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md)
> \|
> [`SubscriptionOrderByWithRelationInput`](SubscriptionOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:4402

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Subscriptions to fetch.

---

### select?

> `optional` **select**:
> [`SubscriptionSelect`](SubscriptionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:4388

Select specific fields to fetch from the Subscription

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:4420

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Subscriptions.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:4414

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Subscriptions from the position of the cursor.

---

### where?

> `optional` **where**: [`SubscriptionWhereInput`](SubscriptionWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:4396

Filter, which Subscription to fetch.

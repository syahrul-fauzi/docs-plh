[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserAggregateArgs

# Type Alias: UserAggregateArgs\<ExtArgs\>

> **UserAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:4698

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`UserCountAggregateInputType`](UserCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4732

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Users

***

### \_max?

> `optional` **\_max**: [`UserMaxAggregateInputType`](UserMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4744

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`UserMinAggregateInputType`](UserMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4738

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`UserWhereUniqueInput`](UserWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4714

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`UserOrderByWithRelationInput`](UserOrderByWithRelationInput.md) \| [`UserOrderByWithRelationInput`](UserOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:4708

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Users to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:4726

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Users.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:4720

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Users from the position of the cursor.

***

### where?

> `optional` **where**: [`UserWhereInput`](UserWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:4702

Filter which User to aggregate.

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentAggregateArgs

# Type Alias: CommentAggregateArgs\<ExtArgs\>

> **CommentAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:8866

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`CommentCountAggregateInputType`](CommentCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8900

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Comments

***

### \_max?

> `optional` **\_max**: [`CommentMaxAggregateInputType`](CommentMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8912

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`CommentMinAggregateInputType`](CommentMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8906

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8882

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md) \| [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:8876

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Comments to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:8894

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Comments.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:8888

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Comments from the position of the cursor.

***

### where?

> `optional` **where**: [`CommentWhereInput`](CommentWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8870

Filter which Comment to aggregate.

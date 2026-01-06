[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentAggregateArgs

# Type Alias: DocumentAggregateArgs\<ExtArgs\>

> **DocumentAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:6814

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`DocumentCountAggregateInputType`](DocumentCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6848

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Documents

***

### \_max?

> `optional` **\_max**: [`DocumentMaxAggregateInputType`](DocumentMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6860

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`DocumentMinAggregateInputType`](DocumentMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6854

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6830

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md) \| [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:6824

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Documents to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:6842

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Documents.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:6836

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Documents from the position of the cursor.

***

### where?

> `optional` **where**: [`DocumentWhereInput`](DocumentWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6818

Filter which Document to aggregate.

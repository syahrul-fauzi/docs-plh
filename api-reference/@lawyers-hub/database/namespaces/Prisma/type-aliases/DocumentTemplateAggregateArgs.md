[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentTemplateAggregateArgs

# Type Alias: DocumentTemplateAggregateArgs\<ExtArgs\>

> **DocumentTemplateAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:12804

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`DocumentTemplateCountAggregateInputType`](DocumentTemplateCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12838

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned DocumentTemplates

***

### \_max?

> `optional` **\_max**: [`DocumentTemplateMaxAggregateInputType`](DocumentTemplateMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12850

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`DocumentTemplateMinAggregateInputType`](DocumentTemplateMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12844

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`DocumentTemplateWhereUniqueInput`](DocumentTemplateWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12820

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md) \| [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:12814

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of DocumentTemplates to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:12832

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` DocumentTemplates.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:12826

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` DocumentTemplates from the position of the cursor.

***

### where?

> `optional` **where**: [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12808

Filter which DocumentTemplate to aggregate.

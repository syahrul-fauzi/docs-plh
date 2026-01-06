[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TemplateVersionAggregateArgs

# Type Alias: TemplateVersionAggregateArgs\<ExtArgs\>

> **TemplateVersionAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:13805

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_avg?

> `optional` **\_avg**: [`TemplateVersionAvgAggregateInputType`](TemplateVersionAvgAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13845

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to average

***

### \_count?

> `optional` **\_count**: `true` \| [`TemplateVersionCountAggregateInputType`](TemplateVersionCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13839

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned TemplateVersions

***

### \_max?

> `optional` **\_max**: [`TemplateVersionMaxAggregateInputType`](TemplateVersionMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13863

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`TemplateVersionMinAggregateInputType`](TemplateVersionMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13857

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### \_sum?

> `optional` **\_sum**: [`TemplateVersionSumAggregateInputType`](TemplateVersionSumAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13851

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to sum

***

### cursor?

> `optional` **cursor**: [`TemplateVersionWhereUniqueInput`](TemplateVersionWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13821

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`TemplateVersionOrderByWithRelationInput`](TemplateVersionOrderByWithRelationInput.md) \| [`TemplateVersionOrderByWithRelationInput`](TemplateVersionOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:13815

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of TemplateVersions to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:13833

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` TemplateVersions.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:13827

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` TemplateVersions from the position of the cursor.

***

### where?

> `optional` **where**: [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13809

Filter which TemplateVersion to aggregate.

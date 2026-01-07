[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AIModelConfigAggregateArgs

# Type Alias: AIModelConfigAggregateArgs\<ExtArgs\>

> **AIModelConfigAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:14828

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_avg?

> `optional` **\_avg**:
> [`AIModelConfigAvgAggregateInputType`](AIModelConfigAvgAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:14868

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to average

---

### \_count?

> `optional` **\_count**: `true` \|
> [`AIModelConfigCountAggregateInputType`](AIModelConfigCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:14862

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned AIModelConfigs

---

### \_max?

> `optional` **\_max**:
> [`AIModelConfigMaxAggregateInputType`](AIModelConfigMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:14886

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`AIModelConfigMinAggregateInputType`](AIModelConfigMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:14880

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### \_sum?

> `optional` **\_sum**:
> [`AIModelConfigSumAggregateInputType`](AIModelConfigSumAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:14874

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to sum

---

### cursor?

> `optional` **cursor**:
> [`AIModelConfigWhereUniqueInput`](AIModelConfigWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14844

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`AIModelConfigOrderByWithRelationInput`](AIModelConfigOrderByWithRelationInput.md)
> \|
> [`AIModelConfigOrderByWithRelationInput`](AIModelConfigOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:14838

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of AIModelConfigs to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:14856

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` AIModelConfigs.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:14850

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` AIModelConfigs from the position of the cursor.

---

### where?

> `optional` **where**: [`AIModelConfigWhereInput`](AIModelConfigWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14832

Filter which AIModelConfig to aggregate.

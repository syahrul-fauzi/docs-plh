[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UsageAggregateArgs

# Type Alias: UsageAggregateArgs\<ExtArgs\>

> **UsageAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:10856

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_avg?

> `optional` **\_avg**:
> [`UsageAvgAggregateInputType`](UsageAvgAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:10896

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to average

---

### \_count?

> `optional` **\_count**: `true` \|
> [`UsageCountAggregateInputType`](UsageCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:10890

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Usages

---

### \_max?

> `optional` **\_max**:
> [`UsageMaxAggregateInputType`](UsageMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:10914

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`UsageMinAggregateInputType`](UsageMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:10908

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### \_sum?

> `optional` **\_sum**:
> [`UsageSumAggregateInputType`](UsageSumAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:10902

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to sum

---

### cursor?

> `optional` **cursor**: [`UsageWhereUniqueInput`](UsageWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:10872

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`UsageOrderByWithRelationInput`](UsageOrderByWithRelationInput.md) \|
> [`UsageOrderByWithRelationInput`](UsageOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:10866

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Usages to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:10884

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Usages.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:10878

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Usages from the position of the cursor.

---

### where?

> `optional` **where**: [`UsageWhereInput`](UsageWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:10860

Filter which Usage to aggregate.

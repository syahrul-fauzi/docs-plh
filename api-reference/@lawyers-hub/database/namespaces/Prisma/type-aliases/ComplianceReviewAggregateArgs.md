[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
ComplianceReviewAggregateArgs

# Type Alias: ComplianceReviewAggregateArgs\<ExtArgs\>

> **ComplianceReviewAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:15832

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_avg?

> `optional` **\_avg**:
> [`ComplianceReviewAvgAggregateInputType`](ComplianceReviewAvgAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:15872

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to average

---

### \_count?

> `optional` **\_count**: `true` \|
> [`ComplianceReviewCountAggregateInputType`](ComplianceReviewCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:15866

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned ComplianceReviews

---

### \_max?

> `optional` **\_max**:
> [`ComplianceReviewMaxAggregateInputType`](ComplianceReviewMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:15890

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`ComplianceReviewMinAggregateInputType`](ComplianceReviewMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:15884

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### \_sum?

> `optional` **\_sum**:
> [`ComplianceReviewSumAggregateInputType`](ComplianceReviewSumAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:15878

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to sum

---

### cursor?

> `optional` **cursor**:
> [`ComplianceReviewWhereUniqueInput`](ComplianceReviewWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:15848

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`ComplianceReviewOrderByWithRelationInput`](ComplianceReviewOrderByWithRelationInput.md)
> \|
> [`ComplianceReviewOrderByWithRelationInput`](ComplianceReviewOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:15842

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of ComplianceReviews to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:15860

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` ComplianceReviews.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:15854

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` ComplianceReviews from the position of the cursor.

---

### where?

> `optional` **where**:
> [`ComplianceReviewWhereInput`](ComplianceReviewWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:15836

Filter which ComplianceReview to aggregate.

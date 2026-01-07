[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseAggregateArgs

# Type Alias: CaseAggregateArgs\<ExtArgs\>

> **CaseAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5777

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \|
> [`CaseCountAggregateInputType`](CaseCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:5811

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Cases

---

### \_max?

> `optional` **\_max**:
> [`CaseMaxAggregateInputType`](CaseMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:5823

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`CaseMinAggregateInputType`](CaseMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:5817

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### cursor?

> `optional` **cursor**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5793

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`CaseOrderByWithRelationInput`](CaseOrderByWithRelationInput.md) \|
> [`CaseOrderByWithRelationInput`](CaseOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5787

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Cases to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5805

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Cases.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5799

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Cases from the position of the cursor.

---

### where?

> `optional` **where**: [`CaseWhereInput`](CaseWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5781

Filter which Case to aggregate.

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DraftAggregateArgs

# Type Alias: DraftAggregateArgs\<ExtArgs\>

> **DraftAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:7838

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \|
> [`DraftCountAggregateInputType`](DraftCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:7872

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Drafts

---

### \_max?

> `optional` **\_max**:
> [`DraftMaxAggregateInputType`](DraftMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:7884

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`DraftMinAggregateInputType`](DraftMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:7878

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### cursor?

> `optional` **cursor**: [`DraftWhereUniqueInput`](DraftWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7854

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`DraftOrderByWithRelationInput`](DraftOrderByWithRelationInput.md) \|
> [`DraftOrderByWithRelationInput`](DraftOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:7848

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Drafts to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:7866

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Drafts.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:7860

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Drafts from the position of the cursor.

---

### where?

> `optional` **where**: [`DraftWhereInput`](DraftWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7842

Filter which Draft to aggregate.

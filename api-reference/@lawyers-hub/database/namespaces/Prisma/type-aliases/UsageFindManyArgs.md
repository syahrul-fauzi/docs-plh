[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UsageFindManyArgs

# Type Alias: UsageFindManyArgs\<ExtArgs\>

> **UsageFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:11557

Usage findMany

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`UsageWhereUniqueInput`](UsageWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:11581

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Usages.

---

### distinct?

> `optional` **distinct**: [`UsageScalarFieldEnum`](UsageScalarFieldEnum.md) \|
> [`UsageScalarFieldEnum`](UsageScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:11594

---

### include?

> `optional` **include**: [`UsageInclude`](UsageInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:11565

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`UsageOrderByWithRelationInput`](UsageOrderByWithRelationInput.md) \|
> [`UsageOrderByWithRelationInput`](UsageOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:11575

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Usages to fetch.

---

### select?

> `optional` **select**: [`UsageSelect`](UsageSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:11561

Select specific fields to fetch from the Usage

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:11593

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Usages.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:11587

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Usages from the position of the cursor.

---

### where?

> `optional` **where**: [`UsageWhereInput`](UsageWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:11569

Filter, which Usages to fetch.

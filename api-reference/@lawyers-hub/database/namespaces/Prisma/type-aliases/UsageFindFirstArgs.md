[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UsageFindFirstArgs

# Type Alias: UsageFindFirstArgs\<ExtArgs\>

> **UsageFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:11461

Usage findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`UsageWhereUniqueInput`](UsageWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:11485

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Usages.

---

### distinct?

> `optional` **distinct**: [`UsageScalarFieldEnum`](UsageScalarFieldEnum.md) \|
> [`UsageScalarFieldEnum`](UsageScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:11503

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Usages.

---

### include?

> `optional` **include**: [`UsageInclude`](UsageInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:11469

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`UsageOrderByWithRelationInput`](UsageOrderByWithRelationInput.md) \|
> [`UsageOrderByWithRelationInput`](UsageOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:11479

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Usages to fetch.

---

### select?

> `optional` **select**: [`UsageSelect`](UsageSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:11465

Select specific fields to fetch from the Usage

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:11497

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Usages.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:11491

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Usages from the position of the cursor.

---

### where?

> `optional` **where**: [`UsageWhereInput`](UsageWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:11473

Filter, which Usage to fetch.

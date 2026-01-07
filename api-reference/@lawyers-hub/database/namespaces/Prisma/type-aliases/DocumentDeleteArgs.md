[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentDeleteArgs

# Type Alias: DocumentDeleteArgs\<ExtArgs\>

> **DocumentDeleteArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:7676

Document delete

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:7684

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:7680

Select specific fields to fetch from the Document

---

### where

> **where**: [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7688

Filter which Document to delete.

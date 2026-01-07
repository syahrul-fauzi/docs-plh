[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentUpdateArgs

# Type Alias: DocumentUpdateArgs\<ExtArgs\>

> **DocumentUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:7614

Document update

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`DocumentUpdateInput`](DocumentUpdateInput.md),
> [`DocumentUncheckedUpdateInput`](DocumentUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:7626

The data needed to update a Document.

---

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:7622

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:7618

Select specific fields to fetch from the Document

---

### where

> **where**: [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7630

Choose, which Document to update.

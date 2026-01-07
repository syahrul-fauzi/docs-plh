[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentUpsertArgs

# Type Alias: DocumentUpsertArgs\<ExtArgs\>

> **DocumentUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:7650

Document upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`DocumentCreateInput`](DocumentCreateInput.md),
> [`DocumentUncheckedCreateInput`](DocumentUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:7666

In case the Document found by the `where` argument doesn't exist, create a new
Document with this data.

---

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:7658

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:7654

Select specific fields to fetch from the Document

---

### update

> **update**: [`XOR`](XOR.md)\<[`DocumentUpdateInput`](DocumentUpdateInput.md),
> [`DocumentUncheckedUpdateInput`](DocumentUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:7670

In case the Document was found with the provided `where` argument, update it
with this data.

---

### where

> **where**: [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7662

The filter to search for the Document to update in case it exists.

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DraftUpdateArgs

# Type Alias: DraftUpdateArgs\<ExtArgs\>

> **DraftUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:8650

Draft update

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`DraftUpdateInput`](DraftUpdateInput.md),
> [`DraftUncheckedUpdateInput`](DraftUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:8662

The data needed to update a Draft.

---

### include?

> `optional` **include**: [`DraftInclude`](DraftInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:8658

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`DraftSelect`](DraftSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:8654

Select specific fields to fetch from the Draft

---

### where

> **where**: [`DraftWhereUniqueInput`](DraftWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:8666

Choose, which Draft to update.

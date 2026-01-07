[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DraftCreateArgs

# Type Alias: DraftCreateArgs\<ExtArgs\>

> **DraftCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:8602

Draft create

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`DraftCreateInput`](DraftCreateInput.md),
> [`DraftUncheckedCreateInput`](DraftUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:8614

The data needed to create a Draft.

---

### include?

> `optional` **include**: [`DraftInclude`](DraftInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:8610

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`DraftSelect`](DraftSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:8606

Select specific fields to fetch from the Draft

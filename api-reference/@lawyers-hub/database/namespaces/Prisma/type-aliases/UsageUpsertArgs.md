[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UsageUpsertArgs

# Type Alias: UsageUpsertArgs\<ExtArgs\>

> **UsageUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:11684

Usage upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`UsageCreateInput`](UsageCreateInput.md),
> [`UsageUncheckedCreateInput`](UsageUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:11700

In case the Usage found by the `where` argument doesn't exist, create a new
Usage with this data.

---

### include?

> `optional` **include**: [`UsageInclude`](UsageInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:11692

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`UsageSelect`](UsageSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:11688

Select specific fields to fetch from the Usage

---

### update

> **update**: [`XOR`](XOR.md)\<[`UsageUpdateInput`](UsageUpdateInput.md),
> [`UsageUncheckedUpdateInput`](UsageUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:11704

In case the Usage was found with the provided `where` argument, update it with
this data.

---

### where

> **where**: [`UsageWhereUniqueInput`](UsageWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:11696

The filter to search for the Usage to update in case it exists.

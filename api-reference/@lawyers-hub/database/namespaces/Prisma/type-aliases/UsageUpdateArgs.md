[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UsageUpdateArgs

# Type Alias: UsageUpdateArgs\<ExtArgs\>

> **UsageUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:11648

Usage update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`UsageUpdateInput`](UsageUpdateInput.md), [`UsageUncheckedUpdateInput`](UsageUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:11660

The data needed to update a Usage.

***

### include?

> `optional` **include**: [`UsageInclude`](UsageInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:11656

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`UsageSelect`](UsageSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:11652

Select specific fields to fetch from the Usage

***

### where

> **where**: [`UsageWhereUniqueInput`](UsageWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:11664

Choose, which Usage to update.

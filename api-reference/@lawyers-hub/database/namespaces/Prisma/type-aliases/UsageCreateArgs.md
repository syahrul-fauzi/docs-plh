[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UsageCreateArgs

# Type Alias: UsageCreateArgs\<ExtArgs\>

> **UsageCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:11600

Usage create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`UsageCreateInput`](UsageCreateInput.md), [`UsageUncheckedCreateInput`](UsageUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:11612

The data needed to create a Usage.

***

### include?

> `optional` **include**: [`UsageInclude`](UsageInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:11608

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`UsageSelect`](UsageSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:11604

Select specific fields to fetch from the Usage

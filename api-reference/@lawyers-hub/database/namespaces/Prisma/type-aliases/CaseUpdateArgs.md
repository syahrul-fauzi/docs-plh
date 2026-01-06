[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CaseUpdateArgs

# Type Alias: CaseUpdateArgs\<ExtArgs\>

> **CaseUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:6573

Case update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`CaseUpdateInput`](CaseUpdateInput.md), [`CaseUncheckedUpdateInput`](CaseUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:6585

The data needed to update a Case.

***

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6581

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6577

Select specific fields to fetch from the Case

***

### where

> **where**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6589

Choose, which Case to update.

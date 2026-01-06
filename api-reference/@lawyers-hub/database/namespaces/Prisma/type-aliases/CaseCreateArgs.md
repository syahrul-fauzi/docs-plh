[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CaseCreateArgs

# Type Alias: CaseCreateArgs\<ExtArgs\>

> **CaseCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:6525

Case create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`CaseCreateInput`](CaseCreateInput.md), [`CaseUncheckedCreateInput`](CaseUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:6537

The data needed to create a Case.

***

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6533

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6529

Select specific fields to fetch from the Case

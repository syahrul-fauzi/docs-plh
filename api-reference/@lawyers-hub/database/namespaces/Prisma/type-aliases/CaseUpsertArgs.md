[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CaseUpsertArgs

# Type Alias: CaseUpsertArgs\<ExtArgs\>

> **CaseUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:6609

Case upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`CaseCreateInput`](CaseCreateInput.md), [`CaseUncheckedCreateInput`](CaseUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:6625

In case the Case found by the `where` argument doesn't exist, create a new Case with this data.

***

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6617

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6613

Select specific fields to fetch from the Case

***

### update

> **update**: [`XOR`](XOR.md)\<[`CaseUpdateInput`](CaseUpdateInput.md), [`CaseUncheckedUpdateInput`](CaseUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:6629

In case the Case was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6621

The filter to search for the Case to update in case it exists.

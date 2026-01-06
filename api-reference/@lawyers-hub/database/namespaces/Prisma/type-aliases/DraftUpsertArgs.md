[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DraftUpsertArgs

# Type Alias: DraftUpsertArgs\<ExtArgs\>

> **DraftUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:8686

Draft upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`DraftCreateInput`](DraftCreateInput.md), [`DraftUncheckedCreateInput`](DraftUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:8702

In case the Draft found by the `where` argument doesn't exist, create a new Draft with this data.

***

### include?

> `optional` **include**: [`DraftInclude`](DraftInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:8694

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`DraftSelect`](DraftSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:8690

Select specific fields to fetch from the Draft

***

### update

> **update**: [`XOR`](XOR.md)\<[`DraftUpdateInput`](DraftUpdateInput.md), [`DraftUncheckedUpdateInput`](DraftUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:8706

In case the Draft was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`DraftWhereUniqueInput`](DraftWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8698

The filter to search for the Draft to update in case it exists.

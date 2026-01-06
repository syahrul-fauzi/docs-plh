[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AIModelConfigUpsertArgs

# Type Alias: AIModelConfigUpsertArgs\<ExtArgs\>

> **AIModelConfigUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:15649

AIModelConfig upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`AIModelConfigCreateInput`](AIModelConfigCreateInput.md), [`AIModelConfigUncheckedCreateInput`](AIModelConfigUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:15661

In case the AIModelConfig found by the `where` argument doesn't exist, create a new AIModelConfig with this data.

***

### select?

> `optional` **select**: [`AIModelConfigSelect`](AIModelConfigSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:15653

Select specific fields to fetch from the AIModelConfig

***

### update

> **update**: [`XOR`](XOR.md)\<[`AIModelConfigUpdateInput`](AIModelConfigUpdateInput.md), [`AIModelConfigUncheckedUpdateInput`](AIModelConfigUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:15665

In case the AIModelConfig was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`AIModelConfigWhereUniqueInput`](AIModelConfigWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:15657

The filter to search for the AIModelConfig to update in case it exists.

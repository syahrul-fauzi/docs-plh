[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentCreateArgs

# Type Alias: DocumentCreateArgs\<ExtArgs\>

> **DocumentCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:7566

Document create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`DocumentCreateInput`](DocumentCreateInput.md), [`DocumentUncheckedCreateInput`](DocumentUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:7578

The data needed to create a Document.

***

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:7574

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:7570

Select specific fields to fetch from the Document

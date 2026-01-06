[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentUpdateArgs

# Type Alias: CommentUpdateArgs\<ExtArgs\>

> **CommentUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9672

Comment update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`CommentUpdateInput`](CommentUpdateInput.md), [`CommentUncheckedUpdateInput`](CommentUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:9684

The data needed to update a Comment.

***

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9680

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9676

Select specific fields to fetch from the Comment

***

### where

> **where**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9688

Choose, which Comment to update.

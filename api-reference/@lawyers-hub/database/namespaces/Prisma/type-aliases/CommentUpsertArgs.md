[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentUpsertArgs

# Type Alias: CommentUpsertArgs\<ExtArgs\>

> **CommentUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9708

Comment upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`CommentCreateInput`](CommentCreateInput.md), [`CommentUncheckedCreateInput`](CommentUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:9724

In case the Comment found by the `where` argument doesn't exist, create a new Comment with this data.

***

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9716

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9712

Select specific fields to fetch from the Comment

***

### update

> **update**: [`XOR`](XOR.md)\<[`CommentUpdateInput`](CommentUpdateInput.md), [`CommentUncheckedUpdateInput`](CommentUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:9728

In case the Comment was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9720

The filter to search for the Comment to update in case it exists.

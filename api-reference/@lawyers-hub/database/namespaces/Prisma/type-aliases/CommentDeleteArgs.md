[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentDeleteArgs

# Type Alias: CommentDeleteArgs\<ExtArgs\>

> **CommentDeleteArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9734

Comment delete

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9742

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9738

Select specific fields to fetch from the Comment

***

### where

> **where**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9746

Filter which Comment to delete.

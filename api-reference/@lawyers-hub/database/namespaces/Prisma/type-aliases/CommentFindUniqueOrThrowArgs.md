[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CommentFindUniqueOrThrowArgs

# Type Alias: CommentFindUniqueOrThrowArgs\<ExtArgs\>

> **CommentFindUniqueOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:9467

Comment findUniqueOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:9475

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:9471

Select specific fields to fetch from the Comment

---

### where

> **where**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:9479

Filter, which Comment to fetch.

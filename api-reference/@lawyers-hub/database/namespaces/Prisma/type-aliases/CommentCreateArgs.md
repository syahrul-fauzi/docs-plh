[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CommentCreateArgs

# Type Alias: CommentCreateArgs\<ExtArgs\>

> **CommentCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:9624

Comment create

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`CommentCreateInput`](CommentCreateInput.md),
> [`CommentUncheckedCreateInput`](CommentUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:9636

The data needed to create a Comment.

---

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:9632

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:9628

Select specific fields to fetch from the Comment

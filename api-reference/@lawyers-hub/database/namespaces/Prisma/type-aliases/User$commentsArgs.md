[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
User$commentsArgs

# Type Alias: User$commentsArgs\<ExtArgs\>

> **User$commentsArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5612

User.comments

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5623

---

### distinct?

> `optional` **distinct**: [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md)
> \| [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5626

---

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:5620

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md) \|
> [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5622

---

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:5616

Select specific fields to fetch from the Comment

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5625

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5624

---

### where?

> `optional` **where**: [`CommentWhereInput`](CommentWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5621

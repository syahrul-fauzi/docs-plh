[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CommentFindFirstArgs

# Type Alias: CommentFindFirstArgs\<ExtArgs\>

> **CommentFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:9485

Comment findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:9509

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Comments.

---

### distinct?

> `optional` **distinct**: [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md)
> \| [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:9527

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Comments.

---

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:9493

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md) \|
> [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:9503

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Comments to fetch.

---

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:9489

Select specific fields to fetch from the Comment

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:9521

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Comments.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:9515

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Comments from the position of the cursor.

---

### where?

> `optional` **where**: [`CommentWhereInput`](CommentWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:9497

Filter, which Comment to fetch.

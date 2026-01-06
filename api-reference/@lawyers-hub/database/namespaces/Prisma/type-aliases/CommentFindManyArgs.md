[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentFindManyArgs

# Type Alias: CommentFindManyArgs\<ExtArgs\>

> **CommentFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9581

Comment findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9605

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Comments.

***

### distinct?

> `optional` **distinct**: [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md) \| [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:9618

***

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9589

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md) \| [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:9599

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Comments to fetch.

***

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9585

Select specific fields to fetch from the Comment

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:9617

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Comments.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:9611

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Comments from the position of the cursor.

***

### where?

> `optional` **where**: [`CommentWhereInput`](CommentWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9593

Filter, which Comments to fetch.

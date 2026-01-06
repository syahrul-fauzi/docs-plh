[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentFindFirstOrThrowArgs

# Type Alias: CommentFindFirstOrThrowArgs\<ExtArgs\>

> **CommentFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9533

Comment findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`CommentWhereUniqueInput`](CommentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9557

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Comments.

***

### distinct?

> `optional` **distinct**: [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md) \| [`CommentScalarFieldEnum`](CommentScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:9575

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Comments.

***

### include?

> `optional` **include**: [`CommentInclude`](CommentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9541

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md) \| [`CommentOrderByWithRelationInput`](CommentOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:9551

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Comments to fetch.

***

### select?

> `optional` **select**: [`CommentSelect`](CommentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9537

Select specific fields to fetch from the Comment

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:9569

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Comments.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:9563

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Comments from the position of the cursor.

***

### where?

> `optional` **where**: [`CommentWhereInput`](CommentWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9545

Filter, which Comment to fetch.

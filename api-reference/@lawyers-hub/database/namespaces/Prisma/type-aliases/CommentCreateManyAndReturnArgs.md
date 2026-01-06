[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CommentCreateManyAndReturnArgs

# Type Alias: CommentCreateManyAndReturnArgs\<ExtArgs\>

> **CommentCreateManyAndReturnArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9653

Comment createManyAndReturn

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`CommentCreateManyInput`](CommentCreateManyInput.md) \| [`CommentCreateManyInput`](CommentCreateManyInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:9661

The data used to create many Comments.

***

### include?

> `optional` **include**: [`CommentIncludeCreateManyAndReturn`](CommentIncludeCreateManyAndReturn.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9666

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CommentSelectCreateManyAndReturn`](CommentSelectCreateManyAndReturn.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:9657

Select specific fields to fetch from the Comment

***

### skipDuplicates?

> `optional` **skipDuplicates**: `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:9662

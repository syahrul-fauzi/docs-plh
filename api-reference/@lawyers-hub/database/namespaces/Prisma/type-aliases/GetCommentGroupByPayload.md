[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetCommentGroupByPayload

# Type Alias: GetCommentGroupByPayload\<T\>

> **GetCommentGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`CommentGroupByOutputType`](CommentGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof CommentGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], CommentGroupByOutputType[P]> : GetScalarType<T[P], CommentGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:8952

## Type Parameters

### T

`T` *extends* [`CommentGroupByArgs`](CommentGroupByArgs.md)

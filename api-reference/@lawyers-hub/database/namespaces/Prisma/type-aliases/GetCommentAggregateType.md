[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetCommentAggregateType

# Type Alias: GetCommentAggregateType\<T\>

> **GetCommentAggregateType**\<`T`\> = \{ \[P in keyof T & keyof
> AggregateComment\]: P extends "\_count" \| "count" ? T\[P\] extends true ?
> number : GetScalarType\<T\[P\], AggregateComment\[P\]\> :
> GetScalarType\<T\[P\], AggregateComment\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:8915

## Type Parameters

### T

`T` _extends_ [`CommentAggregateArgs`](CommentAggregateArgs.md)

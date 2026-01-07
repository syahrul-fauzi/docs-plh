[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetUserAggregateType

# Type Alias: GetUserAggregateType\<T\>

> **GetUserAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateUser\]: P
> extends "\_count" \| "count" ? T\[P\] extends true ? number :
> GetScalarType\<T\[P\], AggregateUser\[P\]\> : GetScalarType\<T\[P\],
> AggregateUser\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:4747

## Type Parameters

### T

`T` _extends_ [`UserAggregateArgs`](UserAggregateArgs.md)

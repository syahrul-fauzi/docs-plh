[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetCaseAggregateType

# Type Alias: GetCaseAggregateType\<T\>

> **GetCaseAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateCase\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregateCase\[P\]\> : GetScalarType\<T\[P\], AggregateCase\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:5826

## Type Parameters

### T

`T` *extends* [`CaseAggregateArgs`](CaseAggregateArgs.md)

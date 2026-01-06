[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetUsageAggregateType

# Type Alias: GetUsageAggregateType\<T\>

> **GetUsageAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateUsage\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregateUsage\[P\]\> : GetScalarType\<T\[P\], AggregateUsage\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:10917

## Type Parameters

### T

`T` *extends* [`UsageAggregateArgs`](UsageAggregateArgs.md)

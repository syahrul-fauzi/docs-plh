[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetAIModelConfigAggregateType

# Type Alias: GetAIModelConfigAggregateType\<T\>

> **GetAIModelConfigAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateAIModelConfig\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregateAIModelConfig\[P\]\> : GetScalarType\<T\[P\], AggregateAIModelConfig\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:14889

## Type Parameters

### T

`T` *extends* [`AIModelConfigAggregateArgs`](AIModelConfigAggregateArgs.md)

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetTemplateVersionAggregateType

# Type Alias: GetTemplateVersionAggregateType\<T\>

> **GetTemplateVersionAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateTemplateVersion\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregateTemplateVersion\[P\]\> : GetScalarType\<T\[P\], AggregateTemplateVersion\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:13866

## Type Parameters

### T

`T` *extends* [`TemplateVersionAggregateArgs`](TemplateVersionAggregateArgs.md)

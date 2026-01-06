[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetDocumentTemplateAggregateType

# Type Alias: GetDocumentTemplateAggregateType\<T\>

> **GetDocumentTemplateAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateDocumentTemplate\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregateDocumentTemplate\[P\]\> : GetScalarType\<T\[P\], AggregateDocumentTemplate\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:12853

## Type Parameters

### T

`T` *extends* [`DocumentTemplateAggregateArgs`](DocumentTemplateAggregateArgs.md)

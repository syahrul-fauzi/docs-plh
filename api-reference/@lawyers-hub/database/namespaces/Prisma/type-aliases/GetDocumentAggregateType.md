[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetDocumentAggregateType

# Type Alias: GetDocumentAggregateType\<T\>

> **GetDocumentAggregateType**\<`T`\> = \{ \[P in keyof T & keyof
> AggregateDocument\]: P extends "\_count" \| "count" ? T\[P\] extends true ?
> number : GetScalarType\<T\[P\], AggregateDocument\[P\]\> :
> GetScalarType\<T\[P\], AggregateDocument\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:6863

## Type Parameters

### T

`T` _extends_ [`DocumentAggregateArgs`](DocumentAggregateArgs.md)

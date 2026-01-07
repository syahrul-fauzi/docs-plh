[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetDraftAggregateType

# Type Alias: GetDraftAggregateType\<T\>

> **GetDraftAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateDraft\]:
> P extends "\_count" \| "count" ? T\[P\] extends true ? number :
> GetScalarType\<T\[P\], AggregateDraft\[P\]\> : GetScalarType\<T\[P\],
> AggregateDraft\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:7887

## Type Parameters

### T

`T` _extends_ [`DraftAggregateArgs`](DraftAggregateArgs.md)

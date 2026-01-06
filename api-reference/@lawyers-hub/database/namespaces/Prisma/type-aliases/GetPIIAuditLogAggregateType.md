[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetPIIAuditLogAggregateType

# Type Alias: GetPIIAuditLogAggregateType\<T\>

> **GetPIIAuditLogAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregatePIIAuditLog\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregatePIIAuditLog\[P\]\> : GetScalarType\<T\[P\], AggregatePIIAuditLog\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:16952

## Type Parameters

### T

`T` *extends* [`PIIAuditLogAggregateArgs`](PIIAuditLogAggregateArgs.md)

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetAuditLogAggregateType

# Type Alias: GetAuditLogAggregateType\<T\>

> **GetAuditLogAggregateType**\<`T`\> = \{ \[P in keyof T & keyof AggregateAuditLog\]: P extends "\_count" \| "count" ? T\[P\] extends true ? number : GetScalarType\<T\[P\], AggregateAuditLog\[P\]\> : GetScalarType\<T\[P\], AggregateAuditLog\[P\]\> \}

Defined in: node\_modules/.prisma/client/index.d.ts:9928

## Type Parameters

### T

`T` *extends* [`AuditLogAggregateArgs`](AuditLogAggregateArgs.md)

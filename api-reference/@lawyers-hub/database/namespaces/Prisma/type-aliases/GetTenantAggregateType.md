[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetTenantAggregateType

# Type Alias: GetTenantAggregateType\<T\>

> **GetTenantAggregateType**\<`T`\> = \{ \[P in keyof T & keyof
> AggregateTenant\]: P extends "\_count" \| "count" ? T\[P\] extends true ?
> number : GetScalarType\<T\[P\], AggregateTenant\[P\]\> :
> GetScalarType\<T\[P\], AggregateTenant\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:2495

## Type Parameters

### T

`T` _extends_ [`TenantAggregateArgs`](TenantAggregateArgs.md)

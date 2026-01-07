[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetSubscriptionAggregateType

# Type Alias: GetSubscriptionAggregateType\<T\>

> **GetSubscriptionAggregateType**\<`T`\> = \{ \[P in keyof T & keyof
> AggregateSubscription\]: P extends "\_count" \| "count" ? T\[P\] extends true
> ? number : GetScalarType\<T\[P\], AggregateSubscription\[P\]\> :
> GetScalarType\<T\[P\], AggregateSubscription\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:3768

## Type Parameters

### T

`T` _extends_ [`SubscriptionAggregateArgs`](SubscriptionAggregateArgs.md)

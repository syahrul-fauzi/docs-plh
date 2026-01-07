[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetSubscriptionGroupByPayload

# Type Alias: GetSubscriptionGroupByPayload\<T\>

> **GetSubscriptionGroupByPayload**\<`T`\> =
> [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`SubscriptionGroupByOutputType`](SubscriptionGroupByOutputType.md),
> `T`\[`"by"`\]\> &
> `{ [P in keyof T & keyof SubscriptionGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], SubscriptionGroupByOutputType[P]> : GetScalarType<T[P], SubscriptionGroupByOutputType[P]> }`[]\>

Defined in: node_modules/.prisma/client/index.d.ts:3811

## Type Parameters

### T

`T` _extends_ [`SubscriptionGroupByArgs`](SubscriptionGroupByArgs.md)

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetUsageGroupByPayload

# Type Alias: GetUsageGroupByPayload\<T\>

> **GetUsageGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`UsageGroupByOutputType`](UsageGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof UsageGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], UsageGroupByOutputType[P]> : GetScalarType<T[P], UsageGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:10956

## Type Parameters

### T

`T` *extends* [`UsageGroupByArgs`](UsageGroupByArgs.md)

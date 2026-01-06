[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetDraftGroupByPayload

# Type Alias: GetDraftGroupByPayload\<T\>

> **GetDraftGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`DraftGroupByOutputType`](DraftGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof DraftGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], DraftGroupByOutputType[P]> : GetScalarType<T[P], DraftGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:7926

## Type Parameters

### T

`T` *extends* [`DraftGroupByArgs`](DraftGroupByArgs.md)

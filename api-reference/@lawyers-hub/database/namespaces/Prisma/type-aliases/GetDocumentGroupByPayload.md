[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetDocumentGroupByPayload

# Type Alias: GetDocumentGroupByPayload\<T\>

> **GetDocumentGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`DocumentGroupByOutputType`](DocumentGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof DocumentGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], DocumentGroupByOutputType[P]> : GetScalarType<T[P], DocumentGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:6900

## Type Parameters

### T

`T` *extends* [`DocumentGroupByArgs`](DocumentGroupByArgs.md)

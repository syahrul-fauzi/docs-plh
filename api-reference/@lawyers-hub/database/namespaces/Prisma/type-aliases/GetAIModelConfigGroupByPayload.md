[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetAIModelConfigGroupByPayload

# Type Alias: GetAIModelConfigGroupByPayload\<T\>

> **GetAIModelConfigGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`AIModelConfigGroupByOutputType`](AIModelConfigGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof AIModelConfigGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], AIModelConfigGroupByOutputType[P]> : GetScalarType<T[P], AIModelConfigGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:14934

## Type Parameters

### T

`T` *extends* [`AIModelConfigGroupByArgs`](AIModelConfigGroupByArgs.md)

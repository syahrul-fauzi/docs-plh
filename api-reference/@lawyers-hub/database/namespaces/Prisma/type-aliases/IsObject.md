[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / IsObject

# Type Alias: IsObject\<T\>

> **IsObject**\<`T`\> = `T` *extends* `any`[] ? [`False`](False.md) : `T` *extends* `Date` ? [`False`](False.md) : `T` *extends* `Uint8Array` ? [`False`](False.md) : `T` *extends* `BigInt` ? [`False`](False.md) : `T` *extends* `object` ? [`True`](True.md) : [`False`](False.md)

Defined in: node\_modules/.prisma/client/index.d.ts:595

Is T a Record?

## Type Parameters

### T

`T` *extends* `any`

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / IsObject

# Type Alias: IsObject\<T\>

> **IsObject**\<`T`\> = `T` _extends_ `any`[] ? [`False`](False.md) : `T`
> _extends_ `Date` ? [`False`](False.md) : `T` _extends_ `Uint8Array` ?
> [`False`](False.md) : `T` _extends_ `BigInt` ? [`False`](False.md) : `T`
> _extends_ `object` ? [`True`](True.md) : [`False`](False.md)

Defined in: node_modules/.prisma/client/index.d.ts:595

Is T a Record?

## Type Parameters

### T

`T` _extends_ `any`

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PickEnumerable

# Type Alias: PickEnumerable\<T, K\>

> **PickEnumerable**\<`T`, `K`\> = [`Prisma__Pick`](Prisma__Pick.md)\<`T`, [`MaybeTupleToUnion`](MaybeTupleToUnion.md)\<`K`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:791

Like `Pick`, but additionally can also accept an array of keys

## Type Parameters

### T

`T`

### K

`K` *extends* [`Enumerable`](Enumerable.md)\<keyof `T`\> \| keyof `T`

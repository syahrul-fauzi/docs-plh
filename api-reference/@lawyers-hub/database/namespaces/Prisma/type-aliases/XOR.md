[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / XOR

# Type Alias: XOR\<T, U\>

> **XOR**\<`T`, `U`\> = `T` _extends_ `object` ? `U` _extends_ `object` ?
> [`Without`](Without.md)\<`T`, `U`\> & `U` \| [`Without`](Without.md)\<`U`,
> `T`\> & `T` : `U` : `T`

Defined in: node_modules/.prisma/client/index.d.ts:585

XOR is needed to have a real mutually exclusive union type
<https://stackoverflow.com/questions/42123407/does-typescript-support-mutually-exclusive-types>

## Type Parameters

### T

`T`

### U

`U`

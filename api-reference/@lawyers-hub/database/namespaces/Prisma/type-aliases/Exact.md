[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Exact

# Type Alias: Exact\<A, W\>

> **Exact**\<`A`, `W`\> = `A` _extends_ `unknown` ? `W` _extends_ `A` ?
> `{ [K in keyof A]: Exact<A[K], W[K]> }` : `W` : `never` \| `A` _extends_
> `Narrowable` ? `A` : `never`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:1214

## Type Parameters

### A

`A`

### W

`W`

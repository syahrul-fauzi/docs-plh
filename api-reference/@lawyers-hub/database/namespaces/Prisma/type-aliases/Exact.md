[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Exact

# Type Alias: Exact\<A, W\>

> **Exact**\<`A`, `W`\> = `A` *extends* `unknown` ? `W` *extends* `A` ? `{ [K in keyof A]: Exact<A[K], W[K]> }` : `W` : `never` \| `A` *extends* `Narrowable` ? `A` : `never`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:1214

## Type Parameters

### A

`A`

### W

`W`

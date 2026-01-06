[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Subset

# Type Alias: Subset\<T, U\>

> **Subset**\<`T`, `U`\> = `{ [key in keyof T]: key extends keyof U ? T[key] : never }`

Defined in: node\_modules/.prisma/client/index.d.ts:552

Subset

## Type Parameters

### T

`T`

### U

`U`

## Desc

From `T` pick properties that exist in `U`. Simple version of Intersection

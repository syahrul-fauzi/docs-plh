[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / SubsetIntersection

# Type Alias: SubsetIntersection\<T, U, K\>

> **SubsetIntersection**\<`T`, `U`, `K`\> = `{ [key in keyof T]: key extends keyof U ? T[key] : never }` & `K`

Defined in: node\_modules/.prisma/client/index.d.ts:574

Subset + Intersection

## Type Parameters

### T

`T`

### U

`U`

### K

`K`

## Desc

From `T` pick properties that exist in `U` and intersect `K`

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
Prisma\_\_Pick

# Type Alias: Prisma\_\_Pick\<T, K\>

> **Prisma\_\_Pick**\<`T`, `K`\> = `{ [P in K]: T[P] }`

Defined in: node_modules/.prisma/client/index.d.ts:531

From T, pick a set of properties whose keys are in the union K

## Type Parameters

### T

`T`

### K

`K` _extends_ keyof `T`

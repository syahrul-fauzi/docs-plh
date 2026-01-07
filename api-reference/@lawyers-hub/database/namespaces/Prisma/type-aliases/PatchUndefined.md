[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PatchUndefined

# Type Alias: PatchUndefined\<O, O1\>

> **PatchUndefined**\<`O`, `O1`\> =
> `{ [K in keyof O]: O[K] extends undefined ? At<O1, K> : O[K] }` & `object`

Defined in: node_modules/.prisma/client/index.d.ts:644

## Type Parameters

### O

`O` _extends_ `object`

### O1

`O1` _extends_ `object`

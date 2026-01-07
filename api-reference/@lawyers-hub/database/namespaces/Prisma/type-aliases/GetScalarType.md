[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetScalarType

# Type Alias: GetScalarType\<T, O\>

> **GetScalarType**\<`T`, `O`\> = `O` _extends_ `object` ?
> `{ [P in keyof T]: P extends keyof O ? O[P] : never }` : `never`

Defined in: node_modules/.prisma/client/index.d.ts:754

Used by group by

## Type Parameters

### T

`T`

### O

`O`

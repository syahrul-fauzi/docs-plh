[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SelectSubset

# Type Alias: SelectSubset\<T, U\>

> **SelectSubset**\<`T`, `U`\> =
> `{ [key in keyof T]: key extends keyof U ? T[key] : never }` & `T` _extends_
> [`SelectAndInclude`](SelectAndInclude.md) ?
> ``"Please either choose `select` or `include`."`` : `T` _extends_
> [`SelectAndOmit`](SelectAndOmit.md) ?
> ``"Please either choose `select` or `omit`."`` : `object`

Defined in: node_modules/.prisma/client/index.d.ts:561

SelectSubset

## Type Parameters

### T

`T`

### U

`U`

## Desc

From `T` pick properties that exist in `U`. Simple version of Intersection.
Additionally, it validates, if both select and include are present. If the case,
it errors.

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Overwrite

# Type Alias: Overwrite\<O, O1\>

> **Overwrite**\<`O`, `O1`\> = `{ [K in keyof O]: K extends keyof O1 ? O1[K] : O[K] }` & `object`

Defined in: node\_modules/.prisma/client/index.d.ts:655

## Type Parameters

### O

`O` *extends* `object`

### O1

`O1` *extends* `object`

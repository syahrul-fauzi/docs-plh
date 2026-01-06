[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / \_\_Either

# Type Alias: \_\_Either\<O, K\>

> **\_\_Either**\<`O`, `K`\> = `Omit`\<`O`, `K`\> & `{ [P in K]: Prisma__Pick<O, P & keyof O> }`\[`K`\]

Defined in: node\_modules/.prisma/client/index.d.ts:617

From ts-toolbelt

## Type Parameters

### O

`O` *extends* `object`

### K

`K` *extends* [`Key`](Key.md)

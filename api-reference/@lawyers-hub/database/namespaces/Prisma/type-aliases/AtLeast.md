[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AtLeast

# Type Alias: AtLeast\<O, K\>

> **AtLeast**\<`O`, `K`\> = [`NoExpand`](NoExpand.md)\<`O` *extends* `unknown` ? `K` *extends* keyof `O` ? `{ [P in K]: O[P] }` & `O` : `O` \| `{ [P in keyof O as P extends K ? K : never]-?: O[P] }` & `O` : `never`\>

Defined in: node\_modules/.prisma/client/index.d.ts:688

## Type Parameters

### O

`O` *extends* `object`

### K

`K` *extends* `string`

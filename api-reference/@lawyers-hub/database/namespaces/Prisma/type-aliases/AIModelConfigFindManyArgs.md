[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AIModelConfigFindManyArgs

# Type Alias: AIModelConfigFindManyArgs\<ExtArgs\>

> **AIModelConfigFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:15538

AIModelConfig findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`AIModelConfigWhereUniqueInput`](AIModelConfigWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:15558

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing AIModelConfigs.

***

### distinct?

> `optional` **distinct**: [`AIModelConfigScalarFieldEnum`](AIModelConfigScalarFieldEnum.md) \| [`AIModelConfigScalarFieldEnum`](AIModelConfigScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:15571

***

### orderBy?

> `optional` **orderBy**: [`AIModelConfigOrderByWithRelationInput`](AIModelConfigOrderByWithRelationInput.md) \| [`AIModelConfigOrderByWithRelationInput`](AIModelConfigOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:15552

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of AIModelConfigs to fetch.

***

### select?

> `optional` **select**: [`AIModelConfigSelect`](AIModelConfigSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:15542

Select specific fields to fetch from the AIModelConfig

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:15570

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` AIModelConfigs.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:15564

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` AIModelConfigs from the position of the cursor.

***

### where?

> `optional` **where**: [`AIModelConfigWhereInput`](AIModelConfigWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:15546

Filter, which AIModelConfigs to fetch.

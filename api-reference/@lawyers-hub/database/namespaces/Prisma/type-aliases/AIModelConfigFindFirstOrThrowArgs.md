[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AIModelConfigFindFirstOrThrowArgs

# Type Alias: AIModelConfigFindFirstOrThrowArgs\<ExtArgs\>

> **AIModelConfigFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:15494

AIModelConfig findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`AIModelConfigWhereUniqueInput`](AIModelConfigWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:15514

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for AIModelConfigs.

---

### distinct?

> `optional` **distinct**:
> [`AIModelConfigScalarFieldEnum`](AIModelConfigScalarFieldEnum.md) \|
> [`AIModelConfigScalarFieldEnum`](AIModelConfigScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:15532

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of AIModelConfigs.

---

### orderBy?

> `optional` **orderBy**:
> [`AIModelConfigOrderByWithRelationInput`](AIModelConfigOrderByWithRelationInput.md)
> \|
> [`AIModelConfigOrderByWithRelationInput`](AIModelConfigOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:15508

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of AIModelConfigs to fetch.

---

### select?

> `optional` **select**:
> [`AIModelConfigSelect`](AIModelConfigSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:15498

Select specific fields to fetch from the AIModelConfig

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:15526

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` AIModelConfigs.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:15520

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` AIModelConfigs from the position of the cursor.

---

### where?

> `optional` **where**: [`AIModelConfigWhereInput`](AIModelConfigWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:15502

Filter, which AIModelConfig to fetch.

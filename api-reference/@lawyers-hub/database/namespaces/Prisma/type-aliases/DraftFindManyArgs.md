[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DraftFindManyArgs

# Type Alias: DraftFindManyArgs\<ExtArgs\>

> **DraftFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:8559

Draft findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`DraftWhereUniqueInput`](DraftWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8583

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Drafts.

***

### distinct?

> `optional` **distinct**: [`DraftScalarFieldEnum`](DraftScalarFieldEnum.md) \| [`DraftScalarFieldEnum`](DraftScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:8596

***

### include?

> `optional` **include**: [`DraftInclude`](DraftInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:8567

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`DraftOrderByWithRelationInput`](DraftOrderByWithRelationInput.md) \| [`DraftOrderByWithRelationInput`](DraftOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:8577

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Drafts to fetch.

***

### select?

> `optional` **select**: [`DraftSelect`](DraftSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:8563

Select specific fields to fetch from the Draft

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:8595

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Drafts.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:8589

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Drafts from the position of the cursor.

***

### where?

> `optional` **where**: [`DraftWhereInput`](DraftWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8571

Filter, which Drafts to fetch.

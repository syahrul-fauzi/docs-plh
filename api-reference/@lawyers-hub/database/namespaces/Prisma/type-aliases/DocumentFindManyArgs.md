[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentFindManyArgs

# Type Alias: DocumentFindManyArgs\<ExtArgs\>

> **DocumentFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:7523

Document findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:7547

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Documents.

***

### distinct?

> `optional` **distinct**: [`DocumentScalarFieldEnum`](DocumentScalarFieldEnum.md) \| [`DocumentScalarFieldEnum`](DocumentScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:7560

***

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:7531

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md) \| [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:7541

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Documents to fetch.

***

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:7527

Select specific fields to fetch from the Document

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:7559

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Documents.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:7553

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Documents from the position of the cursor.

***

### where?

> `optional` **where**: [`DocumentWhereInput`](DocumentWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:7535

Filter, which Documents to fetch.

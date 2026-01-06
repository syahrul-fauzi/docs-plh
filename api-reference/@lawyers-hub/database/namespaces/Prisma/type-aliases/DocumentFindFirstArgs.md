[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentFindFirstArgs

# Type Alias: DocumentFindFirstArgs\<ExtArgs\>

> **DocumentFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:7427

Document findFirst

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:7451

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Documents.

***

### distinct?

> `optional` **distinct**: [`DocumentScalarFieldEnum`](DocumentScalarFieldEnum.md) \| [`DocumentScalarFieldEnum`](DocumentScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:7469

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Documents.

***

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:7435

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md) \| [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:7445

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Documents to fetch.

***

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:7431

Select specific fields to fetch from the Document

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:7463

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Documents.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:7457

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Documents from the position of the cursor.

***

### where?

> `optional` **where**: [`DocumentWhereInput`](DocumentWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:7439

Filter, which Document to fetch.

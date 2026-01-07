[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentFindFirstOrThrowArgs

# Type Alias: DocumentFindFirstOrThrowArgs\<ExtArgs\>

> **DocumentFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:7475

Document findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`DocumentWhereUniqueInput`](DocumentWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7499

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Documents.

---

### distinct?

> `optional` **distinct**:
> [`DocumentScalarFieldEnum`](DocumentScalarFieldEnum.md) \|
> [`DocumentScalarFieldEnum`](DocumentScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:7517

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Documents.

---

### include?

> `optional` **include**: [`DocumentInclude`](DocumentInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:7483

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md) \|
> [`DocumentOrderByWithRelationInput`](DocumentOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:7493

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Documents to fetch.

---

### select?

> `optional` **select**: [`DocumentSelect`](DocumentSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:7479

Select specific fields to fetch from the Document

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:7511

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Documents.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:7505

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Documents from the position of the cursor.

---

### where?

> `optional` **where**: [`DocumentWhereInput`](DocumentWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:7487

Filter, which Document to fetch.

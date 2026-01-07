[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DraftFindFirstArgs

# Type Alias: DraftFindFirstArgs\<ExtArgs\>

> **DraftFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:8463

Draft findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`DraftWhereUniqueInput`](DraftWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:8487

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Drafts.

---

### distinct?

> `optional` **distinct**: [`DraftScalarFieldEnum`](DraftScalarFieldEnum.md) \|
> [`DraftScalarFieldEnum`](DraftScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:8505

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Drafts.

---

### include?

> `optional` **include**: [`DraftInclude`](DraftInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:8471

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`DraftOrderByWithRelationInput`](DraftOrderByWithRelationInput.md) \|
> [`DraftOrderByWithRelationInput`](DraftOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:8481

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Drafts to fetch.

---

### select?

> `optional` **select**: [`DraftSelect`](DraftSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:8467

Select specific fields to fetch from the Draft

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:8499

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Drafts.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:8493

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Drafts from the position of the cursor.

---

### where?

> `optional` **where**: [`DraftWhereInput`](DraftWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:8475

Filter, which Draft to fetch.

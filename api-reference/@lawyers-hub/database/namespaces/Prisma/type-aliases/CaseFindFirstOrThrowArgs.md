[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseFindFirstOrThrowArgs

# Type Alias: CaseFindFirstOrThrowArgs\<ExtArgs\>

> **CaseFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:6434

Case findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:6458

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Cases.

---

### distinct?

> `optional` **distinct**: [`CaseScalarFieldEnum`](CaseScalarFieldEnum.md) \|
> [`CaseScalarFieldEnum`](CaseScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:6476

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Cases.

---

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:6442

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`CaseOrderByWithRelationInput`](CaseOrderByWithRelationInput.md) \|
> [`CaseOrderByWithRelationInput`](CaseOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:6452

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Cases to fetch.

---

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:6438

Select specific fields to fetch from the Case

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:6470

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Cases.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:6464

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Cases from the position of the cursor.

---

### where?

> `optional` **where**: [`CaseWhereInput`](CaseWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:6446

Filter, which Case to fetch.

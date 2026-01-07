[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseFindUniqueOrThrowArgs

# Type Alias: CaseFindUniqueOrThrowArgs\<ExtArgs\>

> **CaseFindUniqueOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:6368

Case findUniqueOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:6376

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:6372

Select specific fields to fetch from the Case

---

### where

> **where**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:6380

Filter, which Case to fetch.

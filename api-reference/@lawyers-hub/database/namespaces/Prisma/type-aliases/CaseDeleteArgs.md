[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CaseDeleteArgs

# Type Alias: CaseDeleteArgs\<ExtArgs\>

> **CaseDeleteArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:6635

Case delete

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6643

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6639

Select specific fields to fetch from the Case

***

### where

> **where**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6647

Filter which Case to delete.

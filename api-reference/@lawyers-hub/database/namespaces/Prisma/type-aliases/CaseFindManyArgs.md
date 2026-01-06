[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / CaseFindManyArgs

# Type Alias: CaseFindManyArgs\<ExtArgs\>

> **CaseFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:6482

Case findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`CaseWhereUniqueInput`](CaseWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6506

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Cases.

***

### distinct?

> `optional` **distinct**: [`CaseScalarFieldEnum`](CaseScalarFieldEnum.md) \| [`CaseScalarFieldEnum`](CaseScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:6519

***

### include?

> `optional` **include**: [`CaseInclude`](CaseInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6490

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`CaseOrderByWithRelationInput`](CaseOrderByWithRelationInput.md) \| [`CaseOrderByWithRelationInput`](CaseOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:6500

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Cases to fetch.

***

### select?

> `optional` **select**: [`CaseSelect`](CaseSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:6486

Select specific fields to fetch from the Case

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:6518

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Cases.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:6512

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Cases from the position of the cursor.

***

### where?

> `optional` **where**: [`CaseWhereInput`](CaseWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:6494

Filter, which Cases to fetch.

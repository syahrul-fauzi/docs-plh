[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentTemplateFindFirstOrThrowArgs

# Type Alias: DocumentTemplateFindFirstOrThrowArgs\<ExtArgs\>

> **DocumentTemplateFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:13453

DocumentTemplate findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`DocumentTemplateWhereUniqueInput`](DocumentTemplateWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13477

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for DocumentTemplates.

***

### distinct?

> `optional` **distinct**: [`DocumentTemplateScalarFieldEnum`](DocumentTemplateScalarFieldEnum.md) \| [`DocumentTemplateScalarFieldEnum`](DocumentTemplateScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:13495

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of DocumentTemplates.

***

### include?

> `optional` **include**: [`DocumentTemplateInclude`](DocumentTemplateInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:13461

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md) \| [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:13471

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of DocumentTemplates to fetch.

***

### select?

> `optional` **select**: [`DocumentTemplateSelect`](DocumentTemplateSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:13457

Select specific fields to fetch from the DocumentTemplate

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:13489

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` DocumentTemplates.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:13483

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` DocumentTemplates from the position of the cursor.

***

### where?

> `optional` **where**: [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13465

Filter, which DocumentTemplate to fetch.

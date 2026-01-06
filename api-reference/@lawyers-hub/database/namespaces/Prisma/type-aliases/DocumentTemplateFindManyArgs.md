[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentTemplateFindManyArgs

# Type Alias: DocumentTemplateFindManyArgs\<ExtArgs\>

> **DocumentTemplateFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:13501

DocumentTemplate findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`DocumentTemplateWhereUniqueInput`](DocumentTemplateWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13525

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing DocumentTemplates.

***

### distinct?

> `optional` **distinct**: [`DocumentTemplateScalarFieldEnum`](DocumentTemplateScalarFieldEnum.md) \| [`DocumentTemplateScalarFieldEnum`](DocumentTemplateScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:13538

***

### include?

> `optional` **include**: [`DocumentTemplateInclude`](DocumentTemplateInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:13509

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md) \| [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:13519

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of DocumentTemplates to fetch.

***

### select?

> `optional` **select**: [`DocumentTemplateSelect`](DocumentTemplateSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:13505

Select specific fields to fetch from the DocumentTemplate

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:13537

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` DocumentTemplates.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:13531

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` DocumentTemplates from the position of the cursor.

***

### where?

> `optional` **where**: [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13513

Filter, which DocumentTemplates to fetch.

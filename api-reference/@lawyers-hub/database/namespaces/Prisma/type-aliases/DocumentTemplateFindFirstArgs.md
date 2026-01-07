[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentTemplateFindFirstArgs

# Type Alias: DocumentTemplateFindFirstArgs\<ExtArgs\>

> **DocumentTemplateFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:13405

DocumentTemplate findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`DocumentTemplateWhereUniqueInput`](DocumentTemplateWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:13429

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for DocumentTemplates.

---

### distinct?

> `optional` **distinct**:
> [`DocumentTemplateScalarFieldEnum`](DocumentTemplateScalarFieldEnum.md) \|
> [`DocumentTemplateScalarFieldEnum`](DocumentTemplateScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:13447

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of DocumentTemplates.

---

### include?

> `optional` **include**:
> [`DocumentTemplateInclude`](DocumentTemplateInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:13413

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md)
> \|
> [`DocumentTemplateOrderByWithRelationInput`](DocumentTemplateOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:13423

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of DocumentTemplates to fetch.

---

### select?

> `optional` **select**:
> [`DocumentTemplateSelect`](DocumentTemplateSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:13409

Select specific fields to fetch from the DocumentTemplate

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:13441

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` DocumentTemplates.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:13435

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` DocumentTemplates from the position of the cursor.

---

### where?

> `optional` **where**:
> [`DocumentTemplateWhereInput`](DocumentTemplateWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:13417

Filter, which DocumentTemplate to fetch.

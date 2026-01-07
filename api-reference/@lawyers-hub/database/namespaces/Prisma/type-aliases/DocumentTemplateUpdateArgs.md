[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentTemplateUpdateArgs

# Type Alias: DocumentTemplateUpdateArgs\<ExtArgs\>

> **DocumentTemplateUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:13592

DocumentTemplate update

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`DocumentTemplateUpdateInput`](DocumentTemplateUpdateInput.md),
> [`DocumentTemplateUncheckedUpdateInput`](DocumentTemplateUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:13604

The data needed to update a DocumentTemplate.

---

### include?

> `optional` **include**:
> [`DocumentTemplateInclude`](DocumentTemplateInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:13600

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`DocumentTemplateSelect`](DocumentTemplateSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:13596

Select specific fields to fetch from the DocumentTemplate

---

### where

> **where**:
> [`DocumentTemplateWhereUniqueInput`](DocumentTemplateWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:13608

Choose, which DocumentTemplate to update.

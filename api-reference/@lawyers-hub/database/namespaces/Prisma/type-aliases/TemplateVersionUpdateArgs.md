[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TemplateVersionUpdateArgs

# Type Alias: TemplateVersionUpdateArgs\<ExtArgs\>

> **TemplateVersionUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:14609

TemplateVersion update

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`TemplateVersionUpdateInput`](TemplateVersionUpdateInput.md),
> [`TemplateVersionUncheckedUpdateInput`](TemplateVersionUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:14621

The data needed to update a TemplateVersion.

---

### include?

> `optional` **include**:
> [`TemplateVersionInclude`](TemplateVersionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14617

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`TemplateVersionSelect`](TemplateVersionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14613

Select specific fields to fetch from the TemplateVersion

---

### where

> **where**:
> [`TemplateVersionWhereUniqueInput`](TemplateVersionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14625

Choose, which TemplateVersion to update.

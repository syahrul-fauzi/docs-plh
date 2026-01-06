[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TemplateVersionCreateArgs

# Type Alias: TemplateVersionCreateArgs\<ExtArgs\>

> **TemplateVersionCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:14561

TemplateVersion create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`TemplateVersionCreateInput`](TemplateVersionCreateInput.md), [`TemplateVersionUncheckedCreateInput`](TemplateVersionUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:14573

The data needed to create a TemplateVersion.

***

### include?

> `optional` **include**: [`TemplateVersionInclude`](TemplateVersionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:14569

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`TemplateVersionSelect`](TemplateVersionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:14565

Select specific fields to fetch from the TemplateVersion

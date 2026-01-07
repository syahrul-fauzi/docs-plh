[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TemplateVersionUpsertArgs

# Type Alias: TemplateVersionUpsertArgs\<ExtArgs\>

> **TemplateVersionUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:14645

TemplateVersion upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**:
> [`XOR`](XOR.md)\<[`TemplateVersionCreateInput`](TemplateVersionCreateInput.md),
> [`TemplateVersionUncheckedCreateInput`](TemplateVersionUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:14661

In case the TemplateVersion found by the `where` argument doesn't exist, create
a new TemplateVersion with this data.

---

### include?

> `optional` **include**:
> [`TemplateVersionInclude`](TemplateVersionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14653

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`TemplateVersionSelect`](TemplateVersionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14649

Select specific fields to fetch from the TemplateVersion

---

### update

> **update**:
> [`XOR`](XOR.md)\<[`TemplateVersionUpdateInput`](TemplateVersionUpdateInput.md),
> [`TemplateVersionUncheckedUpdateInput`](TemplateVersionUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:14665

In case the TemplateVersion was found with the provided `where` argument, update
it with this data.

---

### where

> **where**:
> [`TemplateVersionWhereUniqueInput`](TemplateVersionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14657

The filter to search for the TemplateVersion to update in case it exists.

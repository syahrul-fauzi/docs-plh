[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentTemplateUpsertArgs

# Type Alias: DocumentTemplateUpsertArgs\<ExtArgs\>

> **DocumentTemplateUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:13628

DocumentTemplate upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**:
> [`XOR`](XOR.md)\<[`DocumentTemplateCreateInput`](DocumentTemplateCreateInput.md),
> [`DocumentTemplateUncheckedCreateInput`](DocumentTemplateUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:13644

In case the DocumentTemplate found by the `where` argument doesn't exist, create
a new DocumentTemplate with this data.

---

### include?

> `optional` **include**:
> [`DocumentTemplateInclude`](DocumentTemplateInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:13636

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`DocumentTemplateSelect`](DocumentTemplateSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:13632

Select specific fields to fetch from the DocumentTemplate

---

### update

> **update**:
> [`XOR`](XOR.md)\<[`DocumentTemplateUpdateInput`](DocumentTemplateUpdateInput.md),
> [`DocumentTemplateUncheckedUpdateInput`](DocumentTemplateUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:13648

In case the DocumentTemplate was found with the provided `where` argument,
update it with this data.

---

### where

> **where**:
> [`DocumentTemplateWhereUniqueInput`](DocumentTemplateWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:13640

The filter to search for the DocumentTemplate to update in case it exists.

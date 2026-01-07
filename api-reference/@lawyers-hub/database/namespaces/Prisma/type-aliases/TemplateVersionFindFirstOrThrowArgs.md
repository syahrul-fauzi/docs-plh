[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TemplateVersionFindFirstOrThrowArgs

# Type Alias: TemplateVersionFindFirstOrThrowArgs\<ExtArgs\>

> **TemplateVersionFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:14470

TemplateVersion findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`TemplateVersionWhereUniqueInput`](TemplateVersionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14494

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for TemplateVersions.

---

### distinct?

> `optional` **distinct**:
> [`TemplateVersionScalarFieldEnum`](TemplateVersionScalarFieldEnum.md) \|
> [`TemplateVersionScalarFieldEnum`](TemplateVersionScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:14512

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of TemplateVersions.

---

### include?

> `optional` **include**:
> [`TemplateVersionInclude`](TemplateVersionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14478

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`TemplateVersionOrderByWithRelationInput`](TemplateVersionOrderByWithRelationInput.md)
> \|
> [`TemplateVersionOrderByWithRelationInput`](TemplateVersionOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:14488

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of TemplateVersions to fetch.

---

### select?

> `optional` **select**:
> [`TemplateVersionSelect`](TemplateVersionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14474

Select specific fields to fetch from the TemplateVersion

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:14506

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` TemplateVersions.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:14500

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` TemplateVersions from the position of the cursor.

---

### where?

> `optional` **where**:
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14482

Filter, which TemplateVersion to fetch.

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TemplateVersionFindFirstArgs

# Type Alias: TemplateVersionFindFirstArgs\<ExtArgs\>

> **TemplateVersionFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:14422

TemplateVersion findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`TemplateVersionWhereUniqueInput`](TemplateVersionWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14446

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for TemplateVersions.

---

### distinct?

> `optional` **distinct**:
> [`TemplateVersionScalarFieldEnum`](TemplateVersionScalarFieldEnum.md) \|
> [`TemplateVersionScalarFieldEnum`](TemplateVersionScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:14464

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of TemplateVersions.

---

### include?

> `optional` **include**:
> [`TemplateVersionInclude`](TemplateVersionInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14430

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`TemplateVersionOrderByWithRelationInput`](TemplateVersionOrderByWithRelationInput.md)
> \|
> [`TemplateVersionOrderByWithRelationInput`](TemplateVersionOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:14440

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of TemplateVersions to fetch.

---

### select?

> `optional` **select**:
> [`TemplateVersionSelect`](TemplateVersionSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:14426

Select specific fields to fetch from the TemplateVersion

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:14458

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` TemplateVersions.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:14452

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` TemplateVersions from the position of the cursor.

---

### where?

> `optional` **where**:
> [`TemplateVersionWhereInput`](TemplateVersionWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:14434

Filter, which TemplateVersion to fetch.

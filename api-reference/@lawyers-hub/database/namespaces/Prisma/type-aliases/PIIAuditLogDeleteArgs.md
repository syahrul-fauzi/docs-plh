[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogDeleteArgs

# Type Alias: PIIAuditLogDeleteArgs\<ExtArgs\>

> **PIIAuditLogDeleteArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17787

PIIAuditLog delete

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17795

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17791

Select specific fields to fetch from the PIIAuditLog

---

### where

> **where**: [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17799

Filter which PIIAuditLog to delete.

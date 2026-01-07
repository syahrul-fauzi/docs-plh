[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogUpdateArgs

# Type Alias: PIIAuditLogUpdateArgs\<ExtArgs\>

> **PIIAuditLogUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17725

PIIAuditLog update

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`PIIAuditLogUpdateInput`](PIIAuditLogUpdateInput.md),
> [`PIIAuditLogUncheckedUpdateInput`](PIIAuditLogUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17737

The data needed to update a PIIAuditLog.

---

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17733

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17729

Select specific fields to fetch from the PIIAuditLog

---

### where

> **where**: [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17741

Choose, which PIIAuditLog to update.

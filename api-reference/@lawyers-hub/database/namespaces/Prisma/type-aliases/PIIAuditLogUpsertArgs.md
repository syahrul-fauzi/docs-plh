[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogUpsertArgs

# Type Alias: PIIAuditLogUpsertArgs\<ExtArgs\>

> **PIIAuditLogUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17761

PIIAuditLog upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**:
> [`XOR`](XOR.md)\<[`PIIAuditLogCreateInput`](PIIAuditLogCreateInput.md),
> [`PIIAuditLogUncheckedCreateInput`](PIIAuditLogUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17777

In case the PIIAuditLog found by the `where` argument doesn't exist, create a
new PIIAuditLog with this data.

---

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17769

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17765

Select specific fields to fetch from the PIIAuditLog

---

### update

> **update**:
> [`XOR`](XOR.md)\<[`PIIAuditLogUpdateInput`](PIIAuditLogUpdateInput.md),
> [`PIIAuditLogUncheckedUpdateInput`](PIIAuditLogUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17781

In case the PIIAuditLog was found with the provided `where` argument, update it
with this data.

---

### where

> **where**: [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17773

The filter to search for the PIIAuditLog to update in case it exists.

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogCreateArgs

# Type Alias: PIIAuditLogCreateArgs\<ExtArgs\>

> **PIIAuditLogCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17677

PIIAuditLog create

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`PIIAuditLogCreateInput`](PIIAuditLogCreateInput.md),
> [`PIIAuditLogUncheckedCreateInput`](PIIAuditLogUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17689

The data needed to create a PIIAuditLog.

---

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17685

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17681

Select specific fields to fetch from the PIIAuditLog

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogCreateArgs

# Type Alias: AuditLogCreateArgs\<ExtArgs\>

> **AuditLogCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10625

AuditLog create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`AuditLogCreateInput`](AuditLogCreateInput.md), [`AuditLogUncheckedCreateInput`](AuditLogUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:10637

The data needed to create a AuditLog.

***

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10633

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10629

Select specific fields to fetch from the AuditLog

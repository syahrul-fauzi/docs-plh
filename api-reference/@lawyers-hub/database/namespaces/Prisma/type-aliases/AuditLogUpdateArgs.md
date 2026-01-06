[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogUpdateArgs

# Type Alias: AuditLogUpdateArgs\<ExtArgs\>

> **AuditLogUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10673

AuditLog update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`AuditLogUpdateInput`](AuditLogUpdateInput.md), [`AuditLogUncheckedUpdateInput`](AuditLogUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:10685

The data needed to update a AuditLog.

***

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10681

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10677

Select specific fields to fetch from the AuditLog

***

### where

> **where**: [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:10689

Choose, which AuditLog to update.

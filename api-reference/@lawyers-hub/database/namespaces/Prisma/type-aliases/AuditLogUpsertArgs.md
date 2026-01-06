[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogUpsertArgs

# Type Alias: AuditLogUpsertArgs\<ExtArgs\>

> **AuditLogUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10709

AuditLog upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`AuditLogCreateInput`](AuditLogCreateInput.md), [`AuditLogUncheckedCreateInput`](AuditLogUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:10725

In case the AuditLog found by the `where` argument doesn't exist, create a new AuditLog with this data.

***

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10717

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10713

Select specific fields to fetch from the AuditLog

***

### update

> **update**: [`XOR`](XOR.md)\<[`AuditLogUpdateInput`](AuditLogUpdateInput.md), [`AuditLogUncheckedUpdateInput`](AuditLogUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:10729

In case the AuditLog was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:10721

The filter to search for the AuditLog to update in case it exists.

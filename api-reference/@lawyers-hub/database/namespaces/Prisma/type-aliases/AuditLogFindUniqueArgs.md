[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogFindUniqueArgs

# Type Alias: AuditLogFindUniqueArgs\<ExtArgs\>

> **AuditLogFindUniqueArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10450

AuditLog findUnique

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10458

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10454

Select specific fields to fetch from the AuditLog

***

### where

> **where**: [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:10462

Filter, which AuditLog to fetch.

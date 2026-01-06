[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogFindUniqueOrThrowArgs

# Type Alias: AuditLogFindUniqueOrThrowArgs\<ExtArgs\>

> **AuditLogFindUniqueOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10468

AuditLog findUniqueOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10476

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10472

Select specific fields to fetch from the AuditLog

***

### where

> **where**: [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:10480

Filter, which AuditLog to fetch.

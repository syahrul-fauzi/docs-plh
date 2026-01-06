[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogCreateManyAndReturnArgs

# Type Alias: AuditLogCreateManyAndReturnArgs\<ExtArgs\>

> **AuditLogCreateManyAndReturnArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10654

AuditLog createManyAndReturn

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`AuditLogCreateManyInput`](AuditLogCreateManyInput.md) \| [`AuditLogCreateManyInput`](AuditLogCreateManyInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:10662

The data used to create many AuditLogs.

***

### include?

> `optional` **include**: [`AuditLogIncludeCreateManyAndReturn`](AuditLogIncludeCreateManyAndReturn.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10667

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`AuditLogSelectCreateManyAndReturn`](AuditLogSelectCreateManyAndReturn.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10658

Select specific fields to fetch from the AuditLog

***

### skipDuplicates?

> `optional` **skipDuplicates**: `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:10663

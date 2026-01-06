[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogFindManyArgs

# Type Alias: AuditLogFindManyArgs\<ExtArgs\>

> **AuditLogFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:10582

AuditLog findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:10606

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing AuditLogs.

***

### distinct?

> `optional` **distinct**: [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md) \| [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:10619

***

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10590

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md) \| [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:10600

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of AuditLogs to fetch.

***

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:10586

Select specific fields to fetch from the AuditLog

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:10618

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` AuditLogs.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:10612

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` AuditLogs from the position of the cursor.

***

### where?

> `optional` **where**: [`AuditLogWhereInput`](AuditLogWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:10594

Filter, which AuditLogs to fetch.

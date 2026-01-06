[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PIIAuditLogFindFirstArgs

# Type Alias: PIIAuditLogFindFirstArgs\<ExtArgs\>

> **PIIAuditLogFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:17538

PIIAuditLog findFirst

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:17562

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for PIIAuditLogs.

***

### distinct?

> `optional` **distinct**: [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md) \| [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:17580

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of PIIAuditLogs.

***

### include?

> `optional` **include**: [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:17546

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md) \| [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:17556

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of PIIAuditLogs to fetch.

***

### select?

> `optional` **select**: [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:17542

Select specific fields to fetch from the PIIAuditLog

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:17574

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` PIIAuditLogs.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:17568

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` PIIAuditLogs from the position of the cursor.

***

### where?

> `optional` **where**: [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:17550

Filter, which PIIAuditLog to fetch.

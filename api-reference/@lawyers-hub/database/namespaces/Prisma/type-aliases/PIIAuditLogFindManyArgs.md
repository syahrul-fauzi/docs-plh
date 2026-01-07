[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogFindManyArgs

# Type Alias: PIIAuditLogFindManyArgs\<ExtArgs\>

> **PIIAuditLogFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17634

PIIAuditLog findMany

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17658

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing PIIAuditLogs.

---

### distinct?

> `optional` **distinct**:
> [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md) \|
> [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:17671

---

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17642

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)
> \|
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:17652

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of PIIAuditLogs to fetch.

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17638

Select specific fields to fetch from the PIIAuditLog

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:17670

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` PIIAuditLogs.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:17664

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` PIIAuditLogs from the position of the cursor.

---

### where?

> `optional` **where**: [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17646

Filter, which PIIAuditLogs to fetch.

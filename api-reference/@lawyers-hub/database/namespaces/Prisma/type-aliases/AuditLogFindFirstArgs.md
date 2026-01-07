[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AuditLogFindFirstArgs

# Type Alias: AuditLogFindFirstArgs\<ExtArgs\>

> **AuditLogFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:10486

AuditLog findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:10510

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for AuditLogs.

---

### distinct?

> `optional` **distinct**:
> [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md) \|
> [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:10528

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of AuditLogs.

---

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:10494

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md) \|
> [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:10504

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of AuditLogs to fetch.

---

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:10490

Select specific fields to fetch from the AuditLog

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:10522

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` AuditLogs.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:10516

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` AuditLogs from the position of the cursor.

---

### where?

> `optional` **where**: [`AuditLogWhereInput`](AuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:10498

Filter, which AuditLog to fetch.

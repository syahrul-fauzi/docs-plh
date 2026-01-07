[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
User$auditLogsArgs

# Type Alias: User$auditLogsArgs\<ExtArgs\>

> **User$auditLogsArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5592

User.auditLogs

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5603

---

### distinct?

> `optional` **distinct**:
> [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md) \|
> [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5606

---

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5600

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md) \|
> [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5602

---

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:5596

Select specific fields to fetch from the AuditLog

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5605

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5604

---

### where?

> `optional` **where**: [`AuditLogWhereInput`](AuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5601

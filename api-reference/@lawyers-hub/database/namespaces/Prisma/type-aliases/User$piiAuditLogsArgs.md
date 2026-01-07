[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
User$piiAuditLogsArgs

# Type Alias: User$piiAuditLogsArgs\<ExtArgs\>

> **User$piiAuditLogsArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5652

User.piiAuditLogs

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5663

---

### distinct?

> `optional` **distinct**:
> [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md) \|
> [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5666

---

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5660

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)
> \|
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5662

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5656

Select specific fields to fetch from the PIIAuditLog

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5665

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5664

---

### where?

> `optional` **where**: [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5661

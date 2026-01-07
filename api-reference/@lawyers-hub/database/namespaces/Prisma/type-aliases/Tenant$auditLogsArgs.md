[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
Tenant$auditLogsArgs

# Type Alias: Tenant$auditLogsArgs\<ExtArgs\>

> **Tenant$auditLogsArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3351

Tenant.auditLogs

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3362

---

### distinct?

> `optional` **distinct**:
> [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md) \|
> [`AuditLogScalarFieldEnum`](AuditLogScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3365

---

### include?

> `optional` **include**: [`AuditLogInclude`](AuditLogInclude.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:3359

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md) \|
> [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3361

---

### select?

> `optional` **select**: [`AuditLogSelect`](AuditLogSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3355

Select specific fields to fetch from the AuditLog

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3364

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3363

---

### where?

> `optional` **where**: [`AuditLogWhereInput`](AuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3360

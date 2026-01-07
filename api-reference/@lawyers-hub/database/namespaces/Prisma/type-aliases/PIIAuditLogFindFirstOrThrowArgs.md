[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogFindFirstOrThrowArgs

# Type Alias: PIIAuditLogFindFirstOrThrowArgs\<ExtArgs\>

> **PIIAuditLogFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:17586

PIIAuditLog findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17610

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for PIIAuditLogs.

---

### distinct?

> `optional` **distinct**:
> [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md) \|
> [`PIIAuditLogScalarFieldEnum`](PIIAuditLogScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:17628

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of PIIAuditLogs.

---

### include?

> `optional` **include**:
> [`PIIAuditLogInclude`](PIIAuditLogInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17594

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)
> \|
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:17604

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of PIIAuditLogs to fetch.

---

### select?

> `optional` **select**:
> [`PIIAuditLogSelect`](PIIAuditLogSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:17590

Select specific fields to fetch from the PIIAuditLog

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:17622

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` PIIAuditLogs.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:17616

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` PIIAuditLogs from the position of the cursor.

---

### where?

> `optional` **where**: [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:17598

Filter, which PIIAuditLog to fetch.

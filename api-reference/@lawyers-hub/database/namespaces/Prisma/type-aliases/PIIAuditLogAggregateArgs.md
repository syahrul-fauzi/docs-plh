[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogAggregateArgs

# Type Alias: PIIAuditLogAggregateArgs\<ExtArgs\>

> **PIIAuditLogAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:16891

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_avg?

> `optional` **\_avg**:
> [`PIIAuditLogAvgAggregateInputType`](PIIAuditLogAvgAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:16931

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to average

---

### \_count?

> `optional` **\_count**: `true` \|
> [`PIIAuditLogCountAggregateInputType`](PIIAuditLogCountAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:16925

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned PIIAuditLogs

---

### \_max?

> `optional` **\_max**:
> [`PIIAuditLogMaxAggregateInputType`](PIIAuditLogMaxAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:16949

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

---

### \_min?

> `optional` **\_min**:
> [`PIIAuditLogMinAggregateInputType`](PIIAuditLogMinAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:16943

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

---

### \_sum?

> `optional` **\_sum**:
> [`PIIAuditLogSumAggregateInputType`](PIIAuditLogSumAggregateInputType.md)

Defined in: node_modules/.prisma/client/index.d.ts:16937

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to sum

---

### cursor?

> `optional` **cursor**:
> [`PIIAuditLogWhereUniqueInput`](PIIAuditLogWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:16907

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

---

### orderBy?

> `optional` **orderBy**:
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)
> \|
> [`PIIAuditLogOrderByWithRelationInput`](PIIAuditLogOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:16901

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of PIIAuditLogs to fetch.

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:16919

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` PIIAuditLogs.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:16913

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` PIIAuditLogs from the position of the cursor.

---

### where?

> `optional` **where**: [`PIIAuditLogWhereInput`](PIIAuditLogWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:16895

Filter which PIIAuditLog to aggregate.

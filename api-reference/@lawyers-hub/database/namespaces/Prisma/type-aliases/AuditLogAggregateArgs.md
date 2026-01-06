[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AuditLogAggregateArgs

# Type Alias: AuditLogAggregateArgs\<ExtArgs\>

> **AuditLogAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:9879

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`AuditLogCountAggregateInputType`](AuditLogCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9913

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned AuditLogs

***

### \_max?

> `optional` **\_max**: [`AuditLogMaxAggregateInputType`](AuditLogMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9925

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`AuditLogMinAggregateInputType`](AuditLogMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9919

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`AuditLogWhereUniqueInput`](AuditLogWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9895

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md) \| [`AuditLogOrderByWithRelationInput`](AuditLogOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:9889

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of AuditLogs to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:9907

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` AuditLogs.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:9901

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` AuditLogs from the position of the cursor.

***

### where?

> `optional` **where**: [`AuditLogWhereInput`](AuditLogWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:9883

Filter which AuditLog to aggregate.

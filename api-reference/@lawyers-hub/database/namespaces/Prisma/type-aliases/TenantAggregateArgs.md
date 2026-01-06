[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantAggregateArgs

# Type Alias: TenantAggregateArgs\<ExtArgs\>

> **TenantAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:2446

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`TenantCountAggregateInputType`](TenantCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:2480

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Tenants

***

### \_max?

> `optional` **\_max**: [`TenantMaxAggregateInputType`](TenantMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:2492

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`TenantMinAggregateInputType`](TenantMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:2486

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:2462

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md) \| [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:2456

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Tenants to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:2474

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Tenants.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:2468

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Tenants from the position of the cursor.

***

### where?

> `optional` **where**: [`TenantWhereInput`](TenantWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:2450

Filter which Tenant to aggregate.

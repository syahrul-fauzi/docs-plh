[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantFindUniqueOrThrowArgs

# Type Alias: TenantFindUniqueOrThrowArgs\<ExtArgs\>

> **TenantFindUniqueOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:3060

Tenant findUniqueOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3068

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3064

Select specific fields to fetch from the Tenant

***

### where

> **where**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:3072

Filter, which Tenant to fetch.

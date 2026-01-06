[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantUpdateArgs

# Type Alias: TenantUpdateArgs\<ExtArgs\>

> **TenantUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:3261

Tenant update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`TenantUpdateInput`](TenantUpdateInput.md), [`TenantUncheckedUpdateInput`](TenantUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:3273

The data needed to update a Tenant.

***

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3269

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3265

Select specific fields to fetch from the Tenant

***

### where

> **where**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:3277

Choose, which Tenant to update.

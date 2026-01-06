[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantUpsertArgs

# Type Alias: TenantUpsertArgs\<ExtArgs\>

> **TenantUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:3297

Tenant upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`TenantCreateInput`](TenantCreateInput.md), [`TenantUncheckedCreateInput`](TenantUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:3313

In case the Tenant found by the `where` argument doesn't exist, create a new Tenant with this data.

***

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3305

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3301

Select specific fields to fetch from the Tenant

***

### update

> **update**: [`XOR`](XOR.md)\<[`TenantUpdateInput`](TenantUpdateInput.md), [`TenantUncheckedUpdateInput`](TenantUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:3317

In case the Tenant was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:3309

The filter to search for the Tenant to update in case it exists.

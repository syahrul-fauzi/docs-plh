[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantCreateArgs

# Type Alias: TenantCreateArgs\<ExtArgs\>

> **TenantCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:3217

Tenant create

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`TenantCreateInput`](TenantCreateInput.md), [`TenantUncheckedCreateInput`](TenantUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:3229

The data needed to create a Tenant.

***

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3225

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3221

Select specific fields to fetch from the Tenant

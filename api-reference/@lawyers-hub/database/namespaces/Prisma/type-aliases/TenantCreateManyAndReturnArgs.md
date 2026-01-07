[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TenantCreateManyAndReturnArgs

# Type Alias: TenantCreateManyAndReturnArgs\<ExtArgs\>

> **TenantCreateManyAndReturnArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3246

Tenant createManyAndReturn

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`TenantCreateManyInput`](TenantCreateManyInput.md) \|
> [`TenantCreateManyInput`](TenantCreateManyInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3254

The data used to create many Tenants.

---

### select?

> `optional` **select**:
> [`TenantSelectCreateManyAndReturn`](TenantSelectCreateManyAndReturn.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:3250

Select specific fields to fetch from the Tenant

---

### skipDuplicates?

> `optional` **skipDuplicates**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:3255

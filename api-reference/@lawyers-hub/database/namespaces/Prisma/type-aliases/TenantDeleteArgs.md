[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TenantDeleteArgs

# Type Alias: TenantDeleteArgs\<ExtArgs\>

> **TenantDeleteArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3323

Tenant delete

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3331

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3327

Select specific fields to fetch from the Tenant

---

### where

> **where**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3335

Filter which Tenant to delete.

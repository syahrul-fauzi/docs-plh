[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TenantFindFirstArgs

# Type Alias: TenantFindFirstArgs\<ExtArgs\>

> **TenantFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3078

Tenant findFirst

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3102

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Tenants.

---

### distinct?

> `optional` **distinct**: [`TenantScalarFieldEnum`](TenantScalarFieldEnum.md)
> \| [`TenantScalarFieldEnum`](TenantScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3120

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Tenants.

---

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3086

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md) \|
> [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3096

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Tenants to fetch.

---

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3082

Select specific fields to fetch from the Tenant

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3114

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Tenants.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3108

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Tenants from the position of the cursor.

---

### where?

> `optional` **where**: [`TenantWhereInput`](TenantWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3090

Filter, which Tenant to fetch.

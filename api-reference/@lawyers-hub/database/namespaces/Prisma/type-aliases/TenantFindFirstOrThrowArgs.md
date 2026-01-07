[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TenantFindFirstOrThrowArgs

# Type Alias: TenantFindFirstOrThrowArgs\<ExtArgs\>

> **TenantFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:3126

Tenant findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3150

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Tenants.

---

### distinct?

> `optional` **distinct**: [`TenantScalarFieldEnum`](TenantScalarFieldEnum.md)
> \| [`TenantScalarFieldEnum`](TenantScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3168

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Tenants.

---

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3134

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md) \|
> [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:3144

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Tenants to fetch.

---

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \|
> `null`

Defined in: node_modules/.prisma/client/index.d.ts:3130

Select specific fields to fetch from the Tenant

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3162

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Tenants.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:3156

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Tenants from the position of the cursor.

---

### where?

> `optional` **where**: [`TenantWhereInput`](TenantWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:3138

Filter, which Tenant to fetch.

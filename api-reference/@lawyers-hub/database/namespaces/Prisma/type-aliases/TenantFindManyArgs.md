[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TenantFindManyArgs

# Type Alias: TenantFindManyArgs\<ExtArgs\>

> **TenantFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:3174

Tenant findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`TenantWhereUniqueInput`](TenantWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:3198

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Tenants.

***

### distinct?

> `optional` **distinct**: [`TenantScalarFieldEnum`](TenantScalarFieldEnum.md) \| [`TenantScalarFieldEnum`](TenantScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:3211

***

### include?

> `optional` **include**: [`TenantInclude`](TenantInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3182

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md) \| [`TenantOrderByWithRelationInput`](TenantOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:3192

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Tenants to fetch.

***

### select?

> `optional` **select**: [`TenantSelect`](TenantSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:3178

Select specific fields to fetch from the Tenant

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:3210

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Tenants.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:3204

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Tenants from the position of the cursor.

***

### where?

> `optional` **where**: [`TenantWhereInput`](TenantWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:3186

Filter, which Tenants to fetch.

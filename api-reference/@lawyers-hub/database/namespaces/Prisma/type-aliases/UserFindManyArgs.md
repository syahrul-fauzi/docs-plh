[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserFindManyArgs

# Type Alias: UserFindManyArgs\<ExtArgs\>

> **UserFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:5411

User findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`UserWhereUniqueInput`](UserWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:5435

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Users.

***

### distinct?

> `optional` **distinct**: [`UserScalarFieldEnum`](UserScalarFieldEnum.md) \| [`UserScalarFieldEnum`](UserScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:5448

***

### include?

> `optional` **include**: [`UserInclude`](UserInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5419

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`UserOrderByWithRelationInput`](UserOrderByWithRelationInput.md) \| [`UserOrderByWithRelationInput`](UserOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:5429

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Users to fetch.

***

### select?

> `optional` **select**: [`UserSelect`](UserSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5415

Select specific fields to fetch from the User

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:5447

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Users.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:5441

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Users from the position of the cursor.

***

### where?

> `optional` **where**: [`UserWhereInput`](UserWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:5423

Filter, which Users to fetch.

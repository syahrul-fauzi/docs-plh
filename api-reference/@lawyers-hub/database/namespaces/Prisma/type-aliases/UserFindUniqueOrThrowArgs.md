[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserFindUniqueOrThrowArgs

# Type Alias: UserFindUniqueOrThrowArgs\<ExtArgs\>

> **UserFindUniqueOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:5297

User findUniqueOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### include?

> `optional` **include**: [`UserInclude`](UserInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5305

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`UserSelect`](UserSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5301

Select specific fields to fetch from the User

***

### where

> **where**: [`UserWhereUniqueInput`](UserWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:5309

Filter, which User to fetch.

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserCreateManyAndReturnArgs

# Type Alias: UserCreateManyAndReturnArgs\<ExtArgs\>

> **UserCreateManyAndReturnArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:5483

User createManyAndReturn

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`UserCreateManyInput`](UserCreateManyInput.md) \| [`UserCreateManyInput`](UserCreateManyInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:5491

The data used to create many Users.

***

### include?

> `optional` **include**: [`UserIncludeCreateManyAndReturn`](UserIncludeCreateManyAndReturn.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5496

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`UserSelectCreateManyAndReturn`](UserSelectCreateManyAndReturn.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5487

Select specific fields to fetch from the User

***

### skipDuplicates?

> `optional` **skipDuplicates**: `boolean`

Defined in: node\_modules/.prisma/client/index.d.ts:5492

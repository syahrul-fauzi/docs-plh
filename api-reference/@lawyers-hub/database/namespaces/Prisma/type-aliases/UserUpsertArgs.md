[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserUpsertArgs

# Type Alias: UserUpsertArgs\<ExtArgs\>

> **UserUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:5538

User upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`UserCreateInput`](UserCreateInput.md), [`UserUncheckedCreateInput`](UserUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:5554

In case the User found by the `where` argument doesn't exist, create a new User with this data.

***

### include?

> `optional` **include**: [`UserInclude`](UserInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5546

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`UserSelect`](UserSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5542

Select specific fields to fetch from the User

***

### update

> **update**: [`XOR`](XOR.md)\<[`UserUpdateInput`](UserUpdateInput.md), [`UserUncheckedUpdateInput`](UserUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:5558

In case the User was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`UserWhereUniqueInput`](UserWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:5550

The filter to search for the User to update in case it exists.

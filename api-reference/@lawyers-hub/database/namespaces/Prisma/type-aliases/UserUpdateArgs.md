[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserUpdateArgs

# Type Alias: UserUpdateArgs\<ExtArgs\>

> **UserUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:5502

User update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`UserUpdateInput`](UserUpdateInput.md), [`UserUncheckedUpdateInput`](UserUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:5514

The data needed to update a User.

***

### include?

> `optional` **include**: [`UserInclude`](UserInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5510

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`UserSelect`](UserSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:5506

Select specific fields to fetch from the User

***

### where

> **where**: [`UserWhereUniqueInput`](UserWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:5518

Choose, which User to update.

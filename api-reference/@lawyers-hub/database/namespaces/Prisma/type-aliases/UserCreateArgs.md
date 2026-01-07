[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserCreateArgs

# Type Alias: UserCreateArgs\<ExtArgs\>

> **UserCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5454

User create

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`UserCreateInput`](UserCreateInput.md),
> [`UserUncheckedCreateInput`](UserUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:5466

The data needed to create a User.

---

### include?

> `optional` **include**: [`UserInclude`](UserInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5462

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`UserSelect`](UserSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5458

Select specific fields to fetch from the User

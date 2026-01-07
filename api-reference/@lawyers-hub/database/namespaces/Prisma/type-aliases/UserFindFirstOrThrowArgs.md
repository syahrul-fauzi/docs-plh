[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserFindFirstOrThrowArgs

# Type Alias: UserFindFirstOrThrowArgs\<ExtArgs\>

> **UserFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:5363

User findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`UserWhereUniqueInput`](UserWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5387

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Users.

---

### distinct?

> `optional` **distinct**: [`UserScalarFieldEnum`](UserScalarFieldEnum.md) \|
> [`UserScalarFieldEnum`](UserScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5405

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Users.

---

### include?

> `optional` **include**: [`UserInclude`](UserInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5371

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`UserOrderByWithRelationInput`](UserOrderByWithRelationInput.md) \|
> [`UserOrderByWithRelationInput`](UserOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:5381

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Users to fetch.

---

### select?

> `optional` **select**: [`UserSelect`](UserSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:5367

Select specific fields to fetch from the User

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5399

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Users.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:5393

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Users from the position of the cursor.

---

### where?

> `optional` **where**: [`UserWhereInput`](UserWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:5375

Filter, which User to fetch.

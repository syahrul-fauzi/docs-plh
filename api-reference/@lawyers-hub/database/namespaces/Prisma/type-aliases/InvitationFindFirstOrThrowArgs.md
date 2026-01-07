[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
InvitationFindFirstOrThrowArgs

# Type Alias: InvitationFindFirstOrThrowArgs\<ExtArgs\>

> **InvitationFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:12490

Invitation findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**:
> [`InvitationWhereUniqueInput`](InvitationWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:12514

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Invitations.

---

### distinct?

> `optional` **distinct**:
> [`InvitationScalarFieldEnum`](InvitationScalarFieldEnum.md) \|
> [`InvitationScalarFieldEnum`](InvitationScalarFieldEnum.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:12532

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Invitations.

---

### include?

> `optional` **include**:
> [`InvitationInclude`](InvitationInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12498

Choose, which related nodes to fetch as well

---

### orderBy?

> `optional` **orderBy**:
> [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md)
> \|
> [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:12508

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Invitations to fetch.

---

### select?

> `optional` **select**: [`InvitationSelect`](InvitationSelect.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12494

Select specific fields to fetch from the Invitation

---

### skip?

> `optional` **skip**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:12526

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Invitations.

---

### take?

> `optional` **take**: `number`

Defined in: node_modules/.prisma/client/index.d.ts:12520

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Invitations from the position of the cursor.

---

### where?

> `optional` **where**: [`InvitationWhereInput`](InvitationWhereInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:12502

Filter, which Invitation to fetch.

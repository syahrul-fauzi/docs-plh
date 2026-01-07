[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
InvitationUpsertArgs

# Type Alias: InvitationUpsertArgs\<ExtArgs\>

> **InvitationUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:12665

Invitation upsert

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**:
> [`XOR`](XOR.md)\<[`InvitationCreateInput`](InvitationCreateInput.md),
> [`InvitationUncheckedCreateInput`](InvitationUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:12681

In case the Invitation found by the `where` argument doesn't exist, create a new
Invitation with this data.

---

### include?

> `optional` **include**:
> [`InvitationInclude`](InvitationInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12673

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`InvitationSelect`](InvitationSelect.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12669

Select specific fields to fetch from the Invitation

---

### update

> **update**:
> [`XOR`](XOR.md)\<[`InvitationUpdateInput`](InvitationUpdateInput.md),
> [`InvitationUncheckedUpdateInput`](InvitationUncheckedUpdateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:12685

In case the Invitation was found with the provided `where` argument, update it
with this data.

---

### where

> **where**: [`InvitationWhereUniqueInput`](InvitationWhereUniqueInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:12677

The filter to search for the Invitation to update in case it exists.

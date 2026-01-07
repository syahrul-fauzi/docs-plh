[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
InvitationCreateArgs

# Type Alias: InvitationCreateArgs\<ExtArgs\>

> **InvitationCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:12581

Invitation create

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`InvitationCreateInput`](InvitationCreateInput.md),
> [`InvitationUncheckedCreateInput`](InvitationUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:12593

The data needed to create a Invitation.

---

### include?

> `optional` **include**:
> [`InvitationInclude`](InvitationInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12589

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**: [`InvitationSelect`](InvitationSelect.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12585

Select specific fields to fetch from the Invitation

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / InvitationUpdateArgs

# Type Alias: InvitationUpdateArgs\<ExtArgs\>

> **InvitationUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:12629

Invitation update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`InvitationUpdateInput`](InvitationUpdateInput.md), [`InvitationUncheckedUpdateInput`](InvitationUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:12641

The data needed to update a Invitation.

***

### include?

> `optional` **include**: [`InvitationInclude`](InvitationInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:12637

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`InvitationSelect`](InvitationSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:12633

Select specific fields to fetch from the Invitation

***

### where

> **where**: [`InvitationWhereUniqueInput`](InvitationWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12645

Choose, which Invitation to update.

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / InvitationFindManyArgs

# Type Alias: InvitationFindManyArgs\<ExtArgs\>

> **InvitationFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:12538

Invitation findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`InvitationWhereUniqueInput`](InvitationWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12562

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing Invitations.

***

### distinct?

> `optional` **distinct**: [`InvitationScalarFieldEnum`](InvitationScalarFieldEnum.md) \| [`InvitationScalarFieldEnum`](InvitationScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:12575

***

### include?

> `optional` **include**: [`InvitationInclude`](InvitationInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:12546

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md) \| [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:12556

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Invitations to fetch.

***

### select?

> `optional` **select**: [`InvitationSelect`](InvitationSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:12542

Select specific fields to fetch from the Invitation

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:12574

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Invitations.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:12568

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Invitations from the position of the cursor.

***

### where?

> `optional` **where**: [`InvitationWhereInput`](InvitationWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12550

Filter, which Invitations to fetch.

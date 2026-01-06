[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / InvitationFindFirstArgs

# Type Alias: InvitationFindFirstArgs\<ExtArgs\>

> **InvitationFindFirstArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:12442

Invitation findFirst

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`InvitationWhereUniqueInput`](InvitationWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12466

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for Invitations.

***

### distinct?

> `optional` **distinct**: [`InvitationScalarFieldEnum`](InvitationScalarFieldEnum.md) \| [`InvitationScalarFieldEnum`](InvitationScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:12484

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of Invitations.

***

### include?

> `optional` **include**: [`InvitationInclude`](InvitationInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:12450

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md) \| [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:12460

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Invitations to fetch.

***

### select?

> `optional` **select**: [`InvitationSelect`](InvitationSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:12446

Select specific fields to fetch from the Invitation

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:12478

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Invitations.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:12472

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Invitations from the position of the cursor.

***

### where?

> `optional` **where**: [`InvitationWhereInput`](InvitationWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12454

Filter, which Invitation to fetch.

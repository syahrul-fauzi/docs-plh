[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / InvitationAggregateArgs

# Type Alias: InvitationAggregateArgs\<ExtArgs\>

> **InvitationAggregateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:11835

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \_count?

> `optional` **\_count**: `true` \| [`InvitationCountAggregateInputType`](InvitationCountAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:11869

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Count returned Invitations

***

### \_max?

> `optional` **\_max**: [`InvitationMaxAggregateInputType`](InvitationMaxAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:11881

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the maximum value

***

### \_min?

> `optional` **\_min**: [`InvitationMinAggregateInputType`](InvitationMinAggregateInputType.md)

Defined in: node\_modules/.prisma/client/index.d.ts:11875

[Aggregation Docs](https://www.prisma.io/docs/concepts/components/prisma-client/aggregations)

Select which fields to find the minimum value

***

### cursor?

> `optional` **cursor**: [`InvitationWhereUniqueInput`](InvitationWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:11851

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the start position

***

### orderBy?

> `optional` **orderBy**: [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md) \| [`InvitationOrderByWithRelationInput`](InvitationOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:11845

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of Invitations to fetch.

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:11863

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` Invitations.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:11857

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` Invitations from the position of the cursor.

***

### where?

> `optional` **where**: [`InvitationWhereInput`](InvitationWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:11839

Filter which Invitation to aggregate.

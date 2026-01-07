[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
InvitationCreateManyAndReturnArgs

# Type Alias: InvitationCreateManyAndReturnArgs\<ExtArgs\>

> **InvitationCreateManyAndReturnArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:12610

Invitation createManyAndReturn

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`InvitationCreateManyInput`](InvitationCreateManyInput.md) \|
> [`InvitationCreateManyInput`](InvitationCreateManyInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:12618

The data used to create many Invitations.

---

### include?

> `optional` **include**:
> [`InvitationIncludeCreateManyAndReturn`](InvitationIncludeCreateManyAndReturn.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12623

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`InvitationSelectCreateManyAndReturn`](InvitationSelectCreateManyAndReturn.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:12614

Select specific fields to fetch from the Invitation

---

### skipDuplicates?

> `optional` **skipDuplicates**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:12619

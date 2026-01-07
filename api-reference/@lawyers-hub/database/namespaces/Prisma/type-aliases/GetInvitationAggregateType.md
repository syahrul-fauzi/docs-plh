[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetInvitationAggregateType

# Type Alias: GetInvitationAggregateType\<T\>

> **GetInvitationAggregateType**\<`T`\> = \{ \[P in keyof T & keyof
> AggregateInvitation\]: P extends "\_count" \| "count" ? T\[P\] extends true ?
> number : GetScalarType\<T\[P\], AggregateInvitation\[P\]\> :
> GetScalarType\<T\[P\], AggregateInvitation\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:11884

## Type Parameters

### T

`T` _extends_ [`InvitationAggregateArgs`](InvitationAggregateArgs.md)

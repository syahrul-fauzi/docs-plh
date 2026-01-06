[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetInvitationGroupByPayload

# Type Alias: GetInvitationGroupByPayload\<T\>

> **GetInvitationGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`InvitationGroupByOutputType`](InvitationGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof InvitationGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], InvitationGroupByOutputType[P]> : GetScalarType<T[P], InvitationGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:11922

## Type Parameters

### T

`T` *extends* [`InvitationGroupByArgs`](InvitationGroupByArgs.md)

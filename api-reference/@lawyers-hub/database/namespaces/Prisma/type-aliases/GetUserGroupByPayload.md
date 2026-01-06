[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetUserGroupByPayload

# Type Alias: GetUserGroupByPayload\<T\>

> **GetUserGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`UserGroupByOutputType`](UserGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof UserGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], UserGroupByOutputType[P]> : GetScalarType<T[P], UserGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:4783

## Type Parameters

### T

`T` *extends* [`UserGroupByArgs`](UserGroupByArgs.md)

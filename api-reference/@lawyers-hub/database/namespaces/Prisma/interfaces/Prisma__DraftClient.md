[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
Prisma\_\_DraftClient

# Interface: Prisma\_\_DraftClient\<T, Null, ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:8376

The delegate class that acts as a "Promise-like" for Draft. Why is this prefixed
with `Prisma__`? Because we want to prevent naming conflicts as mentioned in
<https://github.com/prisma/prisma-client-js/issues/707>

## Extends

- [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T`\>

## Type Parameters

### T

`T`

### Null

`Null` = `never`

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \[toStringTag\]

> `readonly` **\[toStringTag\]**: `"PrismaPromise"`

Defined in: node_modules/.prisma/client/index.d.ts:8377

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### case()

> **case**\<`T`\>(`args?`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:8379

#### Type Parameters

##### T

`T` _extends_ [`Draft$caseArgs`](../type-aliases/Draft$caseArgs.md)\<`ExtArgs`\>
= \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`Draft$caseArgs`](../type-aliases/Draft$caseArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

---

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node_modules/.prisma/client/index.d.ts:8393

Attaches a callback for only the rejection of the Promise.

#### Type Parameters

##### TResult

`TResult` = `never`

#### Parameters

##### onrejected?

The callback to execute when the Promise is rejected.

(`reason`) => `TResult` \| `PromiseLike`\<`TResult`\> | `null`

#### Returns

`Promise`\<`T` \| `TResult`\>

A Promise for the completion of the callback.

#### Overrides

`Prisma.PrismaPromise.catch`

---

### comments()

> **comments**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \|
> `GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:8378

#### Type Parameters

##### T

`T` _extends_
[`Draft$commentsArgs`](../type-aliases/Draft$commentsArgs.md)\<`ExtArgs`\> = \{
\}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`Draft$commentsArgs`](../type-aliases/Draft$commentsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \|
`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

---

### finally()

> **finally**(`onfinally?`): `Promise`\<`T`\>

Defined in: node_modules/.prisma/client/index.d.ts:8400

Attaches a callback that is invoked when the Promise is settled (fulfilled or
rejected). The resolved value cannot be modified from the callback.

#### Parameters

##### onfinally?

The callback to execute when the Promise is settled (fulfilled or rejected).

() => `void` | `null`

#### Returns

`Promise`\<`T`\>

A Promise for the completion of the callback.

#### Overrides

`Prisma.PrismaPromise.finally`

---

### tenant()

> **tenant**\<`T`\>(`args?`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`Null` \|
> `GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:8380

#### Type Parameters

##### T

`T` _extends_
[`TenantDefaultArgs`](../type-aliases/TenantDefaultArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`TenantDefaultArgs`](../type-aliases/TenantDefaultArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`Null` \|
`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `Null`, `ExtArgs`\>

---

### then()

> **then**\<`TResult1`, `TResult2`\>(`onfulfilled?`, `onrejected?`):
> `Promise`\<`TResult1` \| `TResult2`\>

Defined in: node_modules/.prisma/client/index.d.ts:8387

Attaches callbacks for the resolution and/or rejection of the Promise.

#### Type Parameters

##### TResult1

`TResult1` = `T`

##### TResult2

`TResult2` = `never`

#### Parameters

##### onfulfilled?

The callback to execute when the Promise is resolved.

(`value`) => `TResult1` \| `PromiseLike`\<`TResult1`\> | `null`

##### onrejected?

The callback to execute when the Promise is rejected.

(`reason`) => `TResult2` \| `PromiseLike`\<`TResult2`\> | `null`

#### Returns

`Promise`\<`TResult1` \| `TResult2`\>

A Promise for the completion of which ever callback is executed.

#### Overrides

`Prisma.PrismaPromise.then`

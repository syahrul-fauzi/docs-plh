[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
Prisma\_\_PIIAuditLogClient

# Interface: Prisma\_\_PIIAuditLogClient\<T, Null, ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:17450

The delegate class that acts as a "Promise-like" for PIIAuditLog. Why is this
prefixed with `Prisma__`? Because we want to prevent naming conflicts as
mentioned in <https://github.com/prisma/prisma-client-js/issues/707>

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

Defined in: node_modules/.prisma/client/index.d.ts:17451

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node_modules/.prisma/client/index.d.ts:17467

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

### document()

> **document**\<`T`\>(`args?`):
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17452

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLog$documentArgs`](../type-aliases/PIIAuditLog$documentArgs.md)\<`ExtArgs`\>
= \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`PIIAuditLog$documentArgs`](../type-aliases/PIIAuditLog$documentArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

---

### finally()

> **finally**(`onfinally?`): `Promise`\<`T`\>

Defined in: node_modules/.prisma/client/index.d.ts:17474

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

Defined in: node_modules/.prisma/client/index.d.ts:17453

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

Defined in: node_modules/.prisma/client/index.d.ts:17461

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

---

### user()

> **user**\<`T`\>(`args?`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`Null` \|
> `GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17454

#### Type Parameters

##### T

`T` _extends_
[`UserDefaultArgs`](../type-aliases/UserDefaultArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`UserDefaultArgs`](../type-aliases/UserDefaultArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`Null` \|
`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `Null`, `ExtArgs`\>

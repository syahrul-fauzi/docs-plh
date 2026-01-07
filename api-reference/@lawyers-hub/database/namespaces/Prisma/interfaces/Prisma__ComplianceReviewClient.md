[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
Prisma\_\_ComplianceReviewClient

# Interface: Prisma\_\_ComplianceReviewClient\<T, Null, ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:16401

The delegate class that acts as a "Promise-like" for ComplianceReview. Why is
this prefixed with `Prisma__`? Because we want to prevent naming conflicts as
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

Defined in: node_modules/.prisma/client/index.d.ts:16402

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node_modules/.prisma/client/index.d.ts:16417

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

### finally()

> **finally**(`onfinally?`): `Promise`\<`T`\>

Defined in: node_modules/.prisma/client/index.d.ts:16424

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

### reviewer()

> **reviewer**\<`T`\>(`args?`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`Null` \|
> `GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:16403

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

---

### tenant()

> **tenant**\<`T`\>(`args?`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`Null` \|
> `GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:16404

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

Defined in: node_modules/.prisma/client/index.d.ts:16411

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

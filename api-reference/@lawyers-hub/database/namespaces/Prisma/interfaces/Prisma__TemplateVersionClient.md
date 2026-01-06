[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Prisma\_\_TemplateVersionClient

# Interface: Prisma\_\_TemplateVersionClient\<T, Null, ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:14339

The delegate class that acts as a "Promise-like" for TemplateVersion.
Why is this prefixed with `Prisma__`?
Because we want to prevent naming conflicts as mentioned in
https://github.com/prisma/prisma-client-js/issues/707

## Extends

- [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T`\>

## Type Parameters

### T

`T`

### Null

`Null` = `never`

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### \[toStringTag\]

> `readonly` **\[toStringTag\]**: `"PrismaPromise"`

Defined in: node\_modules/.prisma/client/index.d.ts:14340

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node\_modules/.prisma/client/index.d.ts:14355

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

***

### finally()

> **finally**(`onfinally?`): `Promise`\<`T`\>

Defined in: node\_modules/.prisma/client/index.d.ts:14362

Attaches a callback that is invoked when the Promise is settled (fulfilled or rejected). The
resolved value cannot be modified from the callback.

#### Parameters

##### onfinally?

The callback to execute when the Promise is settled (fulfilled or rejected).

() => `void` | `null`

#### Returns

`Promise`\<`T`\>

A Promise for the completion of the callback.

#### Overrides

`Prisma.PrismaPromise.finally`

***

### template()

> **template**\<`T`\>(`args?`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`Null` \| `GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:14341

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateDefaultArgs`](../type-aliases/DocumentTemplateDefaultArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`DocumentTemplateDefaultArgs`](../type-aliases/DocumentTemplateDefaultArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`Null` \| `GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

***

### then()

> **then**\<`TResult1`, `TResult2`\>(`onfulfilled?`, `onrejected?`): `Promise`\<`TResult1` \| `TResult2`\>

Defined in: node\_modules/.prisma/client/index.d.ts:14349

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

***

### user()

> **user**\<`T`\>(`args?`): [`Prisma__UserClient`](Prisma__UserClient.md)\<`Null` \| `GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:14342

#### Type Parameters

##### T

`T` *extends* [`UserDefaultArgs`](../type-aliases/UserDefaultArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`UserDefaultArgs`](../type-aliases/UserDefaultArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`Null` \| `GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Prisma\_\_DocumentClient

# Interface: Prisma\_\_DocumentClient\<T, Null, ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:7342

The delegate class that acts as a "Promise-like" for Document.
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

Defined in: node\_modules/.prisma/client/index.d.ts:7343

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### case()

> **case**\<`T`\>(`args?`): [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:7344

#### Type Parameters

##### T

`T` *extends* [`Document$caseArgs`](../type-aliases/Document$caseArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Document$caseArgs`](../type-aliases/Document$caseArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

***

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node\_modules/.prisma/client/index.d.ts:7359

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

Defined in: node\_modules/.prisma/client/index.d.ts:7366

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

### piiAuditLogs()

> **piiAuditLogs**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:7346

#### Type Parameters

##### T

`T` *extends* [`Document$piiAuditLogsArgs`](../type-aliases/Document$piiAuditLogsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Document$piiAuditLogsArgs`](../type-aliases/Document$piiAuditLogsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### tenant()

> **tenant**\<`T`\>(`args?`): [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`Null` \| `GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:7345

#### Type Parameters

##### T

`T` *extends* [`TenantDefaultArgs`](../type-aliases/TenantDefaultArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`TenantDefaultArgs`](../type-aliases/TenantDefaultArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`Null` \| `GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

***

### then()

> **then**\<`TResult1`, `TResult2`\>(`onfulfilled?`, `onrejected?`): `Promise`\<`TResult1` \| `TResult2`\>

Defined in: node\_modules/.prisma/client/index.d.ts:7353

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

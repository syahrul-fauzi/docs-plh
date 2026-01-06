[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Prisma\_\_UserClient

# Interface: Prisma\_\_UserClient\<T, Null, ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:5228

The delegate class that acts as a "Promise-like" for User.
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

Defined in: node\_modules/.prisma/client/index.d.ts:5229

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### auditLogs()

> **auditLogs**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:5230

#### Type Parameters

##### T

`T` *extends* [`User$auditLogsArgs`](../type-aliases/User$auditLogsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`User$auditLogsArgs`](../type-aliases/User$auditLogsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node\_modules/.prisma/client/index.d.ts:5248

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

### comments()

> **comments**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:5231

#### Type Parameters

##### T

`T` *extends* [`User$commentsArgs`](../type-aliases/User$commentsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`User$commentsArgs`](../type-aliases/User$commentsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### complianceReviews()

> **complianceReviews**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:5232

#### Type Parameters

##### T

`T` *extends* [`User$complianceReviewsArgs`](../type-aliases/User$complianceReviewsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`User$complianceReviewsArgs`](../type-aliases/User$complianceReviewsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### finally()

> **finally**(`onfinally?`): `Promise`\<`T`\>

Defined in: node\_modules/.prisma/client/index.d.ts:5255

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

Defined in: node\_modules/.prisma/client/index.d.ts:5233

#### Type Parameters

##### T

`T` *extends* [`User$piiAuditLogsArgs`](../type-aliases/User$piiAuditLogsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`User$piiAuditLogsArgs`](../type-aliases/User$piiAuditLogsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### templateVersions()

> **templateVersions**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:5234

#### Type Parameters

##### T

`T` *extends* [`User$templateVersionsArgs`](../type-aliases/User$templateVersionsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`User$templateVersionsArgs`](../type-aliases/User$templateVersionsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### tenant()

> **tenant**\<`T`\>(`args?`): [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`Null` \| `GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `Null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:5235

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

Defined in: node\_modules/.prisma/client/index.d.ts:5242

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

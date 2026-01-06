[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Prisma\_\_TenantClient

# Interface: Prisma\_\_TenantClient\<T, Null, ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:2986

The delegate class that acts as a "Promise-like" for Tenant.
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

Defined in: node\_modules/.prisma/client/index.d.ts:2987

#### Overrides

`Prisma.PrismaPromise.[toStringTag]`

## Methods

### auditLogs()

> **auditLogs**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2988

#### Type Parameters

##### T

`T` *extends* [`Tenant$auditLogsArgs`](../type-aliases/Tenant$auditLogsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$auditLogsArgs`](../type-aliases/Tenant$auditLogsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### cases()

> **cases**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2989

#### Type Parameters

##### T

`T` *extends* [`Tenant$casesArgs`](../type-aliases/Tenant$casesArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$casesArgs`](../type-aliases/Tenant$casesArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### catch()

> **catch**\<`TResult`\>(`onrejected?`): `Promise`\<`T` \| `TResult`\>

Defined in: node\_modules/.prisma/client/index.d.ts:3012

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

Defined in: node\_modules/.prisma/client/index.d.ts:2990

#### Type Parameters

##### T

`T` *extends* [`Tenant$commentsArgs`](../type-aliases/Tenant$commentsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$commentsArgs`](../type-aliases/Tenant$commentsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### complianceReviews()

> **complianceReviews**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2991

#### Type Parameters

##### T

`T` *extends* [`Tenant$complianceReviewsArgs`](../type-aliases/Tenant$complianceReviewsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$complianceReviewsArgs`](../type-aliases/Tenant$complianceReviewsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### documents()

> **documents**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2993

#### Type Parameters

##### T

`T` *extends* [`Tenant$documentsArgs`](../type-aliases/Tenant$documentsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$documentsArgs`](../type-aliases/Tenant$documentsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### documentTemplates()

> **documentTemplates**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2992

#### Type Parameters

##### T

`T` *extends* [`Tenant$documentTemplatesArgs`](../type-aliases/Tenant$documentTemplatesArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$documentTemplatesArgs`](../type-aliases/Tenant$documentTemplatesArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### drafts()

> **drafts**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2994

#### Type Parameters

##### T

`T` *extends* [`Tenant$draftsArgs`](../type-aliases/Tenant$draftsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$draftsArgs`](../type-aliases/Tenant$draftsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### finally()

> **finally**(`onfinally?`): `Promise`\<`T`\>

Defined in: node\_modules/.prisma/client/index.d.ts:3019

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

### invitations()

> **invitations**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2995

#### Type Parameters

##### T

`T` *extends* [`Tenant$invitationsArgs`](../type-aliases/Tenant$invitationsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$invitationsArgs`](../type-aliases/Tenant$invitationsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### piiAuditLogs()

> **piiAuditLogs**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2996

#### Type Parameters

##### T

`T` *extends* [`Tenant$piiAuditLogsArgs`](../type-aliases/Tenant$piiAuditLogsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$piiAuditLogsArgs`](../type-aliases/Tenant$piiAuditLogsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### subscription()

> **subscription**\<`T`\>(`args?`): [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:2997

#### Type Parameters

##### T

`T` *extends* [`Tenant$subscriptionArgs`](../type-aliases/Tenant$subscriptionArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$subscriptionArgs`](../type-aliases/Tenant$subscriptionArgs.md)\<`ExtArgs`\>\>

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

***

### then()

> **then**\<`TResult1`, `TResult2`\>(`onfulfilled?`, `onrejected?`): `Promise`\<`TResult1` \| `TResult2`\>

Defined in: node\_modules/.prisma/client/index.d.ts:3006

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

### usageRecords()

> **usageRecords**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2998

#### Type Parameters

##### T

`T` *extends* [`Tenant$usageRecordsArgs`](../type-aliases/Tenant$usageRecordsArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$usageRecordsArgs`](../type-aliases/Tenant$usageRecordsArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

***

### users()

> **users**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2999

#### Type Parameters

##### T

`T` *extends* [`Tenant$usersArgs`](../type-aliases/Tenant$usersArgs.md)\<`ExtArgs`\> = \{ \}

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`Tenant$usersArgs`](../type-aliases/Tenant$usersArgs.md)\<`ExtArgs`\>\>

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`Null` \| `GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

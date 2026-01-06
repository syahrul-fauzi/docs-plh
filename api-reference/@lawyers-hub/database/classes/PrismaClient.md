[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/database](../README.md) / PrismaClient

# Class: PrismaClient\<ClientOptions, U, ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:106

##  Prisma Client ʲˢ

Type-safe database client for TypeScript & Node.js

## Example

```
const prisma = new PrismaClient()
// Fetch zero or more Tenants
const tenants = await prisma.tenant.findMany()
```

Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client).

## Type Parameters

### ClientOptions

`ClientOptions` *extends* [`PrismaClientOptions`](../namespaces/Prisma/interfaces/PrismaClientOptions.md) = [`PrismaClientOptions`](../namespaces/Prisma/interfaces/PrismaClientOptions.md)

### U

`U` = `"log"` *extends* keyof `ClientOptions` ? `ClientOptions`\[`"log"`\] *extends* ([`LogLevel`](../namespaces/Prisma/type-aliases/LogLevel.md) \| [`LogDefinition`](../namespaces/Prisma/type-aliases/LogDefinition.md))[] ? [`GetEvents`](../namespaces/Prisma/type-aliases/GetEvents.md)\<`ClientOptions`\[`"log"`\]\> : `never` : `never`

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Constructors

### Constructor

> **new PrismaClient**\<`ClientOptions`, `U`, `ExtArgs`\>(`optionsArg?`): `PrismaClient`\<`ClientOptions`, `U`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:128

##  Prisma Client ʲˢ

Type-safe database client for TypeScript & Node.js

#### Parameters

##### optionsArg?

[`Subset`](../namespaces/Prisma/type-aliases/Subset.md)\<`ClientOptions`, [`PrismaClientOptions`](../namespaces/Prisma/interfaces/PrismaClientOptions.md)\>

#### Returns

`PrismaClient`\<`ClientOptions`, `U`, `ExtArgs`\>

#### Example

```
const prisma = new PrismaClient()
// Fetch zero or more Tenants
const tenants = await prisma.tenant.findMany()
```

Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client).

## Properties

### $extends

> **$extends**: `ExtendsHook`\<`"extends"`, [`TypeMapCb`](../namespaces/Prisma/interfaces/TypeMapCb.md), `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:213

## Accessors

### aIModelConfig

#### Get Signature

> **get** **aIModelConfig**(): [`AIModelConfigDelegate`](../namespaces/Prisma/interfaces/AIModelConfigDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:343

`prisma.aIModelConfig`: Exposes CRUD operations for the **AIModelConfig** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more AIModelConfigs
 * const aIModelConfigs = await prisma.aIModelConfig.findMany()
 * ```

##### Returns

[`AIModelConfigDelegate`](../namespaces/Prisma/interfaces/AIModelConfigDelegate.md)\<`ExtArgs`\>

***

### auditLog

#### Get Signature

> **get** **auditLog**(): [`AuditLogDelegate`](../namespaces/Prisma/interfaces/AuditLogDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:293

`prisma.auditLog`: Exposes CRUD operations for the **AuditLog** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more AuditLogs
 * const auditLogs = await prisma.auditLog.findMany()
 * ```

##### Returns

[`AuditLogDelegate`](../namespaces/Prisma/interfaces/AuditLogDelegate.md)\<`ExtArgs`\>

***

### case

#### Get Signature

> **get** **case**(): [`CaseDelegate`](../namespaces/Prisma/interfaces/CaseDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:253

`prisma.case`: Exposes CRUD operations for the **Case** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Cases
 * const cases = await prisma.case.findMany()
 * ```

##### Returns

[`CaseDelegate`](../namespaces/Prisma/interfaces/CaseDelegate.md)\<`ExtArgs`\>

***

### comment

#### Get Signature

> **get** **comment**(): [`CommentDelegate`](../namespaces/Prisma/interfaces/CommentDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:283

`prisma.comment`: Exposes CRUD operations for the **Comment** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Comments
 * const comments = await prisma.comment.findMany()
 * ```

##### Returns

[`CommentDelegate`](../namespaces/Prisma/interfaces/CommentDelegate.md)\<`ExtArgs`\>

***

### complianceReview

#### Get Signature

> **get** **complianceReview**(): [`ComplianceReviewDelegate`](../namespaces/Prisma/interfaces/ComplianceReviewDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:353

`prisma.complianceReview`: Exposes CRUD operations for the **ComplianceReview** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more ComplianceReviews
 * const complianceReviews = await prisma.complianceReview.findMany()
 * ```

##### Returns

[`ComplianceReviewDelegate`](../namespaces/Prisma/interfaces/ComplianceReviewDelegate.md)\<`ExtArgs`\>

***

### document

#### Get Signature

> **get** **document**(): [`DocumentDelegate`](../namespaces/Prisma/interfaces/DocumentDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:263

`prisma.document`: Exposes CRUD operations for the **Document** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Documents
 * const documents = await prisma.document.findMany()
 * ```

##### Returns

[`DocumentDelegate`](../namespaces/Prisma/interfaces/DocumentDelegate.md)\<`ExtArgs`\>

***

### documentTemplate

#### Get Signature

> **get** **documentTemplate**(): [`DocumentTemplateDelegate`](../namespaces/Prisma/interfaces/DocumentTemplateDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:323

`prisma.documentTemplate`: Exposes CRUD operations for the **DocumentTemplate** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more DocumentTemplates
 * const documentTemplates = await prisma.documentTemplate.findMany()
 * ```

##### Returns

[`DocumentTemplateDelegate`](../namespaces/Prisma/interfaces/DocumentTemplateDelegate.md)\<`ExtArgs`\>

***

### draft

#### Get Signature

> **get** **draft**(): [`DraftDelegate`](../namespaces/Prisma/interfaces/DraftDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:273

`prisma.draft`: Exposes CRUD operations for the **Draft** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Drafts
 * const drafts = await prisma.draft.findMany()
 * ```

##### Returns

[`DraftDelegate`](../namespaces/Prisma/interfaces/DraftDelegate.md)\<`ExtArgs`\>

***

### invitation

#### Get Signature

> **get** **invitation**(): [`InvitationDelegate`](../namespaces/Prisma/interfaces/InvitationDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:313

`prisma.invitation`: Exposes CRUD operations for the **Invitation** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Invitations
 * const invitations = await prisma.invitation.findMany()
 * ```

##### Returns

[`InvitationDelegate`](../namespaces/Prisma/interfaces/InvitationDelegate.md)\<`ExtArgs`\>

***

### pIIAuditLog

#### Get Signature

> **get** **pIIAuditLog**(): [`PIIAuditLogDelegate`](../namespaces/Prisma/interfaces/PIIAuditLogDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:363

`prisma.pIIAuditLog`: Exposes CRUD operations for the **PIIAuditLog** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more PIIAuditLogs
 * const pIIAuditLogs = await prisma.pIIAuditLog.findMany()
 * ```

##### Returns

[`PIIAuditLogDelegate`](../namespaces/Prisma/interfaces/PIIAuditLogDelegate.md)\<`ExtArgs`\>

***

### subscription

#### Get Signature

> **get** **subscription**(): [`SubscriptionDelegate`](../namespaces/Prisma/interfaces/SubscriptionDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:233

`prisma.subscription`: Exposes CRUD operations for the **Subscription** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Subscriptions
 * const subscriptions = await prisma.subscription.findMany()
 * ```

##### Returns

[`SubscriptionDelegate`](../namespaces/Prisma/interfaces/SubscriptionDelegate.md)\<`ExtArgs`\>

***

### templateVersion

#### Get Signature

> **get** **templateVersion**(): [`TemplateVersionDelegate`](../namespaces/Prisma/interfaces/TemplateVersionDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:333

`prisma.templateVersion`: Exposes CRUD operations for the **TemplateVersion** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more TemplateVersions
 * const templateVersions = await prisma.templateVersion.findMany()
 * ```

##### Returns

[`TemplateVersionDelegate`](../namespaces/Prisma/interfaces/TemplateVersionDelegate.md)\<`ExtArgs`\>

***

### tenant

#### Get Signature

> **get** **tenant**(): [`TenantDelegate`](../namespaces/Prisma/interfaces/TenantDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:223

`prisma.tenant`: Exposes CRUD operations for the **Tenant** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Tenants
 * const tenants = await prisma.tenant.findMany()
 * ```

##### Returns

[`TenantDelegate`](../namespaces/Prisma/interfaces/TenantDelegate.md)\<`ExtArgs`\>

***

### usage

#### Get Signature

> **get** **usage**(): [`UsageDelegate`](../namespaces/Prisma/interfaces/UsageDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:303

`prisma.usage`: Exposes CRUD operations for the **Usage** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Usages
 * const usages = await prisma.usage.findMany()
 * ```

##### Returns

[`UsageDelegate`](../namespaces/Prisma/interfaces/UsageDelegate.md)\<`ExtArgs`\>

***

### user

#### Get Signature

> **get** **user**(): [`UserDelegate`](../namespaces/Prisma/interfaces/UserDelegate.md)\<`ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:243

`prisma.user`: Exposes CRUD operations for the **User** model.
 * Example usage:
 * ```ts
 * // Fetch zero or more Users
 * const users = await prisma.user.findMany()
 * ```

##### Returns

[`UserDelegate`](../namespaces/Prisma/interfaces/UserDelegate.md)\<`ExtArgs`\>

## Methods

### $connect()

> **$connect**(): `Promise`\<`void`\>

Defined in: node\_modules/.prisma/client/index.d.ts:134

Connect with the database

#### Returns

`Promise`\<`void`\>

***

### $disconnect()

> **$disconnect**(): `Promise`\<`void`\>

Defined in: node\_modules/.prisma/client/index.d.ts:139

Disconnect from the database

#### Returns

`Promise`\<`void`\>

***

### $executeRaw()

> **$executeRaw**\<`T`\>(`query`, ...`values`): [`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:157

Executes a prepared raw query and returns the number of affected rows.

#### Type Parameters

##### T

`T` = `unknown`

#### Parameters

##### query

`TemplateStringsArray` | [`Sql`](../namespaces/Prisma/classes/Sql.md)

##### values

...`any`[]

#### Returns

[`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`number`\>

#### Example

```
const result = await prisma.$executeRaw`UPDATE User SET cool = ${true} WHERE email = ${'user@email.com'};`
```

Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client/raw-database-access).

***

### $executeRawUnsafe()

> **$executeRawUnsafe**\<`T`\>(`query`, ...`values`): [`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:169

Executes a raw query and returns the number of affected rows.
Susceptible to SQL injections, see documentation.

#### Type Parameters

##### T

`T` = `unknown`

#### Parameters

##### query

`string`

##### values

...`any`[]

#### Returns

[`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`number`\>

#### Example

```
const result = await prisma.$executeRawUnsafe('UPDATE User SET cool = $1 WHERE email = $2 ;', true, 'user@email.com')
```

Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client/raw-database-access).

***

### $on()

> **$on**\<`V`\>(`eventType`, `callback`): `void`

Defined in: node\_modules/.prisma/client/index.d.ts:129

#### Type Parameters

##### V

`V`

#### Parameters

##### eventType

`V`

##### callback

(`event`) => `void`

#### Returns

`void`

***

### $queryRaw()

> **$queryRaw**\<`T`\>(`query`, ...`values`): [`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`T`\>

Defined in: node\_modules/.prisma/client/index.d.ts:180

Performs a prepared raw query and returns the `SELECT` data.

#### Type Parameters

##### T

`T` = `unknown`

#### Parameters

##### query

`TemplateStringsArray` | [`Sql`](../namespaces/Prisma/classes/Sql.md)

##### values

...`any`[]

#### Returns

[`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`T`\>

#### Example

```
const result = await prisma.$queryRaw`SELECT * FROM User WHERE id = ${1} OR email = ${'user@email.com'};`
```

Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client/raw-database-access).

***

### $queryRawUnsafe()

> **$queryRawUnsafe**\<`T`\>(`query`, ...`values`): [`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`T`\>

Defined in: node\_modules/.prisma/client/index.d.ts:192

Performs a raw query and returns the `SELECT` data.
Susceptible to SQL injections, see documentation.

#### Type Parameters

##### T

`T` = `unknown`

#### Parameters

##### query

`string`

##### values

...`any`[]

#### Returns

[`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`T`\>

#### Example

```
const result = await prisma.$queryRawUnsafe('SELECT * FROM User WHERE id = $1 OR email = $2;', 1, 'user@email.com')
```

Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client/raw-database-access).

***

### $transaction()

#### Call Signature

> **$transaction**\<`P`\>(`arg`, `options?`): `Promise`\<`UnwrapTuple`\<`P`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:208

Allows the running of a sequence of read/write operations that are guaranteed to either succeed or fail as a whole.

##### Type Parameters

###### P

`P` *extends* [`PrismaPromise`](../namespaces/Prisma/type-aliases/PrismaPromise.md)\<`any`\>[]

##### Parameters

###### arg

\[`...P[]`\]

###### options?

###### isolationLevel?

[`TransactionIsolationLevel`](../namespaces/Prisma/type-aliases/TransactionIsolationLevel.md)

##### Returns

`Promise`\<`UnwrapTuple`\<`P`\>\>

##### Example

```
const [george, bob, alice] = await prisma.$transaction([
  prisma.user.create({ data: { name: 'George' } }),
  prisma.user.create({ data: { name: 'Bob' } }),
  prisma.user.create({ data: { name: 'Alice' } }),
])
```

Read more in our [docs](https://www.prisma.io/docs/concepts/components/prisma-client/transactions).

#### Call Signature

> **$transaction**\<`R`\>(`fn`, `options?`): `Promise`\<`R`\>

Defined in: node\_modules/.prisma/client/index.d.ts:210

Allows the running of a sequence of read/write operations that are guaranteed to either succeed or fail as a whole.

##### Type Parameters

###### R

`R`

##### Parameters

###### fn

(`prisma`) => `Promise`\<`R`\>

###### options?

###### isolationLevel?

[`TransactionIsolationLevel`](../namespaces/Prisma/type-aliases/TransactionIsolationLevel.md)

###### maxWait?

`number`

###### timeout?

`number`

##### Returns

`Promise`\<`R`\>

##### Example

```
const [george, bob, alice] = await prisma.$transaction([
  prisma.user.create({ data: { name: 'George' } }),
  prisma.user.create({ data: { name: 'Bob' } }),
  prisma.user.create({ data: { name: 'Alice' } }),
])
```

Read more in our [docs](https://www.prisma.io/docs/concepts/components/prisma-client/transactions).

***

### ~~$use()~~

> **$use**(`cb`): `void`

Defined in: node\_modules/.prisma/client/index.d.ts:146

Add a middleware

#### Parameters

##### cb

[`Middleware`](../namespaces/Prisma/type-aliases/Middleware.md)

#### Returns

`void`

#### Deprecated

since 4.16.0. For new code, prefer client extensions instead.

#### See

https://pris.ly/d/extensions

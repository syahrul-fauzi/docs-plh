[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / PrismaClientOptions

# Interface: PrismaClientOptions

Defined in: node\_modules/.prisma/client/index.d.ts:1916

## Properties

### datasources?

> `optional` **datasources**: [`Datasources`](../type-aliases/Datasources.md)

Defined in: node\_modules/.prisma/client/index.d.ts:1920

Overwrites the datasource url from your schema.prisma file

***

### datasourceUrl?

> `optional` **datasourceUrl**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:1924

Overwrites the datasource url from your schema.prisma file

***

### errorFormat?

> `optional` **errorFormat**: [`ErrorFormat`](../type-aliases/ErrorFormat.md)

Defined in: node\_modules/.prisma/client/index.d.ts:1928

#### Default

```ts
"colorless"
```

***

### log?

> `optional` **log**: ([`LogLevel`](../type-aliases/LogLevel.md) \| [`LogDefinition`](../type-aliases/LogDefinition.md))[]

Defined in: node\_modules/.prisma/client/index.d.ts:1945

#### Example

```
// Defaults to stdout
log: ['query', 'info', 'warn', 'error']

// Emit as events
log: [
  { emit: 'stdout', level: 'query' },
  { emit: 'stdout', level: 'info' },
  { emit: 'stdout', level: 'warn' }
  { emit: 'stdout', level: 'error' }
]
```
Read more in our [docs](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client/logging#the-log-option).

***

### transactionOptions?

> `optional` **transactionOptions**: `object`

Defined in: node\_modules/.prisma/client/index.d.ts:1951

The default values for transactionOptions
maxWait ?= 2000
timeout ?= 5000

#### isolationLevel?

> `optional` **isolationLevel**: [`TransactionIsolationLevel`](../type-aliases/TransactionIsolationLevel.md)

#### maxWait?

> `optional` **maxWait**: `number`

#### timeout?

> `optional` **timeout**: `number`

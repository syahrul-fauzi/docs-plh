[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
PIIAuditLogDelegate

# Interface: PIIAuditLogDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:17099

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`PIIAuditLogFieldRefs`](PIIAuditLogFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:17441

Fields of the PIIAuditLog model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetPIIAuditLogAggregateType`](../type-aliases/GetPIIAuditLogAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:17360

Allows you to perform aggregations operations on a PIIAuditLog. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogAggregateArgs`](../type-aliases/PIIAuditLogAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`PIIAuditLogAggregateArgs`](../type-aliases/PIIAuditLogAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetPIIAuditLogAggregateType`](../type-aliases/GetPIIAuditLogAggregateType.md)\<`T`\>\>

#### Example

```ts
// Ordered by age ascending
// Where email contains prisma.io
// Limited to the 10 users
const aggregations = await prisma.user.aggregate({
  _avg: {
    age: true,
  },
  where: {
    email: {
      contains: 'prisma.io',
    },
  },
  orderBy: {
    age: 'asc',
  },
  take: 10,
});
```

---

### count()

> **count**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
> `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
> `number` : \{ \[P in string \| number \| symbol\]: P extends keyof
> PIIAuditLogCountAggregateOutputType ?
> PIIAuditLogCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:17326

Count the number of PIIAuditLogs. Note, that providing `undefined` is treated as
the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogCountArgs`](../type-aliases/PIIAuditLogCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`PIIAuditLogCountArgs`](../type-aliases/PIIAuditLogCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter PIIAuditLogs to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
PIIAuditLogCountAggregateOutputType ?
PIIAuditLogCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of PIIAuditLogs
const count = await prisma.pIIAuditLog.count({
  where: {
    // ... the filter for the PIIAuditLogs we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17189

Create a PIIAuditLog.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogCreateArgs`](../type-aliases/PIIAuditLogCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogCreateArgs`](../type-aliases/PIIAuditLogCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a PIIAuditLog.

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one PIIAuditLog
const PIIAuditLog = await prisma.pIIAuditLog.create({
  data: {
    // ... data to create a PIIAuditLog
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17203

Create many PIIAuditLogs.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogCreateManyArgs`](../type-aliases/PIIAuditLogCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogCreateManyArgs`](../type-aliases/PIIAuditLogCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many PIIAuditLogs.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many PIIAuditLogs
const pIIAuditLog = await prisma.pIIAuditLog.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:17227

Create many PIIAuditLogs and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogCreateManyAndReturnArgs`](../type-aliases/PIIAuditLogCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogCreateManyAndReturnArgs`](../type-aliases/PIIAuditLogCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many PIIAuditLogs.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many PIIAuditLogs
const pIIAuditLog = await prisma.pIIAuditLog.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many PIIAuditLogs and only return the `id`
const pIIAuditLogWithIdOnly = await prisma.pIIAuditLog.createManyAndReturn({
  select: { id: true },
  data: [
    // ... provide data here
  ]
})
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined
```

---

### delete()

> **delete**\<`T`\>(`args`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17241

Delete a PIIAuditLog.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogDeleteArgs`](../type-aliases/PIIAuditLogDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogDeleteArgs`](../type-aliases/PIIAuditLogDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one PIIAuditLog.

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one PIIAuditLog
const PIIAuditLog = await prisma.pIIAuditLog.delete({
  where: {
    // ... filter to delete one PIIAuditLog
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17272

Delete zero or more PIIAuditLogs.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogDeleteManyArgs`](../type-aliases/PIIAuditLogDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogDeleteManyArgs`](../type-aliases/PIIAuditLogDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter PIIAuditLogs to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few PIIAuditLogs
const { count } = await prisma.pIIAuditLog.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17141

Find the first PIIAuditLog that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogFindFirstArgs`](../type-aliases/PIIAuditLogFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogFindFirstArgs`](../type-aliases/PIIAuditLogFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a PIIAuditLog

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one PIIAuditLog
const pIIAuditLog = await prisma.pIIAuditLog.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17157

Find the first PIIAuditLog that matches the filter or throw
`PrismaKnownClientError` with `P2025` code if no matches were found. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogFindFirstOrThrowArgs`](../type-aliases/PIIAuditLogFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogFindFirstOrThrowArgs`](../type-aliases/PIIAuditLogFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a PIIAuditLog

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one PIIAuditLog
const pIIAuditLog = await prisma.pIIAuditLog.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:17175

Find zero or more PIIAuditLogs that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogFindManyArgs`](../type-aliases/PIIAuditLogFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogFindManyArgs`](../type-aliases/PIIAuditLogFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all PIIAuditLogs
const pIIAuditLogs = await prisma.pIIAuditLog.findMany();

// Get first 10 PIIAuditLogs
const pIIAuditLogs = await prisma.pIIAuditLog.findMany({ take: 10 });

// Only select the `id`
const pIIAuditLogWithIdOnly = await prisma.pIIAuditLog.findMany({
  select: { id: true },
});
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17112

Find zero or one PIIAuditLog that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogFindUniqueArgs`](../type-aliases/PIIAuditLogFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogFindUniqueArgs`](../type-aliases/PIIAuditLogFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a PIIAuditLog

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one PIIAuditLog
const pIIAuditLog = await prisma.pIIAuditLog.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17126

Find one PIIAuditLog that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogFindUniqueOrThrowArgs`](../type-aliases/PIIAuditLogFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogFindUniqueOrThrowArgs`](../type-aliases/PIIAuditLogFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a PIIAuditLog

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one PIIAuditLog
const pIIAuditLog = await prisma.pIIAuditLog.findUniqueOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`,
> `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`):
> `object` _extends_ `InputErrors` ?
> [`GetPIIAuditLogGroupByPayload`](../type-aliases/GetPIIAuditLogGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:17380

Group by PIIAuditLog. Note, that providing `undefined` is treated as the value
not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogGroupByArgs`](../type-aliases/PIIAuditLogGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`PIIAuditLogOrderByWithAggregationInput`](../type-aliases/PIIAuditLogOrderByWithAggregationInput.md)
\|
[`PIIAuditLogOrderByWithAggregationInput`](../type-aliases/PIIAuditLogOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`PIIAuditLogOrderByWithAggregationInput`](../type-aliases/PIIAuditLogOrderByWithAggregationInput.md)
\|
[`PIIAuditLogOrderByWithAggregationInput`](../type-aliases/PIIAuditLogOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"tenantId"` \| `"metadata"` \| `"userId"` \|
`"piiType"` \| `"timestamp"` \| `"actionType"` \| `"isMasked"` \| `"riskScore"`
\| `"justification"` \| `"documentId"`

##### ByFields

`ByFields` _extends_
[`PIIAuditLogScalarFieldEnum`](../type-aliases/PIIAuditLogScalarFieldEnum.md)

##### ByValid

`ByValid` _extends_ `0` \| `1`

##### HavingFields

`HavingFields` _extends_ `string` \| `number` \| `symbol`

##### HavingValid

`HavingValid`

##### ByEmpty

`ByEmpty` _extends_ `0` \| `1`

##### InputErrors

`InputErrors`

#### Parameters

##### args

\{ \[key in string \| number \| symbol\]: key extends keyof
PIIAuditLogGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} &
`OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetPIIAuditLogGroupByPayload`](../type-aliases/GetPIIAuditLogGroupByPayload.md)\<`T`\>
: [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

#### Example

```ts
// Group by city, order by createdAt, get count
const result = await prisma.user.groupBy({
  by: ['city', 'createdAt'],
  orderBy: {
    createdAt: true,
  },
  _count: {
    _all: true,
  },
});
```

---

### update()

> **update**\<`T`\>(`args`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17258

Update one PIIAuditLog.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogUpdateArgs`](../type-aliases/PIIAuditLogUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogUpdateArgs`](../type-aliases/PIIAuditLogUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one PIIAuditLog.

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one PIIAuditLog
const pIIAuditLog = await prisma.pIIAuditLog.update({
  where: {
    // ... provide filter here
  },
  data: {
    // ... provide data here
  },
});
```

---

### updateMany()

> **updateMany**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:17291

Update zero or more PIIAuditLogs. Note, that providing `undefined` is treated as
the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogUpdateManyArgs`](../type-aliases/PIIAuditLogUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogUpdateManyArgs`](../type-aliases/PIIAuditLogUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many PIIAuditLogs
const pIIAuditLog = await prisma.pIIAuditLog.updateMany({
  where: {
    // ... provide filter here
  },
  data: {
    // ... provide data here
  },
});
```

---

### upsert()

> **upsert**\<`T`\>(`args`):
> [`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:17310

Create or update one PIIAuditLog.

#### Type Parameters

##### T

`T` _extends_
[`PIIAuditLogUpsertArgs`](../type-aliases/PIIAuditLogUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`PIIAuditLogUpsertArgs`](../type-aliases/PIIAuditLogUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a PIIAuditLog.

#### Returns

[`Prisma__PIIAuditLogClient`](Prisma__PIIAuditLogClient.md)\<`GetFindResult`\<[`$PIIAuditLogPayload`](../type-aliases/$PIIAuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a PIIAuditLog
const pIIAuditLog = await prisma.pIIAuditLog.upsert({
  create: {
    // ... data to create a PIIAuditLog
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the PIIAuditLog we want to update
  },
});
```

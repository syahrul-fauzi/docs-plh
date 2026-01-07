[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
AuditLogDelegate

# Interface: AuditLogDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:10051

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`AuditLogFieldRefs`](AuditLogFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:10393

Fields of the AuditLog model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetAuditLogAggregateType`](../type-aliases/GetAuditLogAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:10312

Allows you to perform aggregations operations on a AuditLog. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogAggregateArgs`](../type-aliases/AuditLogAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`AuditLogAggregateArgs`](../type-aliases/AuditLogAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetAuditLogAggregateType`](../type-aliases/GetAuditLogAggregateType.md)\<`T`\>\>

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
> AuditLogCountAggregateOutputType ? AuditLogCountAggregateOutputType\[P\<P\>\]
> : never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:10278

Count the number of AuditLogs. Note, that providing `undefined` is treated as
the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogCountArgs`](../type-aliases/AuditLogCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`AuditLogCountArgs`](../type-aliases/AuditLogCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter AuditLogs to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
AuditLogCountAggregateOutputType ? AuditLogCountAggregateOutputType\[P\<P\>\] :
never \} : `number`\>

#### Example

```ts
// Count the number of AuditLogs
const count = await prisma.auditLog.count({
  where: {
    // ... the filter for the AuditLogs we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10141

Create a AuditLog.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogCreateArgs`](../type-aliases/AuditLogCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogCreateArgs`](../type-aliases/AuditLogCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a AuditLog.

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one AuditLog
const AuditLog = await prisma.auditLog.create({
  data: {
    // ... data to create a AuditLog
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:10155

Create many AuditLogs.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogCreateManyArgs`](../type-aliases/AuditLogCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogCreateManyArgs`](../type-aliases/AuditLogCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many AuditLogs.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many AuditLogs
const auditLog = await prisma.auditLog.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:10179

Create many AuditLogs and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogCreateManyAndReturnArgs`](../type-aliases/AuditLogCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogCreateManyAndReturnArgs`](../type-aliases/AuditLogCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many AuditLogs.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many AuditLogs
const auditLog = await prisma.auditLog.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many AuditLogs and only return the `id`
const auditLogWithIdOnly = await prisma.auditLog.createManyAndReturn({
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
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10193

Delete a AuditLog.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogDeleteArgs`](../type-aliases/AuditLogDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogDeleteArgs`](../type-aliases/AuditLogDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one AuditLog.

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one AuditLog
const AuditLog = await prisma.auditLog.delete({
  where: {
    // ... filter to delete one AuditLog
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:10224

Delete zero or more AuditLogs.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogDeleteManyArgs`](../type-aliases/AuditLogDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogDeleteManyArgs`](../type-aliases/AuditLogDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter AuditLogs to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few AuditLogs
const { count } = await prisma.auditLog.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10093

Find the first AuditLog that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogFindFirstArgs`](../type-aliases/AuditLogFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogFindFirstArgs`](../type-aliases/AuditLogFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a AuditLog

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one AuditLog
const auditLog = await prisma.auditLog.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10109

Find the first AuditLog that matches the filter or throw
`PrismaKnownClientError` with `P2025` code if no matches were found. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogFindFirstOrThrowArgs`](../type-aliases/AuditLogFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogFindFirstOrThrowArgs`](../type-aliases/AuditLogFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a AuditLog

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one AuditLog
const auditLog = await prisma.auditLog.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:10127

Find zero or more AuditLogs that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogFindManyArgs`](../type-aliases/AuditLogFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogFindManyArgs`](../type-aliases/AuditLogFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all AuditLogs
const auditLogs = await prisma.auditLog.findMany();

// Get first 10 AuditLogs
const auditLogs = await prisma.auditLog.findMany({ take: 10 });

// Only select the `id`
const auditLogWithIdOnly = await prisma.auditLog.findMany({
  select: { id: true },
});
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10064

Find zero or one AuditLog that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogFindUniqueArgs`](../type-aliases/AuditLogFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogFindUniqueArgs`](../type-aliases/AuditLogFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a AuditLog

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one AuditLog
const auditLog = await prisma.auditLog.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10078

Find one AuditLog that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogFindUniqueOrThrowArgs`](../type-aliases/AuditLogFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogFindUniqueOrThrowArgs`](../type-aliases/AuditLogFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a AuditLog

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one AuditLog
const auditLog = await prisma.auditLog.findUniqueOrThrow({
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
> [`GetAuditLogGroupByPayload`](../type-aliases/GetAuditLogGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:10332

Group by AuditLog. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogGroupByArgs`](../type-aliases/AuditLogGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`AuditLogOrderByWithAggregationInput`](../type-aliases/AuditLogOrderByWithAggregationInput.md)
\|
[`AuditLogOrderByWithAggregationInput`](../type-aliases/AuditLogOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`AuditLogOrderByWithAggregationInput`](../type-aliases/AuditLogOrderByWithAggregationInput.md)
\|
[`AuditLogOrderByWithAggregationInput`](../type-aliases/AuditLogOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"tenantId"` \| `"metadata"`
\| `"userId"` \| `"action"` \| `"entityId"` \| `"entityType"`

##### ByFields

`ByFields` _extends_
[`AuditLogScalarFieldEnum`](../type-aliases/AuditLogScalarFieldEnum.md)

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
AuditLogGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetAuditLogGroupByPayload`](../type-aliases/GetAuditLogGroupByPayload.md)\<`T`\>
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
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10210

Update one AuditLog.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogUpdateArgs`](../type-aliases/AuditLogUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogUpdateArgs`](../type-aliases/AuditLogUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one AuditLog.

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one AuditLog
const auditLog = await prisma.auditLog.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:10243

Update zero or more AuditLogs. Note, that providing `undefined` is treated as
the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`AuditLogUpdateManyArgs`](../type-aliases/AuditLogUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogUpdateManyArgs`](../type-aliases/AuditLogUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many AuditLogs
const auditLog = await prisma.auditLog.updateMany({
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
> [`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:10262

Create or update one AuditLog.

#### Type Parameters

##### T

`T` _extends_
[`AuditLogUpsertArgs`](../type-aliases/AuditLogUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`AuditLogUpsertArgs`](../type-aliases/AuditLogUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a AuditLog.

#### Returns

[`Prisma__AuditLogClient`](Prisma__AuditLogClient.md)\<`GetFindResult`\<[`$AuditLogPayload`](../type-aliases/$AuditLogPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a AuditLog
const auditLog = await prisma.auditLog.upsert({
  create: {
    // ... data to create a AuditLog
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the AuditLog we want to update
  },
});
```

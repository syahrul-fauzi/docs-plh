[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UsageDelegate

# Interface: UsageDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:11029

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`UsageFieldRefs`](UsageFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:11371

Fields of the Usage model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetUsageAggregateType`](../type-aliases/GetUsageAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:11290

Allows you to perform aggregations operations on a Usage. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageAggregateArgs`](../type-aliases/UsageAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`UsageAggregateArgs`](../type-aliases/UsageAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetUsageAggregateType`](../type-aliases/GetUsageAggregateType.md)\<`T`\>\>

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
> UsageCountAggregateOutputType ? UsageCountAggregateOutputType\[P\<P\>\] :
> never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:11256

Count the number of Usages. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageCountArgs`](../type-aliases/UsageCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`UsageCountArgs`](../type-aliases/UsageCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Usages to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
UsageCountAggregateOutputType ? UsageCountAggregateOutputType\[P\<P\>\] : never
\} : `number`\>

#### Example

```ts
// Count the number of Usages
const count = await prisma.usage.count({
  where: {
    // ... the filter for the Usages we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11119

Create a Usage.

#### Type Parameters

##### T

`T` _extends_
[`UsageCreateArgs`](../type-aliases/UsageCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageCreateArgs`](../type-aliases/UsageCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Usage.

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Usage
const Usage = await prisma.usage.create({
  data: {
    // ... data to create a Usage
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:11133

Create many Usages.

#### Type Parameters

##### T

`T` _extends_
[`UsageCreateManyArgs`](../type-aliases/UsageCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageCreateManyArgs`](../type-aliases/UsageCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Usages.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Usages
const usage = await prisma.usage.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:11157

Create many Usages and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`UsageCreateManyAndReturnArgs`](../type-aliases/UsageCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageCreateManyAndReturnArgs`](../type-aliases/UsageCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Usages.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Usages
const usage = await prisma.usage.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Usages and only return the `id`
const usageWithIdOnly = await prisma.usage.createManyAndReturn({
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
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11171

Delete a Usage.

#### Type Parameters

##### T

`T` _extends_
[`UsageDeleteArgs`](../type-aliases/UsageDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageDeleteArgs`](../type-aliases/UsageDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Usage.

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Usage
const Usage = await prisma.usage.delete({
  where: {
    // ... filter to delete one Usage
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:11202

Delete zero or more Usages.

#### Type Parameters

##### T

`T` _extends_
[`UsageDeleteManyArgs`](../type-aliases/UsageDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageDeleteManyArgs`](../type-aliases/UsageDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Usages to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Usages
const { count } = await prisma.usage.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11071

Find the first Usage that matches the filter. Note, that providing `undefined`
is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageFindFirstArgs`](../type-aliases/UsageFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageFindFirstArgs`](../type-aliases/UsageFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Usage

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Usage
const usage = await prisma.usage.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11087

Find the first Usage that matches the filter or throw `PrismaKnownClientError`
with `P2025` code if no matches were found. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageFindFirstOrThrowArgs`](../type-aliases/UsageFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageFindFirstOrThrowArgs`](../type-aliases/UsageFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Usage

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Usage
const usage = await prisma.usage.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:11105

Find zero or more Usages that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageFindManyArgs`](../type-aliases/UsageFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageFindManyArgs`](../type-aliases/UsageFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Usages
const usages = await prisma.usage.findMany();

// Get first 10 Usages
const usages = await prisma.usage.findMany({ take: 10 });

// Only select the `id`
const usageWithIdOnly = await prisma.usage.findMany({ select: { id: true } });
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11042

Find zero or one Usage that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`UsageFindUniqueArgs`](../type-aliases/UsageFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageFindUniqueArgs`](../type-aliases/UsageFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Usage

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Usage
const usage = await prisma.usage.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11056

Find one Usage that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`UsageFindUniqueOrThrowArgs`](../type-aliases/UsageFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageFindUniqueOrThrowArgs`](../type-aliases/UsageFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Usage

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Usage
const usage = await prisma.usage.findUniqueOrThrow({
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
> [`GetUsageGroupByPayload`](../type-aliases/GetUsageGroupByPayload.md)\<`T`\> :
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:11310

Group by Usage. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageGroupByArgs`](../type-aliases/UsageGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`UsageOrderByWithAggregationInput`](../type-aliases/UsageOrderByWithAggregationInput.md)
\|
[`UsageOrderByWithAggregationInput`](../type-aliases/UsageOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`UsageOrderByWithAggregationInput`](../type-aliases/UsageOrderByWithAggregationInput.md)
\|
[`UsageOrderByWithAggregationInput`](../type-aliases/UsageOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"tenantId"` \| `"metadata"`
\| `"type"` \| `"amount"`

##### ByFields

`ByFields` _extends_
[`UsageScalarFieldEnum`](../type-aliases/UsageScalarFieldEnum.md)

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
UsageGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetUsageGroupByPayload`](../type-aliases/GetUsageGroupByPayload.md)\<`T`\> :
[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

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
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11188

Update one Usage.

#### Type Parameters

##### T

`T` _extends_
[`UsageUpdateArgs`](../type-aliases/UsageUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageUpdateArgs`](../type-aliases/UsageUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Usage.

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Usage
const usage = await prisma.usage.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:11221

Update zero or more Usages. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UsageUpdateManyArgs`](../type-aliases/UsageUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageUpdateManyArgs`](../type-aliases/UsageUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Usages
const usage = await prisma.usage.updateMany({
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
> [`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:11240

Create or update one Usage.

#### Type Parameters

##### T

`T` _extends_
[`UsageUpsertArgs`](../type-aliases/UsageUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UsageUpsertArgs`](../type-aliases/UsageUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Usage.

#### Returns

[`Prisma__UsageClient`](Prisma__UsageClient.md)\<`GetFindResult`\<[`$UsagePayload`](../type-aliases/$UsagePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Usage
const usage = await prisma.usage.upsert({
  create: {
    // ... data to create a Usage
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Usage we want to update
  },
});
```

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseDelegate

# Interface: CaseDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:5950

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`CaseFieldRefs`](CaseFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:6292

Fields of the Case model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetCaseAggregateType`](../type-aliases/GetCaseAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:6211

Allows you to perform aggregations operations on a Case. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseAggregateArgs`](../type-aliases/CaseAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`CaseAggregateArgs`](../type-aliases/CaseAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetCaseAggregateType`](../type-aliases/GetCaseAggregateType.md)\<`T`\>\>

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
> CaseCountAggregateOutputType ? CaseCountAggregateOutputType\[P\<P\>\] : never
> \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:6177

Count the number of Cases. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseCountArgs`](../type-aliases/CaseCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`CaseCountArgs`](../type-aliases/CaseCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Cases to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
CaseCountAggregateOutputType ? CaseCountAggregateOutputType\[P\<P\>\] : never \}
: `number`\>

#### Example

```ts
// Count the number of Cases
const count = await prisma.case.count({
  where: {
    // ... the filter for the Cases we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:6040

Create a Case.

#### Type Parameters

##### T

`T` _extends_
[`CaseCreateArgs`](../type-aliases/CaseCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseCreateArgs`](../type-aliases/CaseCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Case.

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Case
const Case = await prisma.case.create({
  data: {
    // ... data to create a Case
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:6054

Create many Cases.

#### Type Parameters

##### T

`T` _extends_
[`CaseCreateManyArgs`](../type-aliases/CaseCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseCreateManyArgs`](../type-aliases/CaseCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Cases.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Cases
const case = await prisma.case.createMany({
  data: [
    // ... provide data here
  ]
})
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:6078

Create many Cases and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`CaseCreateManyAndReturnArgs`](../type-aliases/CaseCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseCreateManyAndReturnArgs`](../type-aliases/CaseCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Cases.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Cases
const case = await prisma.case.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Cases and only return the `id`
const caseWithIdOnly = await prisma.case.createManyAndReturn({
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
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:6092

Delete a Case.

#### Type Parameters

##### T

`T` _extends_
[`CaseDeleteArgs`](../type-aliases/CaseDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseDeleteArgs`](../type-aliases/CaseDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Case.

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Case
const Case = await prisma.case.delete({
  where: {
    // ... filter to delete one Case
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:6123

Delete zero or more Cases.

#### Type Parameters

##### T

`T` _extends_
[`CaseDeleteManyArgs`](../type-aliases/CaseDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseDeleteManyArgs`](../type-aliases/CaseDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Cases to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Cases
const { count } = await prisma.case.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:5992

Find the first Case that matches the filter. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseFindFirstArgs`](../type-aliases/CaseFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseFindFirstArgs`](../type-aliases/CaseFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Case

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Case
const case = await prisma.case.findFirst({
  where: {
    // ... provide filter here
  }
})
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:6008

Find the first Case that matches the filter or throw `PrismaKnownClientError`
with `P2025` code if no matches were found. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseFindFirstOrThrowArgs`](../type-aliases/CaseFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseFindFirstOrThrowArgs`](../type-aliases/CaseFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Case

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Case
const case = await prisma.case.findFirstOrThrow({
  where: {
    // ... provide filter here
  }
})
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:6026

Find zero or more Cases that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseFindManyArgs`](../type-aliases/CaseFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseFindManyArgs`](../type-aliases/CaseFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Cases
const cases = await prisma.case.findMany();

// Get first 10 Cases
const cases = await prisma.case.findMany({ take: 10 });

// Only select the `id`
const caseWithIdOnly = await prisma.case.findMany({ select: { id: true } });
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:5963

Find zero or one Case that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`CaseFindUniqueArgs`](../type-aliases/CaseFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseFindUniqueArgs`](../type-aliases/CaseFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Case

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Case
const case = await prisma.case.findUnique({
  where: {
    // ... provide filter here
  }
})
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:5977

Find one Case that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`CaseFindUniqueOrThrowArgs`](../type-aliases/CaseFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseFindUniqueOrThrowArgs`](../type-aliases/CaseFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Case

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Case
const case = await prisma.case.findUniqueOrThrow({
  where: {
    // ... provide filter here
  }
})
```

---

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`,
> `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`):
> `object` _extends_ `InputErrors` ?
> [`GetCaseGroupByPayload`](../type-aliases/GetCaseGroupByPayload.md)\<`T`\> :
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:6231

Group by Case. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseGroupByArgs`](../type-aliases/CaseGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`CaseOrderByWithAggregationInput`](../type-aliases/CaseOrderByWithAggregationInput.md)
\|
[`CaseOrderByWithAggregationInput`](../type-aliases/CaseOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`CaseOrderByWithAggregationInput`](../type-aliases/CaseOrderByWithAggregationInput.md)
\|
[`CaseOrderByWithAggregationInput`](../type-aliases/CaseOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"`
\| `"status"` \| `"title"` \| `"description"`

##### ByFields

`ByFields` _extends_
[`CaseScalarFieldEnum`](../type-aliases/CaseScalarFieldEnum.md)

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
CaseGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetCaseGroupByPayload`](../type-aliases/GetCaseGroupByPayload.md)\<`T`\> :
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
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:6109

Update one Case.

#### Type Parameters

##### T

`T` _extends_
[`CaseUpdateArgs`](../type-aliases/CaseUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseUpdateArgs`](../type-aliases/CaseUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Case.

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Case
const case = await prisma.case.update({
  where: {
    // ... provide filter here
  },
  data: {
    // ... provide data here
  }
})
```

---

### updateMany()

> **updateMany**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:6142

Update zero or more Cases. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CaseUpdateManyArgs`](../type-aliases/CaseUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseUpdateManyArgs`](../type-aliases/CaseUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Cases
const case = await prisma.case.updateMany({
  where: {
    // ... provide filter here
  },
  data: {
    // ... provide data here
  }
})
```

---

### upsert()

> **upsert**\<`T`\>(`args`):
> [`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:6161

Create or update one Case.

#### Type Parameters

##### T

`T` _extends_
[`CaseUpsertArgs`](../type-aliases/CaseUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CaseUpsertArgs`](../type-aliases/CaseUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Case.

#### Returns

[`Prisma__CaseClient`](Prisma__CaseClient.md)\<`GetFindResult`\<[`$CasePayload`](../type-aliases/$CasePayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Case
const case = await prisma.case.upsert({
  create: {
    // ... data to create a Case
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Case we want to update
  }
})
```

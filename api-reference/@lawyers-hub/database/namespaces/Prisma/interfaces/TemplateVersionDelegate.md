[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TemplateVersionDelegate

# Interface: TemplateVersionDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:13988

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**:
> [`TemplateVersionFieldRefs`](TemplateVersionFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:14330

Fields of the TemplateVersion model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetTemplateVersionAggregateType`](../type-aliases/GetTemplateVersionAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:14249

Allows you to perform aggregations operations on a TemplateVersion. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionAggregateArgs`](../type-aliases/TemplateVersionAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`TemplateVersionAggregateArgs`](../type-aliases/TemplateVersionAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetTemplateVersionAggregateType`](../type-aliases/GetTemplateVersionAggregateType.md)\<`T`\>\>

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
> TemplateVersionCountAggregateOutputType ?
> TemplateVersionCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:14215

Count the number of TemplateVersions. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionCountArgs`](../type-aliases/TemplateVersionCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`TemplateVersionCountArgs`](../type-aliases/TemplateVersionCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter TemplateVersions to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
TemplateVersionCountAggregateOutputType ?
TemplateVersionCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of TemplateVersions
const count = await prisma.templateVersion.count({
  where: {
    // ... the filter for the TemplateVersions we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14078

Create a TemplateVersion.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionCreateArgs`](../type-aliases/TemplateVersionCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionCreateArgs`](../type-aliases/TemplateVersionCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a TemplateVersion.

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one TemplateVersion
const TemplateVersion = await prisma.templateVersion.create({
  data: {
    // ... data to create a TemplateVersion
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:14092

Create many TemplateVersions.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionCreateManyArgs`](../type-aliases/TemplateVersionCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionCreateManyArgs`](../type-aliases/TemplateVersionCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many TemplateVersions.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many TemplateVersions
const templateVersion = await prisma.templateVersion.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:14116

Create many TemplateVersions and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionCreateManyAndReturnArgs`](../type-aliases/TemplateVersionCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionCreateManyAndReturnArgs`](../type-aliases/TemplateVersionCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many TemplateVersions.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many TemplateVersions
const templateVersion = await prisma.templateVersion.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many TemplateVersions and only return the `id`
const templateVersionWithIdOnly = await prisma.templateVersion.createManyAndReturn({
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
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14130

Delete a TemplateVersion.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionDeleteArgs`](../type-aliases/TemplateVersionDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionDeleteArgs`](../type-aliases/TemplateVersionDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one TemplateVersion.

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one TemplateVersion
const TemplateVersion = await prisma.templateVersion.delete({
  where: {
    // ... filter to delete one TemplateVersion
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:14161

Delete zero or more TemplateVersions.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionDeleteManyArgs`](../type-aliases/TemplateVersionDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionDeleteManyArgs`](../type-aliases/TemplateVersionDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter TemplateVersions to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few TemplateVersions
const { count } = await prisma.templateVersion.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14030

Find the first TemplateVersion that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionFindFirstArgs`](../type-aliases/TemplateVersionFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionFindFirstArgs`](../type-aliases/TemplateVersionFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a TemplateVersion

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one TemplateVersion
const templateVersion = await prisma.templateVersion.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14046

Find the first TemplateVersion that matches the filter or throw
`PrismaKnownClientError` with `P2025` code if no matches were found. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionFindFirstOrThrowArgs`](../type-aliases/TemplateVersionFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionFindFirstOrThrowArgs`](../type-aliases/TemplateVersionFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a TemplateVersion

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one TemplateVersion
const templateVersion = await prisma.templateVersion.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:14064

Find zero or more TemplateVersions that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionFindManyArgs`](../type-aliases/TemplateVersionFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionFindManyArgs`](../type-aliases/TemplateVersionFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all TemplateVersions
const templateVersions = await prisma.templateVersion.findMany();

// Get first 10 TemplateVersions
const templateVersions = await prisma.templateVersion.findMany({ take: 10 });

// Only select the `id`
const templateVersionWithIdOnly = await prisma.templateVersion.findMany({
  select: { id: true },
});
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14001

Find zero or one TemplateVersion that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionFindUniqueArgs`](../type-aliases/TemplateVersionFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionFindUniqueArgs`](../type-aliases/TemplateVersionFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a TemplateVersion

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one TemplateVersion
const templateVersion = await prisma.templateVersion.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14015

Find one TemplateVersion that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionFindUniqueOrThrowArgs`](../type-aliases/TemplateVersionFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionFindUniqueOrThrowArgs`](../type-aliases/TemplateVersionFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a TemplateVersion

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one TemplateVersion
const templateVersion = await prisma.templateVersion.findUniqueOrThrow({
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
> [`GetTemplateVersionGroupByPayload`](../type-aliases/GetTemplateVersionGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:14269

Group by TemplateVersion. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionGroupByArgs`](../type-aliases/TemplateVersionGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`TemplateVersionOrderByWithAggregationInput`](../type-aliases/TemplateVersionOrderByWithAggregationInput.md)
\|
[`TemplateVersionOrderByWithAggregationInput`](../type-aliases/TemplateVersionOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`TemplateVersionOrderByWithAggregationInput`](../type-aliases/TemplateVersionOrderByWithAggregationInput.md)
\|
[`TemplateVersionOrderByWithAggregationInput`](../type-aliases/TemplateVersionOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"content"` \| `"userId"` \|
`"templateId"` \| `"version"` \| `"changeLog"`

##### ByFields

`ByFields` _extends_
[`TemplateVersionScalarFieldEnum`](../type-aliases/TemplateVersionScalarFieldEnum.md)

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
TemplateVersionGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} &
`OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetTemplateVersionGroupByPayload`](../type-aliases/GetTemplateVersionGroupByPayload.md)\<`T`\>
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
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14147

Update one TemplateVersion.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionUpdateArgs`](../type-aliases/TemplateVersionUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionUpdateArgs`](../type-aliases/TemplateVersionUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one TemplateVersion.

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one TemplateVersion
const templateVersion = await prisma.templateVersion.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:14180

Update zero or more TemplateVersions. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionUpdateManyArgs`](../type-aliases/TemplateVersionUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionUpdateManyArgs`](../type-aliases/TemplateVersionUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many TemplateVersions
const templateVersion = await prisma.templateVersion.updateMany({
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
> [`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:14199

Create or update one TemplateVersion.

#### Type Parameters

##### T

`T` _extends_
[`TemplateVersionUpsertArgs`](../type-aliases/TemplateVersionUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TemplateVersionUpsertArgs`](../type-aliases/TemplateVersionUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a TemplateVersion.

#### Returns

[`Prisma__TemplateVersionClient`](Prisma__TemplateVersionClient.md)\<`GetFindResult`\<[`$TemplateVersionPayload`](../type-aliases/$TemplateVersionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a TemplateVersion
const templateVersion = await prisma.templateVersion.upsert({
  create: {
    // ... data to create a TemplateVersion
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the TemplateVersion we want to update
  },
});
```

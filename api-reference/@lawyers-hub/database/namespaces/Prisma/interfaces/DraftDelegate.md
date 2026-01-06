[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DraftDelegate

# Interface: DraftDelegate\<ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:8025

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`DraftFieldRefs`](DraftFieldRefs.md)

Defined in: node\_modules/.prisma/client/index.d.ts:8367

Fields of the Draft model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetDraftAggregateType`](../type-aliases/GetDraftAggregateType.md)\<`T`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:8286

Allows you to perform aggregations operations on a Draft.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftAggregateArgs`](../type-aliases/DraftAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`, [`DraftAggregateArgs`](../type-aliases/DraftAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetDraftAggregateType`](../type-aliases/GetDraftAggregateType.md)\<`T`\>\>

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
      contains: "prisma.io",
    },
  },
  orderBy: {
    age: "asc",
  },
  take: 10,
})
```

***

### count()

> **count**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof DraftCountAggregateOutputType ? DraftCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8252

Count the number of Drafts.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftCountArgs`](../type-aliases/DraftCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`DraftCountArgs`](../type-aliases/DraftCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Drafts to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof DraftCountAggregateOutputType ? DraftCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of Drafts
const count = await prisma.draft.count({
  where: {
    // ... the filter for the Drafts we want to count
  }
})
```

***

### create()

> **create**\<`T`\>(`args`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8115

Create a Draft.

#### Type Parameters

##### T

`T` *extends* [`DraftCreateArgs`](../type-aliases/DraftCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftCreateArgs`](../type-aliases/DraftCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Draft.

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Draft
const Draft = await prisma.draft.create({
  data: {
    // ... data to create a Draft
  }
})
```

***

### createMany()

> **createMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:8129

Create many Drafts.

#### Type Parameters

##### T

`T` *extends* [`DraftCreateManyArgs`](../type-aliases/DraftCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftCreateManyArgs`](../type-aliases/DraftCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Drafts.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Drafts
const draft = await prisma.draft.createMany({
  data: [
    // ... provide data here
  ]
})
```

***

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:8153

Create many Drafts and returns the data saved in the database.

#### Type Parameters

##### T

`T` *extends* [`DraftCreateManyAndReturnArgs`](../type-aliases/DraftCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftCreateManyAndReturnArgs`](../type-aliases/DraftCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Drafts.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Create many Drafts
const draft = await prisma.draft.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Drafts and only return the `id`
const draftWithIdOnly = await prisma.draft.createManyAndReturn({ 
  select: { id: true },
  data: [
    // ... provide data here
  ]
})
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined
```

***

### delete()

> **delete**\<`T`\>(`args`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8167

Delete a Draft.

#### Type Parameters

##### T

`T` *extends* [`DraftDeleteArgs`](../type-aliases/DraftDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftDeleteArgs`](../type-aliases/DraftDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Draft.

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Draft
const Draft = await prisma.draft.delete({
  where: {
    // ... filter to delete one Draft
  }
})
```

***

### deleteMany()

> **deleteMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:8198

Delete zero or more Drafts.

#### Type Parameters

##### T

`T` *extends* [`DraftDeleteManyArgs`](../type-aliases/DraftDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftDeleteManyArgs`](../type-aliases/DraftDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Drafts to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Drafts
const { count } = await prisma.draft.deleteMany({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirst()

> **findFirst**\<`T`\>(`args?`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8067

Find the first Draft that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftFindFirstArgs`](../type-aliases/DraftFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftFindFirstArgs`](../type-aliases/DraftFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Draft

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Draft
const draft = await prisma.draft.findFirst({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8083

Find the first Draft that matches the filter or
throw `PrismaKnownClientError` with `P2025` code if no matches were found.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftFindFirstOrThrowArgs`](../type-aliases/DraftFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftFindFirstOrThrowArgs`](../type-aliases/DraftFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Draft

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Draft
const draft = await prisma.draft.findFirstOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### findMany()

> **findMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:8101

Find zero or more Drafts that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftFindManyArgs`](../type-aliases/DraftFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftFindManyArgs`](../type-aliases/DraftFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Get all Drafts
const drafts = await prisma.draft.findMany()

// Get first 10 Drafts
const drafts = await prisma.draft.findMany({ take: 10 })

// Only select the `id`
const draftWithIdOnly = await prisma.draft.findMany({ select: { id: true } })
```

***

### findUnique()

> **findUnique**\<`T`\>(`args`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8038

Find zero or one Draft that matches the filter.

#### Type Parameters

##### T

`T` *extends* [`DraftFindUniqueArgs`](../type-aliases/DraftFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftFindUniqueArgs`](../type-aliases/DraftFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Draft

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Draft
const draft = await prisma.draft.findUnique({
  where: {
    // ... provide filter here
  }
})
```

***

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8052

Find one Draft that matches the filter or throw an error with `error.code='P2025'` 
if no matches were found.

#### Type Parameters

##### T

`T` *extends* [`DraftFindUniqueOrThrowArgs`](../type-aliases/DraftFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftFindUniqueOrThrowArgs`](../type-aliases/DraftFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Draft

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Draft
const draft = await prisma.draft.findUniqueOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`, `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`): `object` *extends* `InputErrors` ? [`GetDraftGroupByPayload`](../type-aliases/GetDraftGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8306

Group by Draft.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftGroupByArgs`](../type-aliases/DraftGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` *extends* `0` \| `1`

##### OrderByArg

`OrderByArg` *extends* \{ `orderBy`: [`DraftOrderByWithAggregationInput`](../type-aliases/DraftOrderByWithAggregationInput.md) \| [`DraftOrderByWithAggregationInput`](../type-aliases/DraftOrderByWithAggregationInput.md)[] \| `undefined`; \} \| \{ `orderBy?`: [`DraftOrderByWithAggregationInput`](../type-aliases/DraftOrderByWithAggregationInput.md) \| [`DraftOrderByWithAggregationInput`](../type-aliases/DraftOrderByWithAggregationInput.md)[]; \}

##### OrderFields

`OrderFields` *extends* `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"` \| `"status"` \| `"title"` \| `"content"` \| `"caseId"` \| `"templateType"` \| `"metadata"`

##### ByFields

`ByFields` *extends* [`DraftScalarFieldEnum`](../type-aliases/DraftScalarFieldEnum.md)

##### ByValid

`ByValid` *extends* `0` \| `1`

##### HavingFields

`HavingFields` *extends* `string` \| `number` \| `symbol`

##### HavingValid

`HavingValid`

##### ByEmpty

`ByEmpty` *extends* `0` \| `1`

##### InputErrors

`InputErrors`

#### Parameters

##### args

\{ \[key in string \| number \| symbol\]: key extends keyof DraftGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` *extends* `InputErrors` ? [`GetDraftGroupByPayload`](../type-aliases/GetDraftGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

#### Example

```ts
// Group by city, order by createdAt, get count
const result = await prisma.user.groupBy({
  by: ['city', 'createdAt'],
  orderBy: {
    createdAt: true
  },
  _count: {
    _all: true
  },
})
```

***

### update()

> **update**\<`T`\>(`args`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8184

Update one Draft.

#### Type Parameters

##### T

`T` *extends* [`DraftUpdateArgs`](../type-aliases/DraftUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftUpdateArgs`](../type-aliases/DraftUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Draft.

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Draft
const draft = await prisma.draft.update({
  where: {
    // ... provide filter here
  },
  data: {
    // ... provide data here
  }
})
```

***

### updateMany()

> **updateMany**\<`T`\>(`args`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:8217

Update zero or more Drafts.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DraftUpdateManyArgs`](../type-aliases/DraftUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftUpdateManyArgs`](../type-aliases/DraftUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Drafts
const draft = await prisma.draft.updateMany({
  where: {
    // ... provide filter here
  },
  data: {
    // ... provide data here
  }
})
```

***

### upsert()

> **upsert**\<`T`\>(`args`): [`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:8236

Create or update one Draft.

#### Type Parameters

##### T

`T` *extends* [`DraftUpsertArgs`](../type-aliases/DraftUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DraftUpsertArgs`](../type-aliases/DraftUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Draft.

#### Returns

[`Prisma__DraftClient`](Prisma__DraftClient.md)\<`GetFindResult`\<[`$DraftPayload`](../type-aliases/$DraftPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Draft
const draft = await prisma.draft.upsert({
  create: {
    // ... data to create a Draft
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Draft we want to update
  }
})
```

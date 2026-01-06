[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewDelegate

# Interface: ComplianceReviewDelegate\<ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:16050

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`ComplianceReviewFieldRefs`](ComplianceReviewFieldRefs.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16392

Fields of the ComplianceReview model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetComplianceReviewAggregateType`](../type-aliases/GetComplianceReviewAggregateType.md)\<`T`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:16311

Allows you to perform aggregations operations on a ComplianceReview.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewAggregateArgs`](../type-aliases/ComplianceReviewAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`, [`ComplianceReviewAggregateArgs`](../type-aliases/ComplianceReviewAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetComplianceReviewAggregateType`](../type-aliases/GetComplianceReviewAggregateType.md)\<`T`\>\>

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

> **count**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof ComplianceReviewCountAggregateOutputType ? ComplianceReviewCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16277

Count the number of ComplianceReviews.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewCountArgs`](../type-aliases/ComplianceReviewCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`ComplianceReviewCountArgs`](../type-aliases/ComplianceReviewCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter ComplianceReviews to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof ComplianceReviewCountAggregateOutputType ? ComplianceReviewCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of ComplianceReviews
const count = await prisma.complianceReview.count({
  where: {
    // ... the filter for the ComplianceReviews we want to count
  }
})
```

***

### create()

> **create**\<`T`\>(`args`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16140

Create a ComplianceReview.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewCreateArgs`](../type-aliases/ComplianceReviewCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewCreateArgs`](../type-aliases/ComplianceReviewCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a ComplianceReview.

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one ComplianceReview
const ComplianceReview = await prisma.complianceReview.create({
  data: {
    // ... data to create a ComplianceReview
  }
})
```

***

### createMany()

> **createMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:16154

Create many ComplianceReviews.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewCreateManyArgs`](../type-aliases/ComplianceReviewCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewCreateManyArgs`](../type-aliases/ComplianceReviewCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many ComplianceReviews.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many ComplianceReviews
const complianceReview = await prisma.complianceReview.createMany({
  data: [
    // ... provide data here
  ]
})
```

***

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:16178

Create many ComplianceReviews and returns the data saved in the database.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewCreateManyAndReturnArgs`](../type-aliases/ComplianceReviewCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewCreateManyAndReturnArgs`](../type-aliases/ComplianceReviewCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many ComplianceReviews.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Create many ComplianceReviews
const complianceReview = await prisma.complianceReview.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many ComplianceReviews and only return the `id`
const complianceReviewWithIdOnly = await prisma.complianceReview.createManyAndReturn({ 
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

> **delete**\<`T`\>(`args`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16192

Delete a ComplianceReview.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewDeleteArgs`](../type-aliases/ComplianceReviewDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewDeleteArgs`](../type-aliases/ComplianceReviewDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one ComplianceReview.

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one ComplianceReview
const ComplianceReview = await prisma.complianceReview.delete({
  where: {
    // ... filter to delete one ComplianceReview
  }
})
```

***

### deleteMany()

> **deleteMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:16223

Delete zero or more ComplianceReviews.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewDeleteManyArgs`](../type-aliases/ComplianceReviewDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewDeleteManyArgs`](../type-aliases/ComplianceReviewDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter ComplianceReviews to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few ComplianceReviews
const { count } = await prisma.complianceReview.deleteMany({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirst()

> **findFirst**\<`T`\>(`args?`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16092

Find the first ComplianceReview that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewFindFirstArgs`](../type-aliases/ComplianceReviewFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewFindFirstArgs`](../type-aliases/ComplianceReviewFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a ComplianceReview

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one ComplianceReview
const complianceReview = await prisma.complianceReview.findFirst({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16108

Find the first ComplianceReview that matches the filter or
throw `PrismaKnownClientError` with `P2025` code if no matches were found.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewFindFirstOrThrowArgs`](../type-aliases/ComplianceReviewFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewFindFirstOrThrowArgs`](../type-aliases/ComplianceReviewFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a ComplianceReview

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one ComplianceReview
const complianceReview = await prisma.complianceReview.findFirstOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### findMany()

> **findMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:16126

Find zero or more ComplianceReviews that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewFindManyArgs`](../type-aliases/ComplianceReviewFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewFindManyArgs`](../type-aliases/ComplianceReviewFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Get all ComplianceReviews
const complianceReviews = await prisma.complianceReview.findMany()

// Get first 10 ComplianceReviews
const complianceReviews = await prisma.complianceReview.findMany({ take: 10 })

// Only select the `id`
const complianceReviewWithIdOnly = await prisma.complianceReview.findMany({ select: { id: true } })
```

***

### findUnique()

> **findUnique**\<`T`\>(`args`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16063

Find zero or one ComplianceReview that matches the filter.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewFindUniqueArgs`](../type-aliases/ComplianceReviewFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewFindUniqueArgs`](../type-aliases/ComplianceReviewFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a ComplianceReview

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one ComplianceReview
const complianceReview = await prisma.complianceReview.findUnique({
  where: {
    // ... provide filter here
  }
})
```

***

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16077

Find one ComplianceReview that matches the filter or throw an error with `error.code='P2025'` 
if no matches were found.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewFindUniqueOrThrowArgs`](../type-aliases/ComplianceReviewFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewFindUniqueOrThrowArgs`](../type-aliases/ComplianceReviewFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a ComplianceReview

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one ComplianceReview
const complianceReview = await prisma.complianceReview.findUniqueOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`, `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`): `object` *extends* `InputErrors` ? [`GetComplianceReviewGroupByPayload`](../type-aliases/GetComplianceReviewGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16331

Group by ComplianceReview.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewGroupByArgs`](../type-aliases/ComplianceReviewGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` *extends* `0` \| `1`

##### OrderByArg

`OrderByArg` *extends* \{ `orderBy`: [`ComplianceReviewOrderByWithAggregationInput`](../type-aliases/ComplianceReviewOrderByWithAggregationInput.md) \| [`ComplianceReviewOrderByWithAggregationInput`](../type-aliases/ComplianceReviewOrderByWithAggregationInput.md)[] \| `undefined`; \} \| \{ `orderBy?`: [`ComplianceReviewOrderByWithAggregationInput`](../type-aliases/ComplianceReviewOrderByWithAggregationInput.md) \| [`ComplianceReviewOrderByWithAggregationInput`](../type-aliases/ComplianceReviewOrderByWithAggregationInput.md)[]; \}

##### OrderFields

`OrderFields` *extends* `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"` \| `"status"` \| `"metadata"` \| `"entityId"` \| `"entityType"` \| `"reviewerId"` \| `"piiType"` \| `"originalValue"` \| `"correctedValue"` \| `"confidenceScore"` \| `"isProcessed"`

##### ByFields

`ByFields` *extends* [`ComplianceReviewScalarFieldEnum`](../type-aliases/ComplianceReviewScalarFieldEnum.md)

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

\{ \[key in string \| number \| symbol\]: key extends keyof ComplianceReviewGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` *extends* `InputErrors` ? [`GetComplianceReviewGroupByPayload`](../type-aliases/GetComplianceReviewGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

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

> **update**\<`T`\>(`args`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16209

Update one ComplianceReview.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewUpdateArgs`](../type-aliases/ComplianceReviewUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewUpdateArgs`](../type-aliases/ComplianceReviewUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one ComplianceReview.

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one ComplianceReview
const complianceReview = await prisma.complianceReview.update({
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

Defined in: node\_modules/.prisma/client/index.d.ts:16242

Update zero or more ComplianceReviews.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewUpdateManyArgs`](../type-aliases/ComplianceReviewUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewUpdateManyArgs`](../type-aliases/ComplianceReviewUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many ComplianceReviews
const complianceReview = await prisma.complianceReview.updateMany({
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

> **upsert**\<`T`\>(`args`): [`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:16261

Create or update one ComplianceReview.

#### Type Parameters

##### T

`T` *extends* [`ComplianceReviewUpsertArgs`](../type-aliases/ComplianceReviewUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`ComplianceReviewUpsertArgs`](../type-aliases/ComplianceReviewUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a ComplianceReview.

#### Returns

[`Prisma__ComplianceReviewClient`](Prisma__ComplianceReviewClient.md)\<`GetFindResult`\<[`$ComplianceReviewPayload`](../type-aliases/$ComplianceReviewPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a ComplianceReview
const complianceReview = await prisma.complianceReview.upsert({
  create: {
    // ... data to create a ComplianceReview
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the ComplianceReview we want to update
  }
})
```

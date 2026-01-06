[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / AIModelConfigDelegate

# Interface: AIModelConfigDelegate\<ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:15021

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`AIModelConfigFieldRefs`](AIModelConfigFieldRefs.md)

Defined in: node\_modules/.prisma/client/index.d.ts:15363

Fields of the AIModelConfig model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetAIModelConfigAggregateType`](../type-aliases/GetAIModelConfigAggregateType.md)\<`T`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:15282

Allows you to perform aggregations operations on a AIModelConfig.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigAggregateArgs`](../type-aliases/AIModelConfigAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`, [`AIModelConfigAggregateArgs`](../type-aliases/AIModelConfigAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetAIModelConfigAggregateType`](../type-aliases/GetAIModelConfigAggregateType.md)\<`T`\>\>

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

> **count**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof AIModelConfigCountAggregateOutputType ? AIModelConfigCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15248

Count the number of AIModelConfigs.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigCountArgs`](../type-aliases/AIModelConfigCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`AIModelConfigCountArgs`](../type-aliases/AIModelConfigCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter AIModelConfigs to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof AIModelConfigCountAggregateOutputType ? AIModelConfigCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of AIModelConfigs
const count = await prisma.aIModelConfig.count({
  where: {
    // ... the filter for the AIModelConfigs we want to count
  }
})
```

***

### create()

> **create**\<`T`\>(`args`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15111

Create a AIModelConfig.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigCreateArgs`](../type-aliases/AIModelConfigCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigCreateArgs`](../type-aliases/AIModelConfigCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a AIModelConfig.

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one AIModelConfig
const AIModelConfig = await prisma.aIModelConfig.create({
  data: {
    // ... data to create a AIModelConfig
  }
})
```

***

### createMany()

> **createMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:15125

Create many AIModelConfigs.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigCreateManyArgs`](../type-aliases/AIModelConfigCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigCreateManyArgs`](../type-aliases/AIModelConfigCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many AIModelConfigs.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many AIModelConfigs
const aIModelConfig = await prisma.aIModelConfig.createMany({
  data: [
    // ... provide data here
  ]
})
```

***

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:15149

Create many AIModelConfigs and returns the data saved in the database.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigCreateManyAndReturnArgs`](../type-aliases/AIModelConfigCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigCreateManyAndReturnArgs`](../type-aliases/AIModelConfigCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many AIModelConfigs.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Create many AIModelConfigs
const aIModelConfig = await prisma.aIModelConfig.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many AIModelConfigs and only return the `id`
const aIModelConfigWithIdOnly = await prisma.aIModelConfig.createManyAndReturn({ 
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

> **delete**\<`T`\>(`args`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15163

Delete a AIModelConfig.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigDeleteArgs`](../type-aliases/AIModelConfigDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigDeleteArgs`](../type-aliases/AIModelConfigDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one AIModelConfig.

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one AIModelConfig
const AIModelConfig = await prisma.aIModelConfig.delete({
  where: {
    // ... filter to delete one AIModelConfig
  }
})
```

***

### deleteMany()

> **deleteMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:15194

Delete zero or more AIModelConfigs.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigDeleteManyArgs`](../type-aliases/AIModelConfigDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigDeleteManyArgs`](../type-aliases/AIModelConfigDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter AIModelConfigs to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few AIModelConfigs
const { count } = await prisma.aIModelConfig.deleteMany({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirst()

> **findFirst**\<`T`\>(`args?`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15063

Find the first AIModelConfig that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigFindFirstArgs`](../type-aliases/AIModelConfigFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigFindFirstArgs`](../type-aliases/AIModelConfigFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a AIModelConfig

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one AIModelConfig
const aIModelConfig = await prisma.aIModelConfig.findFirst({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15079

Find the first AIModelConfig that matches the filter or
throw `PrismaKnownClientError` with `P2025` code if no matches were found.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigFindFirstOrThrowArgs`](../type-aliases/AIModelConfigFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigFindFirstOrThrowArgs`](../type-aliases/AIModelConfigFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a AIModelConfig

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one AIModelConfig
const aIModelConfig = await prisma.aIModelConfig.findFirstOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### findMany()

> **findMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:15097

Find zero or more AIModelConfigs that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigFindManyArgs`](../type-aliases/AIModelConfigFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigFindManyArgs`](../type-aliases/AIModelConfigFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Get all AIModelConfigs
const aIModelConfigs = await prisma.aIModelConfig.findMany()

// Get first 10 AIModelConfigs
const aIModelConfigs = await prisma.aIModelConfig.findMany({ take: 10 })

// Only select the `id`
const aIModelConfigWithIdOnly = await prisma.aIModelConfig.findMany({ select: { id: true } })
```

***

### findUnique()

> **findUnique**\<`T`\>(`args`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15034

Find zero or one AIModelConfig that matches the filter.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigFindUniqueArgs`](../type-aliases/AIModelConfigFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigFindUniqueArgs`](../type-aliases/AIModelConfigFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a AIModelConfig

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one AIModelConfig
const aIModelConfig = await prisma.aIModelConfig.findUnique({
  where: {
    // ... provide filter here
  }
})
```

***

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15048

Find one AIModelConfig that matches the filter or throw an error with `error.code='P2025'` 
if no matches were found.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigFindUniqueOrThrowArgs`](../type-aliases/AIModelConfigFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigFindUniqueOrThrowArgs`](../type-aliases/AIModelConfigFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a AIModelConfig

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one AIModelConfig
const aIModelConfig = await prisma.aIModelConfig.findUniqueOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`, `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`): `object` *extends* `InputErrors` ? [`GetAIModelConfigGroupByPayload`](../type-aliases/GetAIModelConfigGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15302

Group by AIModelConfig.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigGroupByArgs`](../type-aliases/AIModelConfigGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` *extends* `0` \| `1`

##### OrderByArg

`OrderByArg` *extends* \{ `orderBy`: [`AIModelConfigOrderByWithAggregationInput`](../type-aliases/AIModelConfigOrderByWithAggregationInput.md) \| [`AIModelConfigOrderByWithAggregationInput`](../type-aliases/AIModelConfigOrderByWithAggregationInput.md)[] \| `undefined`; \} \| \{ `orderBy?`: [`AIModelConfigOrderByWithAggregationInput`](../type-aliases/AIModelConfigOrderByWithAggregationInput.md) \| [`AIModelConfigOrderByWithAggregationInput`](../type-aliases/AIModelConfigOrderByWithAggregationInput.md)[]; \}

##### OrderFields

`OrderFields` *extends* `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"status"` \| `"version"` \| `"endpoint"` \| `"apiKey"` \| `"isDefault"` \| `"trafficWeight"` \| `"metrics"` \| `"canaryStartedAt"` \| `"lastPromotedAt"`

##### ByFields

`ByFields` *extends* [`AIModelConfigScalarFieldEnum`](../type-aliases/AIModelConfigScalarFieldEnum.md)

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

\{ \[key in string \| number \| symbol\]: key extends keyof AIModelConfigGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` *extends* `InputErrors` ? [`GetAIModelConfigGroupByPayload`](../type-aliases/GetAIModelConfigGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

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

> **update**\<`T`\>(`args`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15180

Update one AIModelConfig.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigUpdateArgs`](../type-aliases/AIModelConfigUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigUpdateArgs`](../type-aliases/AIModelConfigUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one AIModelConfig.

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one AIModelConfig
const aIModelConfig = await prisma.aIModelConfig.update({
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

Defined in: node\_modules/.prisma/client/index.d.ts:15213

Update zero or more AIModelConfigs.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigUpdateManyArgs`](../type-aliases/AIModelConfigUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigUpdateManyArgs`](../type-aliases/AIModelConfigUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many AIModelConfigs
const aIModelConfig = await prisma.aIModelConfig.updateMany({
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

> **upsert**\<`T`\>(`args`): [`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:15232

Create or update one AIModelConfig.

#### Type Parameters

##### T

`T` *extends* [`AIModelConfigUpsertArgs`](../type-aliases/AIModelConfigUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`AIModelConfigUpsertArgs`](../type-aliases/AIModelConfigUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a AIModelConfig.

#### Returns

[`Prisma__AIModelConfigClient`](Prisma__AIModelConfigClient.md)\<`GetFindResult`\<[`$AIModelConfigPayload`](../type-aliases/$AIModelConfigPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a AIModelConfig
const aIModelConfig = await prisma.aIModelConfig.upsert({
  create: {
    // ... data to create a AIModelConfig
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the AIModelConfig we want to update
  }
})
```

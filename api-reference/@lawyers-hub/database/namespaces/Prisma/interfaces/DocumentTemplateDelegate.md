[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / DocumentTemplateDelegate

# Interface: DocumentTemplateDelegate\<ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:12971

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`DocumentTemplateFieldRefs`](DocumentTemplateFieldRefs.md)

Defined in: node\_modules/.prisma/client/index.d.ts:13313

Fields of the DocumentTemplate model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetDocumentTemplateAggregateType`](../type-aliases/GetDocumentTemplateAggregateType.md)\<`T`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:13232

Allows you to perform aggregations operations on a DocumentTemplate.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateAggregateArgs`](../type-aliases/DocumentTemplateAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`, [`DocumentTemplateAggregateArgs`](../type-aliases/DocumentTemplateAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetDocumentTemplateAggregateType`](../type-aliases/GetDocumentTemplateAggregateType.md)\<`T`\>\>

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

> **count**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof DocumentTemplateCountAggregateOutputType ? DocumentTemplateCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13198

Count the number of DocumentTemplates.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateCountArgs`](../type-aliases/DocumentTemplateCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`DocumentTemplateCountArgs`](../type-aliases/DocumentTemplateCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter DocumentTemplates to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof DocumentTemplateCountAggregateOutputType ? DocumentTemplateCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of DocumentTemplates
const count = await prisma.documentTemplate.count({
  where: {
    // ... the filter for the DocumentTemplates we want to count
  }
})
```

***

### create()

> **create**\<`T`\>(`args`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13061

Create a DocumentTemplate.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateCreateArgs`](../type-aliases/DocumentTemplateCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateCreateArgs`](../type-aliases/DocumentTemplateCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a DocumentTemplate.

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one DocumentTemplate
const DocumentTemplate = await prisma.documentTemplate.create({
  data: {
    // ... data to create a DocumentTemplate
  }
})
```

***

### createMany()

> **createMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:13075

Create many DocumentTemplates.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateCreateManyArgs`](../type-aliases/DocumentTemplateCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateCreateManyArgs`](../type-aliases/DocumentTemplateCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many DocumentTemplates.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many DocumentTemplates
const documentTemplate = await prisma.documentTemplate.createMany({
  data: [
    // ... provide data here
  ]
})
```

***

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:13099

Create many DocumentTemplates and returns the data saved in the database.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateCreateManyAndReturnArgs`](../type-aliases/DocumentTemplateCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateCreateManyAndReturnArgs`](../type-aliases/DocumentTemplateCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many DocumentTemplates.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Create many DocumentTemplates
const documentTemplate = await prisma.documentTemplate.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many DocumentTemplates and only return the `id`
const documentTemplateWithIdOnly = await prisma.documentTemplate.createManyAndReturn({ 
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

> **delete**\<`T`\>(`args`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13113

Delete a DocumentTemplate.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateDeleteArgs`](../type-aliases/DocumentTemplateDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateDeleteArgs`](../type-aliases/DocumentTemplateDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one DocumentTemplate.

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one DocumentTemplate
const DocumentTemplate = await prisma.documentTemplate.delete({
  where: {
    // ... filter to delete one DocumentTemplate
  }
})
```

***

### deleteMany()

> **deleteMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:13144

Delete zero or more DocumentTemplates.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateDeleteManyArgs`](../type-aliases/DocumentTemplateDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateDeleteManyArgs`](../type-aliases/DocumentTemplateDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter DocumentTemplates to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few DocumentTemplates
const { count } = await prisma.documentTemplate.deleteMany({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirst()

> **findFirst**\<`T`\>(`args?`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13013

Find the first DocumentTemplate that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateFindFirstArgs`](../type-aliases/DocumentTemplateFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateFindFirstArgs`](../type-aliases/DocumentTemplateFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a DocumentTemplate

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one DocumentTemplate
const documentTemplate = await prisma.documentTemplate.findFirst({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13029

Find the first DocumentTemplate that matches the filter or
throw `PrismaKnownClientError` with `P2025` code if no matches were found.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateFindFirstOrThrowArgs`](../type-aliases/DocumentTemplateFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateFindFirstOrThrowArgs`](../type-aliases/DocumentTemplateFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a DocumentTemplate

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one DocumentTemplate
const documentTemplate = await prisma.documentTemplate.findFirstOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### findMany()

> **findMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:13047

Find zero or more DocumentTemplates that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateFindManyArgs`](../type-aliases/DocumentTemplateFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateFindManyArgs`](../type-aliases/DocumentTemplateFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Get all DocumentTemplates
const documentTemplates = await prisma.documentTemplate.findMany()

// Get first 10 DocumentTemplates
const documentTemplates = await prisma.documentTemplate.findMany({ take: 10 })

// Only select the `id`
const documentTemplateWithIdOnly = await prisma.documentTemplate.findMany({ select: { id: true } })
```

***

### findUnique()

> **findUnique**\<`T`\>(`args`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12984

Find zero or one DocumentTemplate that matches the filter.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateFindUniqueArgs`](../type-aliases/DocumentTemplateFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateFindUniqueArgs`](../type-aliases/DocumentTemplateFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a DocumentTemplate

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one DocumentTemplate
const documentTemplate = await prisma.documentTemplate.findUnique({
  where: {
    // ... provide filter here
  }
})
```

***

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12998

Find one DocumentTemplate that matches the filter or throw an error with `error.code='P2025'` 
if no matches were found.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateFindUniqueOrThrowArgs`](../type-aliases/DocumentTemplateFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateFindUniqueOrThrowArgs`](../type-aliases/DocumentTemplateFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a DocumentTemplate

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one DocumentTemplate
const documentTemplate = await prisma.documentTemplate.findUniqueOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`, `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`): `object` *extends* `InputErrors` ? [`GetDocumentTemplateGroupByPayload`](../type-aliases/GetDocumentTemplateGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13252

Group by DocumentTemplate.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateGroupByArgs`](../type-aliases/DocumentTemplateGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` *extends* `0` \| `1`

##### OrderByArg

`OrderByArg` *extends* \{ `orderBy`: [`DocumentTemplateOrderByWithAggregationInput`](../type-aliases/DocumentTemplateOrderByWithAggregationInput.md) \| [`DocumentTemplateOrderByWithAggregationInput`](../type-aliases/DocumentTemplateOrderByWithAggregationInput.md)[] \| `undefined`; \} \| \{ `orderBy?`: [`DocumentTemplateOrderByWithAggregationInput`](../type-aliases/DocumentTemplateOrderByWithAggregationInput.md) \| [`DocumentTemplateOrderByWithAggregationInput`](../type-aliases/DocumentTemplateOrderByWithAggregationInput.md)[]; \}

##### OrderFields

`OrderFields` *extends* `"name"` \| `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"` \| `"content"` \| `"category"`

##### ByFields

`ByFields` *extends* [`DocumentTemplateScalarFieldEnum`](../type-aliases/DocumentTemplateScalarFieldEnum.md)

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

\{ \[key in string \| number \| symbol\]: key extends keyof DocumentTemplateGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` *extends* `InputErrors` ? [`GetDocumentTemplateGroupByPayload`](../type-aliases/GetDocumentTemplateGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

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

> **update**\<`T`\>(`args`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13130

Update one DocumentTemplate.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateUpdateArgs`](../type-aliases/DocumentTemplateUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateUpdateArgs`](../type-aliases/DocumentTemplateUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one DocumentTemplate.

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one DocumentTemplate
const documentTemplate = await prisma.documentTemplate.update({
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

Defined in: node\_modules/.prisma/client/index.d.ts:13163

Update zero or more DocumentTemplates.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateUpdateManyArgs`](../type-aliases/DocumentTemplateUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateUpdateManyArgs`](../type-aliases/DocumentTemplateUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many DocumentTemplates
const documentTemplate = await prisma.documentTemplate.updateMany({
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

> **upsert**\<`T`\>(`args`): [`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:13182

Create or update one DocumentTemplate.

#### Type Parameters

##### T

`T` *extends* [`DocumentTemplateUpsertArgs`](../type-aliases/DocumentTemplateUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`DocumentTemplateUpsertArgs`](../type-aliases/DocumentTemplateUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a DocumentTemplate.

#### Returns

[`Prisma__DocumentTemplateClient`](Prisma__DocumentTemplateClient.md)\<`GetFindResult`\<[`$DocumentTemplatePayload`](../type-aliases/$DocumentTemplatePayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a DocumentTemplate
const documentTemplate = await prisma.documentTemplate.upsert({
  create: {
    // ... data to create a DocumentTemplate
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the DocumentTemplate we want to update
  }
})
```

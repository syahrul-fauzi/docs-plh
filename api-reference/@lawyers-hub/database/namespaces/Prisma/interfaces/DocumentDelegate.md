[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
DocumentDelegate

# Interface: DocumentDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:6991

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`DocumentFieldRefs`](DocumentFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:7333

Fields of the Document model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetDocumentAggregateType`](../type-aliases/GetDocumentAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:7252

Allows you to perform aggregations operations on a Document. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentAggregateArgs`](../type-aliases/DocumentAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`DocumentAggregateArgs`](../type-aliases/DocumentAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetDocumentAggregateType`](../type-aliases/GetDocumentAggregateType.md)\<`T`\>\>

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
> DocumentCountAggregateOutputType ? DocumentCountAggregateOutputType\[P\<P\>\]
> : never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:7218

Count the number of Documents. Note, that providing `undefined` is treated as
the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentCountArgs`](../type-aliases/DocumentCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`DocumentCountArgs`](../type-aliases/DocumentCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Documents to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
DocumentCountAggregateOutputType ? DocumentCountAggregateOutputType\[P\<P\>\] :
never \} : `number`\>

#### Example

```ts
// Count the number of Documents
const count = await prisma.document.count({
  where: {
    // ... the filter for the Documents we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7081

Create a Document.

#### Type Parameters

##### T

`T` _extends_
[`DocumentCreateArgs`](../type-aliases/DocumentCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentCreateArgs`](../type-aliases/DocumentCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Document.

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Document
const Document = await prisma.document.create({
  data: {
    // ... data to create a Document
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:7095

Create many Documents.

#### Type Parameters

##### T

`T` _extends_
[`DocumentCreateManyArgs`](../type-aliases/DocumentCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentCreateManyArgs`](../type-aliases/DocumentCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Documents.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Documents
const document = await prisma.document.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:7119

Create many Documents and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`DocumentCreateManyAndReturnArgs`](../type-aliases/DocumentCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentCreateManyAndReturnArgs`](../type-aliases/DocumentCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Documents.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Documents
const document = await prisma.document.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Documents and only return the `id`
const documentWithIdOnly = await prisma.document.createManyAndReturn({
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
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7133

Delete a Document.

#### Type Parameters

##### T

`T` _extends_
[`DocumentDeleteArgs`](../type-aliases/DocumentDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentDeleteArgs`](../type-aliases/DocumentDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Document.

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Document
const Document = await prisma.document.delete({
  where: {
    // ... filter to delete one Document
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:7164

Delete zero or more Documents.

#### Type Parameters

##### T

`T` _extends_
[`DocumentDeleteManyArgs`](../type-aliases/DocumentDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentDeleteManyArgs`](../type-aliases/DocumentDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Documents to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Documents
const { count } = await prisma.document.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7033

Find the first Document that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentFindFirstArgs`](../type-aliases/DocumentFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentFindFirstArgs`](../type-aliases/DocumentFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Document

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Document
const document = await prisma.document.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7049

Find the first Document that matches the filter or throw
`PrismaKnownClientError` with `P2025` code if no matches were found. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentFindFirstOrThrowArgs`](../type-aliases/DocumentFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentFindFirstOrThrowArgs`](../type-aliases/DocumentFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Document

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Document
const document = await prisma.document.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:7067

Find zero or more Documents that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentFindManyArgs`](../type-aliases/DocumentFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentFindManyArgs`](../type-aliases/DocumentFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Documents
const documents = await prisma.document.findMany();

// Get first 10 Documents
const documents = await prisma.document.findMany({ take: 10 });

// Only select the `id`
const documentWithIdOnly = await prisma.document.findMany({
  select: { id: true },
});
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7004

Find zero or one Document that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`DocumentFindUniqueArgs`](../type-aliases/DocumentFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentFindUniqueArgs`](../type-aliases/DocumentFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Document

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Document
const document = await prisma.document.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7018

Find one Document that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`DocumentFindUniqueOrThrowArgs`](../type-aliases/DocumentFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentFindUniqueOrThrowArgs`](../type-aliases/DocumentFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Document

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Document
const document = await prisma.document.findUniqueOrThrow({
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
> [`GetDocumentGroupByPayload`](../type-aliases/GetDocumentGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:7272

Group by Document. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentGroupByArgs`](../type-aliases/DocumentGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`DocumentOrderByWithAggregationInput`](../type-aliases/DocumentOrderByWithAggregationInput.md)
\|
[`DocumentOrderByWithAggregationInput`](../type-aliases/DocumentOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`DocumentOrderByWithAggregationInput`](../type-aliases/DocumentOrderByWithAggregationInput.md)
\|
[`DocumentOrderByWithAggregationInput`](../type-aliases/DocumentOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"`
\| `"status"` \| `"title"` \| `"content"` \| `"caseId"`

##### ByFields

`ByFields` _extends_
[`DocumentScalarFieldEnum`](../type-aliases/DocumentScalarFieldEnum.md)

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
DocumentGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetDocumentGroupByPayload`](../type-aliases/GetDocumentGroupByPayload.md)\<`T`\>
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
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7150

Update one Document.

#### Type Parameters

##### T

`T` _extends_
[`DocumentUpdateArgs`](../type-aliases/DocumentUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentUpdateArgs`](../type-aliases/DocumentUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Document.

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Document
const document = await prisma.document.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:7183

Update zero or more Documents. Note, that providing `undefined` is treated as
the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`DocumentUpdateManyArgs`](../type-aliases/DocumentUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentUpdateManyArgs`](../type-aliases/DocumentUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Documents
const document = await prisma.document.updateMany({
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
> [`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:7202

Create or update one Document.

#### Type Parameters

##### T

`T` _extends_
[`DocumentUpsertArgs`](../type-aliases/DocumentUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`DocumentUpsertArgs`](../type-aliases/DocumentUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Document.

#### Returns

[`Prisma__DocumentClient`](Prisma__DocumentClient.md)\<`GetFindResult`\<[`$DocumentPayload`](../type-aliases/$DocumentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Document
const document = await prisma.document.upsert({
  create: {
    // ... data to create a Document
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Document we want to update
  },
});
```

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CommentDelegate

# Interface: CommentDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:9048

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`CommentFieldRefs`](CommentFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:9390

Fields of the Comment model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetCommentAggregateType`](../type-aliases/GetCommentAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:9309

Allows you to perform aggregations operations on a Comment. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentAggregateArgs`](../type-aliases/CommentAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`CommentAggregateArgs`](../type-aliases/CommentAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetCommentAggregateType`](../type-aliases/GetCommentAggregateType.md)\<`T`\>\>

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
> CommentCountAggregateOutputType ? CommentCountAggregateOutputType\[P\<P\>\] :
> never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:9275

Count the number of Comments. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentCountArgs`](../type-aliases/CommentCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`CommentCountArgs`](../type-aliases/CommentCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Comments to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
CommentCountAggregateOutputType ? CommentCountAggregateOutputType\[P\<P\>\] :
never \} : `number`\>

#### Example

```ts
// Count the number of Comments
const count = await prisma.comment.count({
  where: {
    // ... the filter for the Comments we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9138

Create a Comment.

#### Type Parameters

##### T

`T` _extends_
[`CommentCreateArgs`](../type-aliases/CommentCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentCreateArgs`](../type-aliases/CommentCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Comment.

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Comment
const Comment = await prisma.comment.create({
  data: {
    // ... data to create a Comment
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:9152

Create many Comments.

#### Type Parameters

##### T

`T` _extends_
[`CommentCreateManyArgs`](../type-aliases/CommentCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentCreateManyArgs`](../type-aliases/CommentCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Comments.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Comments
const comment = await prisma.comment.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:9176

Create many Comments and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`CommentCreateManyAndReturnArgs`](../type-aliases/CommentCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentCreateManyAndReturnArgs`](../type-aliases/CommentCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Comments.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Comments
const comment = await prisma.comment.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Comments and only return the `id`
const commentWithIdOnly = await prisma.comment.createManyAndReturn({
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
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9190

Delete a Comment.

#### Type Parameters

##### T

`T` _extends_
[`CommentDeleteArgs`](../type-aliases/CommentDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentDeleteArgs`](../type-aliases/CommentDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Comment.

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Comment
const Comment = await prisma.comment.delete({
  where: {
    // ... filter to delete one Comment
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:9221

Delete zero or more Comments.

#### Type Parameters

##### T

`T` _extends_
[`CommentDeleteManyArgs`](../type-aliases/CommentDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentDeleteManyArgs`](../type-aliases/CommentDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Comments to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Comments
const { count } = await prisma.comment.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9090

Find the first Comment that matches the filter. Note, that providing `undefined`
is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentFindFirstArgs`](../type-aliases/CommentFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentFindFirstArgs`](../type-aliases/CommentFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Comment

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Comment
const comment = await prisma.comment.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9106

Find the first Comment that matches the filter or throw `PrismaKnownClientError`
with `P2025` code if no matches were found. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentFindFirstOrThrowArgs`](../type-aliases/CommentFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentFindFirstOrThrowArgs`](../type-aliases/CommentFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Comment

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Comment
const comment = await prisma.comment.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:9124

Find zero or more Comments that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentFindManyArgs`](../type-aliases/CommentFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentFindManyArgs`](../type-aliases/CommentFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Comments
const comments = await prisma.comment.findMany();

// Get first 10 Comments
const comments = await prisma.comment.findMany({ take: 10 });

// Only select the `id`
const commentWithIdOnly = await prisma.comment.findMany({
  select: { id: true },
});
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9061

Find zero or one Comment that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`CommentFindUniqueArgs`](../type-aliases/CommentFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentFindUniqueArgs`](../type-aliases/CommentFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Comment

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Comment
const comment = await prisma.comment.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9075

Find one Comment that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`CommentFindUniqueOrThrowArgs`](../type-aliases/CommentFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentFindUniqueOrThrowArgs`](../type-aliases/CommentFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Comment

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Comment
const comment = await prisma.comment.findUniqueOrThrow({
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
> [`GetCommentGroupByPayload`](../type-aliases/GetCommentGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:9329

Group by Comment. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentGroupByArgs`](../type-aliases/CommentGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`CommentOrderByWithAggregationInput`](../type-aliases/CommentOrderByWithAggregationInput.md)
\|
[`CommentOrderByWithAggregationInput`](../type-aliases/CommentOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`CommentOrderByWithAggregationInput`](../type-aliases/CommentOrderByWithAggregationInput.md)
\|
[`CommentOrderByWithAggregationInput`](../type-aliases/CommentOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"`
\| `"content"` \| `"caseId"` \| `"userId"` \| `"draftId"`

##### ByFields

`ByFields` _extends_
[`CommentScalarFieldEnum`](../type-aliases/CommentScalarFieldEnum.md)

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
CommentGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetCommentGroupByPayload`](../type-aliases/GetCommentGroupByPayload.md)\<`T`\>
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
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9207

Update one Comment.

#### Type Parameters

##### T

`T` _extends_
[`CommentUpdateArgs`](../type-aliases/CommentUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentUpdateArgs`](../type-aliases/CommentUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Comment.

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Comment
const comment = await prisma.comment.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:9240

Update zero or more Comments. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`CommentUpdateManyArgs`](../type-aliases/CommentUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentUpdateManyArgs`](../type-aliases/CommentUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Comments
const comment = await prisma.comment.updateMany({
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
> [`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:9259

Create or update one Comment.

#### Type Parameters

##### T

`T` _extends_
[`CommentUpsertArgs`](../type-aliases/CommentUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`CommentUpsertArgs`](../type-aliases/CommentUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Comment.

#### Returns

[`Prisma__CommentClient`](Prisma__CommentClient.md)\<`GetFindResult`\<[`$CommentPayload`](../type-aliases/$CommentPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Comment
const comment = await prisma.comment.upsert({
  create: {
    // ... data to create a Comment
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Comment we want to update
  },
});
```

[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
SubscriptionDelegate

# Interface: SubscriptionDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:3900

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`SubscriptionFieldRefs`](SubscriptionFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:4242

Fields of the Subscription model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetSubscriptionAggregateType`](../type-aliases/GetSubscriptionAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:4161

Allows you to perform aggregations operations on a Subscription. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionAggregateArgs`](../type-aliases/SubscriptionAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`SubscriptionAggregateArgs`](../type-aliases/SubscriptionAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetSubscriptionAggregateType`](../type-aliases/GetSubscriptionAggregateType.md)\<`T`\>\>

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
> SubscriptionCountAggregateOutputType ?
> SubscriptionCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:4127

Count the number of Subscriptions. Note, that providing `undefined` is treated
as the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionCountArgs`](../type-aliases/SubscriptionCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`SubscriptionCountArgs`](../type-aliases/SubscriptionCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Subscriptions to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
SubscriptionCountAggregateOutputType ?
SubscriptionCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of Subscriptions
const count = await prisma.subscription.count({
  where: {
    // ... the filter for the Subscriptions we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:3990

Create a Subscription.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionCreateArgs`](../type-aliases/SubscriptionCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionCreateArgs`](../type-aliases/SubscriptionCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Subscription.

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Subscription
const Subscription = await prisma.subscription.create({
  data: {
    // ... data to create a Subscription
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:4004

Create many Subscriptions.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionCreateManyArgs`](../type-aliases/SubscriptionCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionCreateManyArgs`](../type-aliases/SubscriptionCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Subscriptions.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Subscriptions
const subscription = await prisma.subscription.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:4028

Create many Subscriptions and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionCreateManyAndReturnArgs`](../type-aliases/SubscriptionCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionCreateManyAndReturnArgs`](../type-aliases/SubscriptionCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Subscriptions.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Subscriptions
const subscription = await prisma.subscription.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Subscriptions and only return the `id`
const subscriptionWithIdOnly = await prisma.subscription.createManyAndReturn({
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
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4042

Delete a Subscription.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionDeleteArgs`](../type-aliases/SubscriptionDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionDeleteArgs`](../type-aliases/SubscriptionDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Subscription.

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Subscription
const Subscription = await prisma.subscription.delete({
  where: {
    // ... filter to delete one Subscription
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:4073

Delete zero or more Subscriptions.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionDeleteManyArgs`](../type-aliases/SubscriptionDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionDeleteManyArgs`](../type-aliases/SubscriptionDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Subscriptions to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Subscriptions
const { count } = await prisma.subscription.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:3942

Find the first Subscription that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionFindFirstArgs`](../type-aliases/SubscriptionFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionFindFirstArgs`](../type-aliases/SubscriptionFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Subscription

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Subscription
const subscription = await prisma.subscription.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:3958

Find the first Subscription that matches the filter or throw
`PrismaKnownClientError` with `P2025` code if no matches were found. Note, that
providing `undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionFindFirstOrThrowArgs`](../type-aliases/SubscriptionFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionFindFirstOrThrowArgs`](../type-aliases/SubscriptionFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Subscription

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Subscription
const subscription = await prisma.subscription.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:3976

Find zero or more Subscriptions that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionFindManyArgs`](../type-aliases/SubscriptionFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionFindManyArgs`](../type-aliases/SubscriptionFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Subscriptions
const subscriptions = await prisma.subscription.findMany();

// Get first 10 Subscriptions
const subscriptions = await prisma.subscription.findMany({ take: 10 });

// Only select the `id`
const subscriptionWithIdOnly = await prisma.subscription.findMany({
  select: { id: true },
});
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:3913

Find zero or one Subscription that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionFindUniqueArgs`](../type-aliases/SubscriptionFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionFindUniqueArgs`](../type-aliases/SubscriptionFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Subscription

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Subscription
const subscription = await prisma.subscription.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:3927

Find one Subscription that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionFindUniqueOrThrowArgs`](../type-aliases/SubscriptionFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionFindUniqueOrThrowArgs`](../type-aliases/SubscriptionFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Subscription

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Subscription
const subscription = await prisma.subscription.findUniqueOrThrow({
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
> [`GetSubscriptionGroupByPayload`](../type-aliases/GetSubscriptionGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:4181

Group by Subscription. Note, that providing `undefined` is treated as the value
not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionGroupByArgs`](../type-aliases/SubscriptionGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`SubscriptionOrderByWithAggregationInput`](../type-aliases/SubscriptionOrderByWithAggregationInput.md)
\|
[`SubscriptionOrderByWithAggregationInput`](../type-aliases/SubscriptionOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`SubscriptionOrderByWithAggregationInput`](../type-aliases/SubscriptionOrderByWithAggregationInput.md)
\|
[`SubscriptionOrderByWithAggregationInput`](../type-aliases/SubscriptionOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"`
\| `"stripeCustomerId"` \| `"stripePriceId"` \| `"status"` \| `"plan"` \|
`"quantity"` \| `"currentPeriodEnd"`

##### ByFields

`ByFields` _extends_
[`SubscriptionScalarFieldEnum`](../type-aliases/SubscriptionScalarFieldEnum.md)

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
SubscriptionGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} &
`OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetSubscriptionGroupByPayload`](../type-aliases/GetSubscriptionGroupByPayload.md)\<`T`\>
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
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4059

Update one Subscription.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionUpdateArgs`](../type-aliases/SubscriptionUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionUpdateArgs`](../type-aliases/SubscriptionUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Subscription.

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Subscription
const subscription = await prisma.subscription.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:4092

Update zero or more Subscriptions. Note, that providing `undefined` is treated
as the value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionUpdateManyArgs`](../type-aliases/SubscriptionUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionUpdateManyArgs`](../type-aliases/SubscriptionUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Subscriptions
const subscription = await prisma.subscription.updateMany({
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
> [`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4111

Create or update one Subscription.

#### Type Parameters

##### T

`T` _extends_
[`SubscriptionUpsertArgs`](../type-aliases/SubscriptionUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`SubscriptionUpsertArgs`](../type-aliases/SubscriptionUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Subscription.

#### Returns

[`Prisma__SubscriptionClient`](Prisma__SubscriptionClient.md)\<`GetFindResult`\<[`$SubscriptionPayload`](../type-aliases/$SubscriptionPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Subscription
const subscription = await prisma.subscription.upsert({
  create: {
    // ... data to create a Subscription
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Subscription we want to update
  },
});
```

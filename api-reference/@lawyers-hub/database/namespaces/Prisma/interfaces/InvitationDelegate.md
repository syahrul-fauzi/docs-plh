[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / InvitationDelegate

# Interface: InvitationDelegate\<ExtArgs\>

Defined in: node\_modules/.prisma/client/index.d.ts:12007

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`InvitationFieldRefs`](InvitationFieldRefs.md)

Defined in: node\_modules/.prisma/client/index.d.ts:12349

Fields of the Invitation model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetInvitationAggregateType`](../type-aliases/GetInvitationAggregateType.md)\<`T`\>\>

Defined in: node\_modules/.prisma/client/index.d.ts:12268

Allows you to perform aggregations operations on a Invitation.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationAggregateArgs`](../type-aliases/InvitationAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`, [`InvitationAggregateArgs`](../type-aliases/InvitationAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetInvitationAggregateType`](../type-aliases/GetInvitationAggregateType.md)\<`T`\>\>

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

> **count**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof InvitationCountAggregateOutputType ? InvitationCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12234

Count the number of Invitations.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationCountArgs`](../type-aliases/InvitationCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`, [`InvitationCountArgs`](../type-aliases/InvitationCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Invitations to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` *extends* `Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] *extends* `true` ? `number` : \{ \[P in string \| number \| symbol\]: P extends keyof InvitationCountAggregateOutputType ? InvitationCountAggregateOutputType\[P\<P\>\] : never \} : `number`\>

#### Example

```ts
// Count the number of Invitations
const count = await prisma.invitation.count({
  where: {
    // ... the filter for the Invitations we want to count
  }
})
```

***

### create()

> **create**\<`T`\>(`args`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12097

Create a Invitation.

#### Type Parameters

##### T

`T` *extends* [`InvitationCreateArgs`](../type-aliases/InvitationCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationCreateArgs`](../type-aliases/InvitationCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Invitation.

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Invitation
const Invitation = await prisma.invitation.create({
  data: {
    // ... data to create a Invitation
  }
})
```

***

### createMany()

> **createMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:12111

Create many Invitations.

#### Type Parameters

##### T

`T` *extends* [`InvitationCreateManyArgs`](../type-aliases/InvitationCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationCreateManyArgs`](../type-aliases/InvitationCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Invitations.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Invitations
const invitation = await prisma.invitation.createMany({
  data: [
    // ... provide data here
  ]
})
```

***

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:12135

Create many Invitations and returns the data saved in the database.

#### Type Parameters

##### T

`T` *extends* [`InvitationCreateManyAndReturnArgs`](../type-aliases/InvitationCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationCreateManyAndReturnArgs`](../type-aliases/InvitationCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Invitations.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Create many Invitations
const invitation = await prisma.invitation.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Invitations and only return the `id`
const invitationWithIdOnly = await prisma.invitation.createManyAndReturn({ 
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

> **delete**\<`T`\>(`args`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12149

Delete a Invitation.

#### Type Parameters

##### T

`T` *extends* [`InvitationDeleteArgs`](../type-aliases/InvitationDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationDeleteArgs`](../type-aliases/InvitationDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Invitation.

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Invitation
const Invitation = await prisma.invitation.delete({
  where: {
    // ... filter to delete one Invitation
  }
})
```

***

### deleteMany()

> **deleteMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:12180

Delete zero or more Invitations.

#### Type Parameters

##### T

`T` *extends* [`InvitationDeleteManyArgs`](../type-aliases/InvitationDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationDeleteManyArgs`](../type-aliases/InvitationDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Invitations to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Invitations
const { count } = await prisma.invitation.deleteMany({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirst()

> **findFirst**\<`T`\>(`args?`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12049

Find the first Invitation that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationFindFirstArgs`](../type-aliases/InvitationFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationFindFirstArgs`](../type-aliases/InvitationFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Invitation

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Invitation
const invitation = await prisma.invitation.findFirst({
  where: {
    // ... provide filter here
  }
})
```

***

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12065

Find the first Invitation that matches the filter or
throw `PrismaKnownClientError` with `P2025` code if no matches were found.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationFindFirstOrThrowArgs`](../type-aliases/InvitationFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationFindFirstOrThrowArgs`](../type-aliases/InvitationFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Invitation

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Invitation
const invitation = await prisma.invitation.findFirstOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### findMany()

> **findMany**\<`T`\>(`args?`): [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:12083

Find zero or more Invitations that matches the filter.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationFindManyArgs`](../type-aliases/InvitationFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationFindManyArgs`](../type-aliases/InvitationFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>[]\>

#### Example

```ts
// Get all Invitations
const invitations = await prisma.invitation.findMany()

// Get first 10 Invitations
const invitations = await prisma.invitation.findMany({ take: 10 })

// Only select the `id`
const invitationWithIdOnly = await prisma.invitation.findMany({ select: { id: true } })
```

***

### findUnique()

> **findUnique**\<`T`\>(`args`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12020

Find zero or one Invitation that matches the filter.

#### Type Parameters

##### T

`T` *extends* [`InvitationFindUniqueArgs`](../type-aliases/InvitationFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationFindUniqueArgs`](../type-aliases/InvitationFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Invitation

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Invitation
const invitation = await prisma.invitation.findUnique({
  where: {
    // ... provide filter here
  }
})
```

***

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12034

Find one Invitation that matches the filter or throw an error with `error.code='P2025'` 
if no matches were found.

#### Type Parameters

##### T

`T` *extends* [`InvitationFindUniqueOrThrowArgs`](../type-aliases/InvitationFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationFindUniqueOrThrowArgs`](../type-aliases/InvitationFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Invitation

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Invitation
const invitation = await prisma.invitation.findUniqueOrThrow({
  where: {
    // ... provide filter here
  }
})
```

***

### groupBy()

> **groupBy**\<`T`, `HasSelectOrTake`, `OrderByArg`, `OrderFields`, `ByFields`, `ByValid`, `HavingFields`, `HavingValid`, `ByEmpty`, `InputErrors`\>(`args`): `object` *extends* `InputErrors` ? [`GetInvitationGroupByPayload`](../type-aliases/GetInvitationGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12288

Group by Invitation.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationGroupByArgs`](../type-aliases/InvitationGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` *extends* `0` \| `1`

##### OrderByArg

`OrderByArg` *extends* \{ `orderBy`: [`InvitationOrderByWithAggregationInput`](../type-aliases/InvitationOrderByWithAggregationInput.md) \| [`InvitationOrderByWithAggregationInput`](../type-aliases/InvitationOrderByWithAggregationInput.md)[] \| `undefined`; \} \| \{ `orderBy?`: [`InvitationOrderByWithAggregationInput`](../type-aliases/InvitationOrderByWithAggregationInput.md) \| [`InvitationOrderByWithAggregationInput`](../type-aliases/InvitationOrderByWithAggregationInput.md)[]; \}

##### OrderFields

`OrderFields` *extends* `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"` \| `"status"` \| `"email"` \| `"role"` \| `"token"` \| `"expiresAt"`

##### ByFields

`ByFields` *extends* [`InvitationScalarFieldEnum`](../type-aliases/InvitationScalarFieldEnum.md)

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

\{ \[key in string \| number \| symbol\]: key extends keyof InvitationGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` & `InputErrors`

Group by arguments.

#### Returns

`object` *extends* `InputErrors` ? [`GetInvitationGroupByPayload`](../type-aliases/GetInvitationGroupByPayload.md)\<`T`\> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

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

> **update**\<`T`\>(`args`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12166

Update one Invitation.

#### Type Parameters

##### T

`T` *extends* [`InvitationUpdateArgs`](../type-aliases/InvitationUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationUpdateArgs`](../type-aliases/InvitationUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Invitation.

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Invitation
const invitation = await prisma.invitation.update({
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

Defined in: node\_modules/.prisma/client/index.d.ts:12199

Update zero or more Invitations.
Note, that providing `undefined` is treated as the value not being there.
Read more here: https://pris.ly/d/null-undefined

#### Type Parameters

##### T

`T` *extends* [`InvitationUpdateManyArgs`](../type-aliases/InvitationUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationUpdateManyArgs`](../type-aliases/InvitationUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Invitations
const invitation = await prisma.invitation.updateMany({
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

> **upsert**\<`T`\>(`args`): [`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node\_modules/.prisma/client/index.d.ts:12218

Create or update one Invitation.

#### Type Parameters

##### T

`T` *extends* [`InvitationUpsertArgs`](../type-aliases/InvitationUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`, [`InvitationUpsertArgs`](../type-aliases/InvitationUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Invitation.

#### Returns

[`Prisma__InvitationClient`](Prisma__InvitationClient.md)\<`GetFindResult`\<[`$InvitationPayload`](../type-aliases/$InvitationPayload.md)\<`ExtArgs`\>, `T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Invitation
const invitation = await prisma.invitation.upsert({
  create: {
    // ... data to create a Invitation
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Invitation we want to update
  }
})
```

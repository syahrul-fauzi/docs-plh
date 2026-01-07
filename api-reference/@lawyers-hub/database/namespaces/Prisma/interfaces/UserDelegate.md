[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserDelegate

# Interface: UserDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:4877

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`UserFieldRefs`](UserFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:5219

Fields of the User model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetUserAggregateType`](../type-aliases/GetUserAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:5138

Allows you to perform aggregations operations on a User. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserAggregateArgs`](../type-aliases/UserAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`UserAggregateArgs`](../type-aliases/UserAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetUserAggregateType`](../type-aliases/GetUserAggregateType.md)\<`T`\>\>

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
> UserCountAggregateOutputType ? UserCountAggregateOutputType\[P\<P\>\] : never
> \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:5104

Count the number of Users. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserCountArgs`](../type-aliases/UserCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`UserCountArgs`](../type-aliases/UserCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Users to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
UserCountAggregateOutputType ? UserCountAggregateOutputType\[P\<P\>\] : never \}
: `number`\>

#### Example

```ts
// Count the number of Users
const count = await prisma.user.count({
  where: {
    // ... the filter for the Users we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4967

Create a User.

#### Type Parameters

##### T

`T` _extends_
[`UserCreateArgs`](../type-aliases/UserCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserCreateArgs`](../type-aliases/UserCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a User.

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one User
const User = await prisma.user.create({
  data: {
    // ... data to create a User
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:4981

Create many Users.

#### Type Parameters

##### T

`T` _extends_
[`UserCreateManyArgs`](../type-aliases/UserCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserCreateManyArgs`](../type-aliases/UserCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Users.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Users
const user = await prisma.user.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:5005

Create many Users and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`UserCreateManyAndReturnArgs`](../type-aliases/UserCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserCreateManyAndReturnArgs`](../type-aliases/UserCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Users.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Users
const user = await prisma.user.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Users and only return the `id`
const userWithIdOnly = await prisma.user.createManyAndReturn({
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
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:5019

Delete a User.

#### Type Parameters

##### T

`T` _extends_
[`UserDeleteArgs`](../type-aliases/UserDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserDeleteArgs`](../type-aliases/UserDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one User.

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one User
const User = await prisma.user.delete({
  where: {
    // ... filter to delete one User
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:5050

Delete zero or more Users.

#### Type Parameters

##### T

`T` _extends_
[`UserDeleteManyArgs`](../type-aliases/UserDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserDeleteManyArgs`](../type-aliases/UserDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Users to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Users
const { count } = await prisma.user.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4919

Find the first User that matches the filter. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserFindFirstArgs`](../type-aliases/UserFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserFindFirstArgs`](../type-aliases/UserFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a User

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one User
const user = await prisma.user.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4935

Find the first User that matches the filter or throw `PrismaKnownClientError`
with `P2025` code if no matches were found. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserFindFirstOrThrowArgs`](../type-aliases/UserFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserFindFirstOrThrowArgs`](../type-aliases/UserFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a User

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one User
const user = await prisma.user.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:4953

Find zero or more Users that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserFindManyArgs`](../type-aliases/UserFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserFindManyArgs`](../type-aliases/UserFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Users
const users = await prisma.user.findMany();

// Get first 10 Users
const users = await prisma.user.findMany({ take: 10 });

// Only select the `id`
const userWithIdOnly = await prisma.user.findMany({ select: { id: true } });
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4890

Find zero or one User that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`UserFindUniqueArgs`](../type-aliases/UserFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserFindUniqueArgs`](../type-aliases/UserFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a User

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one User
const user = await prisma.user.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:4904

Find one User that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`UserFindUniqueOrThrowArgs`](../type-aliases/UserFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserFindUniqueOrThrowArgs`](../type-aliases/UserFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a User

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one User
const user = await prisma.user.findUniqueOrThrow({
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
> [`GetUserGroupByPayload`](../type-aliases/GetUserGroupByPayload.md)\<`T`\> :
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:5158

Group by User. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserGroupByArgs`](../type-aliases/UserGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`UserOrderByWithAggregationInput`](../type-aliases/UserOrderByWithAggregationInput.md)
\|
[`UserOrderByWithAggregationInput`](../type-aliases/UserOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`UserOrderByWithAggregationInput`](../type-aliases/UserOrderByWithAggregationInput.md)
\|
[`UserOrderByWithAggregationInput`](../type-aliases/UserOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"id"` \| `"createdAt"` \| `"updatedAt"` \| `"tenantId"`
\| `"email"` \| `"fullName"` \| `"role"`

##### ByFields

`ByFields` _extends_
[`UserScalarFieldEnum`](../type-aliases/UserScalarFieldEnum.md)

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
UserGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetUserGroupByPayload`](../type-aliases/GetUserGroupByPayload.md)\<`T`\> :
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
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:5036

Update one User.

#### Type Parameters

##### T

`T` _extends_
[`UserUpdateArgs`](../type-aliases/UserUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserUpdateArgs`](../type-aliases/UserUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one User.

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one User
const user = await prisma.user.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:5069

Update zero or more Users. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`UserUpdateManyArgs`](../type-aliases/UserUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserUpdateManyArgs`](../type-aliases/UserUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Users
const user = await prisma.user.updateMany({
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
> [`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:5088

Create or update one User.

#### Type Parameters

##### T

`T` _extends_
[`UserUpsertArgs`](../type-aliases/UserUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`UserUpsertArgs`](../type-aliases/UserUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a User.

#### Returns

[`Prisma__UserClient`](Prisma__UserClient.md)\<`GetFindResult`\<[`$UserPayload`](../type-aliases/$UserPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a User
const user = await prisma.user.upsert({
  create: {
    // ... data to create a User
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the User we want to update
  },
});
```

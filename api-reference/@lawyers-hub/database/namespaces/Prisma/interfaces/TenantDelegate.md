[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TenantDelegate

# Interface: TenantDelegate\<ExtArgs\>

Defined in: node_modules/.prisma/client/index.d.ts:2635

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Indexable

\[`K`: `symbol`\]: `object`

## Properties

### fields

> `readonly` **fields**: [`TenantFieldRefs`](TenantFieldRefs.md)

Defined in: node_modules/.prisma/client/index.d.ts:2977

Fields of the Tenant model

## Methods

### aggregate()

> **aggregate**\<`T`\>(`args`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetTenantAggregateType`](../type-aliases/GetTenantAggregateType.md)\<`T`\>\>

Defined in: node_modules/.prisma/client/index.d.ts:2896

Allows you to perform aggregations operations on a Tenant. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantAggregateArgs`](../type-aliases/TenantAggregateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`TenantAggregateArgs`](../type-aliases/TenantAggregateArgs.md)\>

Select which aggregations you would like to apply and on what fields.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`GetTenantAggregateType`](../type-aliases/GetTenantAggregateType.md)\<`T`\>\>

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
> TenantCountAggregateOutputType ? TenantCountAggregateOutputType\[P\<P\>\] :
> never \} : `number`\>

Defined in: node_modules/.prisma/client/index.d.ts:2862

Count the number of Tenants. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantCountArgs`](../type-aliases/TenantCountArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`Subset`](../type-aliases/Subset.md)\<`T`,
[`TenantCountArgs`](../type-aliases/TenantCountArgs.md)\<`DefaultArgs`\>\>

Arguments to filter Tenants to count.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`T` _extends_
`Record_2`\<`"select"`, `any`\> ? `T`\<`T`\>\[`"select"`\] _extends_ `true` ?
`number` : \{ \[P in string \| number \| symbol\]: P extends keyof
TenantCountAggregateOutputType ? TenantCountAggregateOutputType\[P\<P\>\] :
never \} : `number`\>

#### Example

```ts
// Count the number of Tenants
const count = await prisma.tenant.count({
  where: {
    // ... the filter for the Tenants we want to count
  },
});
```

---

### create()

> **create**\<`T`\>(`args`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2725

Create a Tenant.

#### Type Parameters

##### T

`T` _extends_
[`TenantCreateArgs`](../type-aliases/TenantCreateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantCreateArgs`](../type-aliases/TenantCreateArgs.md)\<`ExtArgs`\>\>

Arguments to create a Tenant.

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Create one Tenant
const Tenant = await prisma.tenant.create({
  data: {
    // ... data to create a Tenant
  },
});
```

---

### createMany()

> **createMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:2739

Create many Tenants.

#### Type Parameters

##### T

`T` _extends_
[`TenantCreateManyArgs`](../type-aliases/TenantCreateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantCreateManyArgs`](../type-aliases/TenantCreateManyArgs.md)\<`ExtArgs`\>\>

Arguments to create many Tenants.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Create many Tenants
const tenant = await prisma.tenant.createMany({
  data: [
    // ... provide data here
  ],
});
```

---

### createManyAndReturn()

> **createManyAndReturn**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:2763

Create many Tenants and returns the data saved in the database.

#### Type Parameters

##### T

`T` _extends_
[`TenantCreateManyAndReturnArgs`](../type-aliases/TenantCreateManyAndReturnArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantCreateManyAndReturnArgs`](../type-aliases/TenantCreateManyAndReturnArgs.md)\<`ExtArgs`\>\>

Arguments to create many Tenants.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Create many Tenants
const tenant = await prisma.tenant.createManyAndReturn({
  data: [
    // ... provide data here
  ]
})

// Create many Tenants and only return the `id`
const tenantWithIdOnly = await prisma.tenant.createManyAndReturn({
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
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2777

Delete a Tenant.

#### Type Parameters

##### T

`T` _extends_
[`TenantDeleteArgs`](../type-aliases/TenantDeleteArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantDeleteArgs`](../type-aliases/TenantDeleteArgs.md)\<`ExtArgs`\>\>

Arguments to delete one Tenant.

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Delete one Tenant
const Tenant = await prisma.tenant.delete({
  where: {
    // ... filter to delete one Tenant
  },
});
```

---

### deleteMany()

> **deleteMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:2808

Delete zero or more Tenants.

#### Type Parameters

##### T

`T` _extends_
[`TenantDeleteManyArgs`](../type-aliases/TenantDeleteManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantDeleteManyArgs`](../type-aliases/TenantDeleteManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter Tenants to delete.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Delete a few Tenants
const { count } = await prisma.tenant.deleteMany({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirst()

> **findFirst**\<`T`\>(`args?`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2677

Find the first Tenant that matches the filter. Note, that providing `undefined`
is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantFindFirstArgs`](../type-aliases/TenantFindFirstArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantFindFirstArgs`](../type-aliases/TenantFindFirstArgs.md)\<`ExtArgs`\>\>

Arguments to find a Tenant

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Tenant
const tenant = await prisma.tenant.findFirst({
  where: {
    // ... provide filter here
  },
});
```

---

### findFirstOrThrow()

> **findFirstOrThrow**\<`T`\>(`args?`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2693

Find the first Tenant that matches the filter or throw `PrismaKnownClientError`
with `P2025` code if no matches were found. Note, that providing `undefined` is
treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantFindFirstOrThrowArgs`](../type-aliases/TenantFindFirstOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantFindFirstOrThrowArgs`](../type-aliases/TenantFindFirstOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Tenant

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Tenant
const tenant = await prisma.tenant.findFirstOrThrow({
  where: {
    // ... provide filter here
  },
});
```

---

### findMany()

> **findMany**\<`T`\>(`args?`):
> [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>[]\>

Defined in: node_modules/.prisma/client/index.d.ts:2711

Find zero or more Tenants that matches the filter. Note, that providing
`undefined` is treated as the value not being there. Read more here:
<https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantFindManyArgs`](../type-aliases/TenantFindManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args?

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantFindManyArgs`](../type-aliases/TenantFindManyArgs.md)\<`ExtArgs`\>\>

Arguments to filter and select certain fields only.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>[]\>

#### Example

```ts
// Get all Tenants
const tenants = await prisma.tenant.findMany();

// Get first 10 Tenants
const tenants = await prisma.tenant.findMany({ take: 10 });

// Only select the `id`
const tenantWithIdOnly = await prisma.tenant.findMany({ select: { id: true } });
```

---

### findUnique()

> **findUnique**\<`T`\>(`args`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2648

Find zero or one Tenant that matches the filter.

#### Type Parameters

##### T

`T` _extends_
[`TenantFindUniqueArgs`](../type-aliases/TenantFindUniqueArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantFindUniqueArgs`](../type-aliases/TenantFindUniqueArgs.md)\<`ExtArgs`\>\>

Arguments to find a Tenant

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\> \| `null`, `null`, `ExtArgs`\>

#### Example

```ts
// Get one Tenant
const tenant = await prisma.tenant.findUnique({
  where: {
    // ... provide filter here
  },
});
```

---

### findUniqueOrThrow()

> **findUniqueOrThrow**\<`T`\>(`args`):
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2662

Find one Tenant that matches the filter or throw an error with
`error.code='P2025'` if no matches were found.

#### Type Parameters

##### T

`T` _extends_
[`TenantFindUniqueOrThrowArgs`](../type-aliases/TenantFindUniqueOrThrowArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantFindUniqueOrThrowArgs`](../type-aliases/TenantFindUniqueOrThrowArgs.md)\<`ExtArgs`\>\>

Arguments to find a Tenant

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Get one Tenant
const tenant = await prisma.tenant.findUniqueOrThrow({
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
> [`GetTenantGroupByPayload`](../type-aliases/GetTenantGroupByPayload.md)\<`T`\>
> : [`PrismaPromise`](../type-aliases/PrismaPromise.md)\<`InputErrors`\>

Defined in: node_modules/.prisma/client/index.d.ts:2916

Group by Tenant. Note, that providing `undefined` is treated as the value not
being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantGroupByArgs`](../type-aliases/TenantGroupByArgs.md)\<`DefaultArgs`\>

##### HasSelectOrTake

`HasSelectOrTake` _extends_ `0` \| `1`

##### OrderByArg

`OrderByArg` _extends_ \{ `orderBy`:
[`TenantOrderByWithAggregationInput`](../type-aliases/TenantOrderByWithAggregationInput.md)
\|
[`TenantOrderByWithAggregationInput`](../type-aliases/TenantOrderByWithAggregationInput.md)[]
\| `undefined`; \} \| \{ `orderBy?`:
[`TenantOrderByWithAggregationInput`](../type-aliases/TenantOrderByWithAggregationInput.md)
\|
[`TenantOrderByWithAggregationInput`](../type-aliases/TenantOrderByWithAggregationInput.md)[];
\}

##### OrderFields

`OrderFields` _extends_ `"name"` \| `"id"` \| `"slug"` \| `"isActive"` \|
`"createdAt"` \| `"updatedAt"`

##### ByFields

`ByFields` _extends_
[`TenantScalarFieldEnum`](../type-aliases/TenantScalarFieldEnum.md)

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
TenantGroupByArgs\<DefaultArgs\> ? T\[key\<key\>\] : never \} & `OrderByArg` &
`InputErrors`

Group by arguments.

#### Returns

`object` _extends_ `InputErrors` ?
[`GetTenantGroupByPayload`](../type-aliases/GetTenantGroupByPayload.md)\<`T`\> :
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
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2794

Update one Tenant.

#### Type Parameters

##### T

`T` _extends_
[`TenantUpdateArgs`](../type-aliases/TenantUpdateArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantUpdateArgs`](../type-aliases/TenantUpdateArgs.md)\<`ExtArgs`\>\>

Arguments to update one Tenant.

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update one Tenant
const tenant = await prisma.tenant.update({
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

Defined in: node_modules/.prisma/client/index.d.ts:2827

Update zero or more Tenants. Note, that providing `undefined` is treated as the
value not being there. Read more here: <https://pris.ly/d/null-undefined>

#### Type Parameters

##### T

`T` _extends_
[`TenantUpdateManyArgs`](../type-aliases/TenantUpdateManyArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantUpdateManyArgs`](../type-aliases/TenantUpdateManyArgs.md)\<`ExtArgs`\>\>

Arguments to update one or more rows.

#### Returns

[`PrismaPromise`](../type-aliases/PrismaPromise.md)\<[`BatchPayload`](../type-aliases/BatchPayload.md)\>

#### Example

```ts
// Update many Tenants
const tenant = await prisma.tenant.updateMany({
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
> [`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
> `T`, \{ \}\>, `never`, `ExtArgs`\>

Defined in: node_modules/.prisma/client/index.d.ts:2846

Create or update one Tenant.

#### Type Parameters

##### T

`T` _extends_
[`TenantUpsertArgs`](../type-aliases/TenantUpsertArgs.md)\<`DefaultArgs`\>

#### Parameters

##### args

[`SelectSubset`](../type-aliases/SelectSubset.md)\<`T`,
[`TenantUpsertArgs`](../type-aliases/TenantUpsertArgs.md)\<`ExtArgs`\>\>

Arguments to update or create a Tenant.

#### Returns

[`Prisma__TenantClient`](Prisma__TenantClient.md)\<`GetFindResult`\<[`$TenantPayload`](../type-aliases/$TenantPayload.md)\<`ExtArgs`\>,
`T`, \{ \}\>, `never`, `ExtArgs`\>

#### Example

```ts
// Update or create a Tenant
const tenant = await prisma.tenant.upsert({
  create: {
    // ... data to create a Tenant
  },
  update: {
    // ... in case it already exists, update
  },
  where: {
    // ... the filter for the Tenant we want to update
  },
});
```

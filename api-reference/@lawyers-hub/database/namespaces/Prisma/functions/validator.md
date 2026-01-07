[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / validator

# Function: validator()

## Call Signature

> **validator**\<`V`\>(): \<`S`\>(`select`) => `S`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3370

### Type Parameters

#### V

`V`

### Returns

> \<`S`\>(`select`): `S`

#### Type Parameters

##### S

`S`

#### Parameters

##### select

[`Exact`](../type-aliases/Exact.md)\<`S`, `V`\>

#### Returns

`S`

## Call Signature

> **validator**\<`C`, `M`, `O`\>(`client`, `model`, `operation`):
> \<`S`\>(`select`) => `S`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3372

### Type Parameters

#### C

`C`

#### M

`M` _extends_ `string` \| `number` \| `symbol`

#### O

`O` _extends_ `"$executeRaw"` \| `"$executeRawUnsafe"` \| `"$queryRaw"` \|
`"$queryRawUnsafe"` \| `"findUnique"` \| `"findUniqueOrThrow"` \| `"findMany"`
\| `"findFirst"` \| `"findFirstOrThrow"` \| `"create"` \| `"createMany"` \|
`"createManyAndReturn"` \| `"update"` \| `"updateMany"` \| `"upsert"` \|
`"delete"` \| `"deleteMany"` \| `"aggregate"` \| `"count"` \| `"findRaw"` \|
`"groupBy"` \| `"aggregateRaw"` \| `"$runCommandRaw"`

### Parameters

#### client

`C`

#### model

`M`

#### operation

`O`

### Returns

> \<`S`\>(`select`): `S`

#### Type Parameters

##### S

`S`

#### Parameters

##### select

[`Exact`](../type-aliases/Exact.md)\<`S`,
[`Args`](../type-aliases/Args.md)\<`C`\[`M`\], `O`\>\>

#### Returns

`S`

## Call Signature

> **validator**\<`C`, `M`, `O`, `P`\>(`client`, `model`, `operation`, `prop`):
> \<`S`\>(`select`) => `S`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3374

### Type Parameters

#### C

`C`

#### M

`M` _extends_ `string` \| `number` \| `symbol`

#### O

`O` _extends_ `"$executeRaw"` \| `"$executeRawUnsafe"` \| `"$queryRaw"` \|
`"$queryRawUnsafe"` \| `"findUnique"` \| `"findUniqueOrThrow"` \| `"findMany"`
\| `"findFirst"` \| `"findFirstOrThrow"` \| `"create"` \| `"createMany"` \|
`"createManyAndReturn"` \| `"update"` \| `"updateMany"` \| `"upsert"` \|
`"delete"` \| `"deleteMany"` \| `"aggregate"` \| `"count"` \| `"findRaw"` \|
`"groupBy"` \| `"aggregateRaw"` \| `"$runCommandRaw"`

#### P

`P` _extends_ `string` \| `number` \| `symbol`

### Parameters

#### client

`C`

#### model

`M`

#### operation

`O`

#### prop

`P`

### Returns

> \<`S`\>(`select`): `S`

#### Type Parameters

##### S

`S`

#### Parameters

##### select

[`Exact`](../type-aliases/Exact.md)\<`S`,
[`Args`](../type-aliases/Args.md)\<`C`\[`M`\], `O`\>\[`P`\]\>

#### Returns

`S`

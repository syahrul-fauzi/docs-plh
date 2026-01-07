[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Sql

# Class: Sql

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3153

A SQL instance can be nested within each other to build SQL strings.

## Constructors

### Constructor

> **new Sql**(`rawStrings`, `rawValues`): `Sql`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3156

#### Parameters

##### rawStrings

readonly `string`[]

##### rawValues

readonly `unknown`[]

#### Returns

`Sql`

## Properties

### strings

> `readonly` **strings**: `string`[]

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3155

---

### values

> `readonly` **values**: `unknown`[]

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3154

## Accessors

### sql

#### Get Signature

> **get** **sql**(): `string`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3157

##### Returns

`string`

---

### statement

#### Get Signature

> **get** **statement**(): `string`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3158

##### Returns

`string`

---

### text

#### Get Signature

> **get** **text**(): `string`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3159

##### Returns

`string`

## Methods

### inspect()

> **inspect**(): `object`

Defined in: node_modules/@prisma/client/runtime/library.d.ts:3160

#### Returns

`object`

##### sql

> **sql**: `string`

##### statement

> **statement**: `string`

##### text

> **text**: `string`

##### values

> **values**: `unknown`[]

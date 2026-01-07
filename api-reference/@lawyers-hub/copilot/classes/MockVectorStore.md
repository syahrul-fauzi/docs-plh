[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/copilot](../README.md) / MockVectorStore

# Class: MockVectorStore

Defined in:
[rag/vector-store.ts:37](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L37)

Mock implementation for local development.

## Extends

- [`VectorStore`](VectorStore.md)

## Constructors

### Constructor

> **new MockVectorStore**(): `MockVectorStore`

#### Returns

`MockVectorStore`

#### Inherited from

[`VectorStore`](VectorStore.md).[`constructor`](VectorStore.md#constructor)

## Methods

### delete()

> **delete**(`tenantId`, `documentId?`): `Promise`\<`void`\>

Defined in:
[rag/vector-store.ts:78](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L78)

Deletes all vectors for a specific tenant or document.

#### Parameters

##### tenantId

`string`

##### documentId?

`string`

#### Returns

`Promise`\<`void`\>

#### Overrides

[`VectorStore`](VectorStore.md).[`delete`](VectorStore.md#delete)

---

### query()

> **query**(`tenantId`, `vector`, `topK`, `options?`):
> `Promise`\<[`VectorRecord`](../interfaces/VectorRecord.md)[]\>

Defined in:
[rag/vector-store.ts:46](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L46)

Queries vectors within a specific tenant's namespace.

#### Parameters

##### tenantId

`string`

##### vector

`number`[]

##### topK

`number`

##### options?

###### filter?

`any`

###### minScore?

`number`

###### searchQuery?

`string`

#### Returns

`Promise`\<[`VectorRecord`](../interfaces/VectorRecord.md)[]\>

#### Overrides

[`VectorStore`](VectorStore.md).[`query`](VectorStore.md#query)

---

### upsert()

> **upsert**(`tenantId`, `records`): `Promise`\<`void`\>

Defined in:
[rag/vector-store.ts:40](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L40)

Upserts vectors into a specific tenant's namespace.

#### Parameters

##### tenantId

`string`

##### records

[`VectorRecord`](../interfaces/VectorRecord.md)[]

#### Returns

`Promise`\<`void`\>

#### Overrides

[`VectorStore`](VectorStore.md).[`upsert`](VectorStore.md#upsert)

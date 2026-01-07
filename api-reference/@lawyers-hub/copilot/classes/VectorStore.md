[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/copilot](../README.md) / VectorStore

# Abstract Class: VectorStore

Defined in:
[rag/vector-store.ts:17](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L17)

Interface for Vector Store operations with strict tenant isolation.

## Extended by

- [`MockVectorStore`](MockVectorStore.md)

## Constructors

### Constructor

> **new VectorStore**(): `VectorStore`

#### Returns

`VectorStore`

## Methods

### delete()

> `abstract` **delete**(`tenantId`, `documentId?`): `Promise`\<`void`\>

Defined in:
[rag/vector-store.ts:31](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L31)

Deletes all vectors for a specific tenant or document.

#### Parameters

##### tenantId

`string`

##### documentId?

`string`

#### Returns

`Promise`\<`void`\>

---

### query()

> `abstract` **query**(`tenantId`, `vector`, `topK`, `options?`):
> `Promise`\<[`VectorRecord`](../interfaces/VectorRecord.md)[]\>

Defined in:
[rag/vector-store.ts:26](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L26)

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

---

### upsert()

> `abstract` **upsert**(`tenantId`, `records`): `Promise`\<`void`\>

Defined in:
[rag/vector-store.ts:21](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/vector-store.ts#L21)

Upserts vectors into a specific tenant's namespace.

#### Parameters

##### tenantId

`string`

##### records

[`VectorRecord`](../interfaces/VectorRecord.md)[]

#### Returns

`Promise`\<`void`\>

[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/copilot](../README.md) / RAGEngine

# Class: RAGEngine

Defined in:
[rag/engine.ts:13](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/engine.ts#L13)

Retrieval-Augmented Generation (RAG) Engine specifically tuned for Legal
Documents. Integrates hierarchical chunking, vector search, and legal rules
validation.

## Constructors

### Constructor

> **new RAGEngine**(`apiKey`, `options`): `RAGEngine`

Defined in:
[rag/engine.ts:21](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/engine.ts#L21)

#### Parameters

##### apiKey

`string`

API Key for the embedding service (e.g., OpenAI).

##### options

Configuration options for vector store and embeddings.

###### embeddingService?

`EmbeddingService`

###### useMock?

`boolean`

###### vectorStore?

[`VectorStore`](VectorStore.md)

#### Returns

`RAGEngine`

## Methods

### generateDraft()

> **generateDraft**(`templateType`, `prompt`, `context`): `Promise`\<\{
> `content`: `string`; `triggeredRule?`: `string`; `warnings?`: `string`[]; \}\>

Defined in:
[rag/engine.ts:80](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/engine.ts#L80)

Generates a legal draft based on a template type, prompt, and optional context.

#### Parameters

##### templateType

`string`

The type of document to generate (e.g., 'NDA', 'PKS').

##### prompt

`string`

The user's specific instructions for the draft.

##### context

`string`[] = `[]`

Optional array of strings providing context (e.g., from case documents).

#### Returns

`Promise`\<\{ `content`: `string`; `triggeredRule?`: `string`; `warnings?`:
`string`[]; \}\>

The generated draft content, any warnings, and the triggered rule if applicable.

---

### generateResponse()

> **generateResponse**(`query`, `tenantId`, `options`): `Promise`\<\{ `answer`:
> `string`; `citations?`: `string`[]; `warnings?`: `string`[]; \}\>

Defined in:
[rag/engine.ts:110](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/engine.ts#L110)

Processes a natural language legal query, retrieves relevant context from the
vector store, and validates the context against predefined legal rules.

#### Parameters

##### query

`string`

The user's query (will be automatically masked for PII).

##### tenantId

`string`

The tenant's ID for data isolation.

##### options

Additional options like document type and case ID for filtering.

###### authorized?

`boolean`

###### caseId?

`string`

###### docType?

`string`

#### Returns

`Promise`\<\{ `answer`: `string`; `citations?`: `string`[]; `warnings?`:
`string`[]; \}\>

The AI-generated answer, citations, and any compliance warnings.

---

### indexDocument()

> **indexDocument**(`tenantId`, `documentId`, `content`): `Promise`\<`void`\>

Defined in:
[rag/engine.ts:48](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/engine.ts#L48)

Indexes a legal document by breaking it into hierarchical chunks, generating
embeddings, and storing them in the tenant-isolated vector store. Includes
automated PII masking before storage.

#### Parameters

##### tenantId

`string`

The unique identifier for the law firm/tenant.

##### documentId

`string`

The unique ID for the document (e.g., 'UU-PDP-2022').

##### content

`string`

The full text content of the document.

#### Returns

`Promise`\<`void`\>

#### Example

```typescript
await engine.indexDocument('firm_1', 'law_001', 'Bab I: Ketentuan Umum...');
```

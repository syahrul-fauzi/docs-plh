[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/copilot](../README.md) / LegalChunker

# Class: LegalChunker

Defined in: [rag/chunking.ts:9](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/chunking.ts#L9)

## Constructors

### Constructor

> **new LegalChunker**(): `LegalChunker`

#### Returns

`LegalChunker`

## Methods

### hierarchicalChunk()

> `static` **hierarchicalChunk**(`text`, `documentId`): [`Chunk`](../interfaces/Chunk.md)[]

Defined in: [rag/chunking.ts:14](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/copilot/src/rag/chunking.ts#L14)

Chunks a legal document hierarchically based on common legal document structures.
e.g., "BAB I", "Pasal 1", "Ayat (1)", etc.

#### Parameters

##### text

`string`

##### documentId

`string`

#### Returns

[`Chunk`](../interfaces/Chunk.md)[]

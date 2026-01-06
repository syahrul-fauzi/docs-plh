[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/core](../README.md) / StorageService

# Class: StorageService

Defined in: [packages/core/src/storage.ts:12](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/storage.ts#L12)

## Constructors

### Constructor

> **new StorageService**(`options`): `StorageService`

Defined in: [packages/core/src/storage.ts:16](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/storage.ts#L16)

#### Parameters

##### options

[`StorageOptions`](../interfaces/StorageOptions.md)

#### Returns

`StorageService`

## Methods

### getDownloadUrl()

> **getDownloadUrl**(`key`): `Promise`\<`string`\>

Defined in: [packages/core/src/storage.ts:35](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/storage.ts#L35)

#### Parameters

##### key

`string`

#### Returns

`Promise`\<`string`\>

***

### upload()

> **upload**(`key`, `body`, `contentType?`): `Promise`\<`PutObjectCommandOutput`\>

Defined in: [packages/core/src/storage.ts:24](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/storage.ts#L24)

#### Parameters

##### key

`string`

##### body

`string` | `Buffer`\<`ArrayBufferLike`\>

##### contentType?

`string`

#### Returns

`Promise`\<`PutObjectCommandOutput`\>

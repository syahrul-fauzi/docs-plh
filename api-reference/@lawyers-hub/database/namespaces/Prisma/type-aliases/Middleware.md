[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Middleware

# Type Alias: Middleware()\<T\>

> **Middleware**\<`T`\> = (`params`, `next`) => `$Utils.JsPromise`\<`T`\>

Defined in: node\_modules/.prisma/client/index.d.ts:2023

The `T` type makes sure, that the `return proceed` is not forgotten in the middleware implementation

## Type Parameters

### T

`T` = `any`

## Parameters

### params

[`MiddlewareParams`](MiddlewareParams.md)

### next

(`params`) => `$Utils.JsPromise`\<`T`\>

## Returns

`$Utils.JsPromise`\<`T`\>

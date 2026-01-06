[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetTenantGroupByPayload

# Type Alias: GetTenantGroupByPayload\<T\>

> **GetTenantGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`TenantGroupByOutputType`](TenantGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof TenantGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], TenantGroupByOutputType[P]> : GetScalarType<T[P], TenantGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:2530

## Type Parameters

### T

`T` *extends* [`TenantGroupByArgs`](TenantGroupByArgs.md)

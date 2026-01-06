[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetAuditLogGroupByPayload

# Type Alias: GetAuditLogGroupByPayload\<T\>

> **GetAuditLogGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`AuditLogGroupByOutputType`](AuditLogGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof AuditLogGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], AuditLogGroupByOutputType[P]> : GetScalarType<T[P], AuditLogGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:9965

## Type Parameters

### T

`T` *extends* [`AuditLogGroupByArgs`](AuditLogGroupByArgs.md)

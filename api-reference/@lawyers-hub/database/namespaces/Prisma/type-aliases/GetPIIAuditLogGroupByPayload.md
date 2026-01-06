[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetPIIAuditLogGroupByPayload

# Type Alias: GetPIIAuditLogGroupByPayload\<T\>

> **GetPIIAuditLogGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`PIIAuditLogGroupByOutputType`](PIIAuditLogGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof PIIAuditLogGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], PIIAuditLogGroupByOutputType[P]> : GetScalarType<T[P], PIIAuditLogGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:16996

## Type Parameters

### T

`T` *extends* [`PIIAuditLogGroupByArgs`](PIIAuditLogGroupByArgs.md)

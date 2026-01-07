[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetCaseGroupByPayload

# Type Alias: GetCaseGroupByPayload\<T\>

> **GetCaseGroupByPayload**\<`T`\> =
> [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`CaseGroupByOutputType`](CaseGroupByOutputType.md),
> `T`\[`"by"`\]\> &
> `{ [P in keyof T & keyof CaseGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], CaseGroupByOutputType[P]> : GetScalarType<T[P], CaseGroupByOutputType[P]> }`[]\>

Defined in: node_modules/.prisma/client/index.d.ts:5862

## Type Parameters

### T

`T` _extends_ [`CaseGroupByArgs`](CaseGroupByArgs.md)

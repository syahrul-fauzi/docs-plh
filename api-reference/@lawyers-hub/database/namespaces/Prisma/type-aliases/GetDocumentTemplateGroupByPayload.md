[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetDocumentTemplateGroupByPayload

# Type Alias: GetDocumentTemplateGroupByPayload\<T\>

> **GetDocumentTemplateGroupByPayload**\<`T`\> =
> [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`DocumentTemplateGroupByOutputType`](DocumentTemplateGroupByOutputType.md),
> `T`\[`"by"`\]\> &
> `{ [P in keyof T & keyof DocumentTemplateGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], DocumentTemplateGroupByOutputType[P]> : GetScalarType<T[P], DocumentTemplateGroupByOutputType[P]> }`[]\>

Defined in: node_modules/.prisma/client/index.d.ts:12889

## Type Parameters

### T

`T` _extends_ [`DocumentTemplateGroupByArgs`](DocumentTemplateGroupByArgs.md)

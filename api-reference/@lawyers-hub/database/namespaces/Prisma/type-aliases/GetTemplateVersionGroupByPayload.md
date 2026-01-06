[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetTemplateVersionGroupByPayload

# Type Alias: GetTemplateVersionGroupByPayload\<T\>

> **GetTemplateVersionGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`TemplateVersionGroupByOutputType`](TemplateVersionGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof TemplateVersionGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], TemplateVersionGroupByOutputType[P]> : GetScalarType<T[P], TemplateVersionGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:13906

## Type Parameters

### T

`T` *extends* [`TemplateVersionGroupByArgs`](TemplateVersionGroupByArgs.md)

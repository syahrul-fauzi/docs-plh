[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetLogType

# Type Alias: GetLogType\<T\>

> **GetLogType**\<`T`\> = `T` *extends* [`LogDefinition`](LogDefinition.md) ? `T`\[`"emit"`\] *extends* `"event"` ? `T`\[`"level"`\] : `never` : `never`

Defined in: node\_modules/.prisma/client/index.d.ts:1966

## Type Parameters

### T

`T` *extends* [`LogLevel`](LogLevel.md) \| [`LogDefinition`](LogDefinition.md)

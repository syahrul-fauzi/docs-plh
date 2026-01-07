[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetLogType

# Type Alias: GetLogType\<T\>

> **GetLogType**\<`T`\> = `T` _extends_ [`LogDefinition`](LogDefinition.md) ?
> `T`\[`"emit"`\] _extends_ `"event"` ? `T`\[`"level"`\] : `never` : `never`

Defined in: node_modules/.prisma/client/index.d.ts:1966

## Type Parameters

### T

`T` _extends_ [`LogLevel`](LogLevel.md) \| [`LogDefinition`](LogDefinition.md)

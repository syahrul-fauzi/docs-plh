[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
TruthyKeys

# Type Alias: TruthyKeys\<T\>

> **TruthyKeys**\<`T`\> = keyof \{ \[K in keyof T as T\[K\] extends false \|
> undefined \| null ? never : K\]: K \}

Defined in: node_modules/.prisma/client/index.d.ts:542

## Type Parameters

### T

`T`

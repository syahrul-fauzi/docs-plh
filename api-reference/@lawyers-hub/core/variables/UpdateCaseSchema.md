[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/core](../README.md) / UpdateCaseSchema

# Variable: UpdateCaseSchema

> `const` **UpdateCaseSchema**: `ZodObject`\<\{ `description`: `ZodOptional`\<`ZodOptional`\<`ZodString`\>\>; `status`: `ZodOptional`\<`ZodDefault`\<`ZodEnum`\<\[`"OPEN"`, `"CLOSED"`, `"ARCHIVED"`\]\>\>\>; `title`: `ZodOptional`\<`ZodString`\>; \}, `"strip"`, `ZodTypeAny`, \{ `description?`: `string`; `status?`: `"OPEN"` \| `"CLOSED"` \| `"ARCHIVED"`; `title?`: `string`; \}, \{ `description?`: `string`; `status?`: `"OPEN"` \| `"CLOSED"` \| `"ARCHIVED"`; `title?`: `string`; \}\>

Defined in: [packages/core/src/validation.ts:41](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/validation.ts#L41)

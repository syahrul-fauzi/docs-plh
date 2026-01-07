[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/core](../README.md) / CreateCaseSchema

# Variable: CreateCaseSchema

> `const` **CreateCaseSchema**: `ZodObject`\<\{ `description`:
> `ZodOptional`\<`ZodString`\>; `status`: `ZodDefault`\<`ZodEnum`\<\[`"OPEN"`,
> `"CLOSED"`, `"ARCHIVED"`\]\>\>; `title`: `ZodString`; \}, `"strip"`,
> `ZodTypeAny`, \{ `description?`: `string`; `status`: `"OPEN"` \| `"CLOSED"` \|
> `"ARCHIVED"`; `title`: `string`; \}, \{ `description?`: `string`; `status?`:
> `"OPEN"` \| `"CLOSED"` \| `"ARCHIVED"`; `title`: `string`; \}\>

Defined in:
[packages/core/src/validation.ts:33](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/validation.ts#L33)

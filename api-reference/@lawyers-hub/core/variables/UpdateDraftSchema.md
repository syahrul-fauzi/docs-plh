[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/core](../README.md) / UpdateDraftSchema

# Variable: UpdateDraftSchema

> `const` **UpdateDraftSchema**: `ZodObject`\<\{ `caseId`: `ZodOptional`\<`ZodOptional`\<`ZodString`\>\>; `content`: `ZodOptional`\<`ZodString`\>; `status`: `ZodOptional`\<`ZodDefault`\<`ZodEnum`\<\[`"DRAFT"`, `"REVIEW"`, `"FINAL"`\]\>\>\>; `templateType`: `ZodOptional`\<`ZodOptional`\<`ZodString`\>\>; `title`: `ZodOptional`\<`ZodString`\>; \}, `"strip"`, `ZodTypeAny`, \{ `caseId?`: `string`; `content?`: `string`; `status?`: `"DRAFT"` \| `"REVIEW"` \| `"FINAL"`; `templateType?`: `string`; `title?`: `string`; \}, \{ `caseId?`: `string`; `content?`: `string`; `status?`: `"DRAFT"` \| `"REVIEW"` \| `"FINAL"`; `templateType?`: `string`; `title?`: `string`; \}\>

Defined in: [packages/core/src/validation.ts:55](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/core/src/validation.ts#L55)

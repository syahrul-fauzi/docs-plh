[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/auth](../README.md) / unmaskPII

# Function: unmaskPII()

> **unmaskPII**(`maskedText`, `mappings`): `string`

Defined in: [masking.ts:267](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L267)

Reverses the masking process by replacing placeholders with their original values.

## Parameters

### maskedText

`string`

The text with placeholders.

### mappings

`Record`\<`string`, `string`\>

The map of placeholder to original value.

## Returns

`string`

The original text with PII restored.

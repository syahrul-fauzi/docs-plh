[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/auth](../README.md) / MaskingResult

# Interface: MaskingResult

Defined in: [masking.ts:184](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L184)

Result of a masking operation, containing the redacted text and a map of original values.

## Properties

### mappings

> **mappings**: `Record`\<`string`, `string`\>

Defined in: [masking.ts:188](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L188)

A map of placeholder string to original sensitive value

***

### maskedText

> **maskedText**: `string`

Defined in: [masking.ts:186](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L186)

The text with sensitive information replaced by placeholders

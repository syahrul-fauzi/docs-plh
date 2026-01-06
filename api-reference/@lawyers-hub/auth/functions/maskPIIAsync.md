[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/auth](../README.md) / maskPIIAsync

# Function: maskPIIAsync()

> **maskPIIAsync**(`text`, `threshold`): `Promise`\<[`MaskingResult`](../interfaces/MaskingResult.md)\>

Defined in: [masking.ts:198](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L198)

Asynchronously masks all detected PII in a string using both local and Presidio detection.

## Parameters

### text

`string`

The raw input text to mask.

### threshold

`number` = `0.7`

Confidence threshold for masking (default: 0.7).

## Returns

`Promise`\<[`MaskingResult`](../interfaces/MaskingResult.md)\>

A MaskingResult object with redacted text and mapping.

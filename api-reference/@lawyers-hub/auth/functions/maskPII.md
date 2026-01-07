[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/auth](../README.md) / maskPII

# Function: maskPII()

> **maskPII**(`text`, `threshold`):
> [`MaskingResult`](../interfaces/MaskingResult.md)

Defined in:
[masking.ts:238](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L238)

Synchronously masks all detected PII in a string using local regex-based
detection only.

## Parameters

### text

`string`

The raw input text to mask.

### threshold

`number` = `0.7`

Confidence threshold for masking (default: 0.7).

## Returns

[`MaskingResult`](../interfaces/MaskingResult.md)

A MaskingResult object with redacted text and mapping.

## Example

```typescript
const result = maskPII('Hubungi Budi di 08123456789');
console.log(result.maskedText); // "Hubungi [PERSON_...] di [PHONE_...]"
```

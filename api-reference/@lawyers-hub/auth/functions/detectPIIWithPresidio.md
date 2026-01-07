[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/auth](../README.md) / detectPIIWithPresidio

# Function: detectPIIWithPresidio()

> **detectPIIWithPresidio**(`text`, `language`):
> `Promise`\<[`PIIFinding`](../interfaces/PIIFinding.md)[]\>

Defined in:
[masking.ts:124](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L124)

Enhanced PII detection using Microsoft Presidio (via API).

## Parameters

### text

`string`

The raw input text to scan.

### language

`string` = `'en'`

The language code for analysis (default: 'en').

## Returns

`Promise`\<[`PIIFinding`](../interfaces/PIIFinding.md)[]\>

An array of PIIFinding objects detected by Presidio.

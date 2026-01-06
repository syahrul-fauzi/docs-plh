[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/auth](../README.md) / detectPII

# Function: detectPII()

> **detectPII**(`text`): [`PIIFinding`](../interfaces/PIIFinding.md)[]

Defined in: [masking.ts:45](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L45)

Detects PII within a given string using a hybrid approach of Regex and Rule-based NER.

Patterns include:
- Emails, Credit Cards, NIK (National ID), NPWP (Tax ID), Phone Numbers, Passports.
- Contextual clues for Person names, Addresses, and Legal Entities.

## Parameters

### text

`string`

The raw input text to scan for PII.

## Returns

[`PIIFinding`](../interfaces/PIIFinding.md)[]

An array of PIIFinding objects, sorted by their position in the text.

## Example

```typescript
const findings = detectPII("Nama saya Budi, NIK saya 1234567890123456.");
console.log(findings);
```

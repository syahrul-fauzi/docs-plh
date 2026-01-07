[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/auth](../README.md) / PIIFinding

# Interface: PIIFinding

Defined in:
[masking.ts:16](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L16)

Represents a single instance of detected PII.

## Properties

### confidence

> **confidence**: `number`

Defined in:
[masking.ts:24](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L24)

Confidence score of the detection (0.0 to 1.0)

---

### index

> **index**: `number`

Defined in:
[masking.ts:22](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L22)

The starting index of the match in the original text

---

### method

> **method**: `"REGEX"` \| `"NER"`

Defined in:
[masking.ts:26](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L26)

The method used for detection

---

### type

> **type**: `string`

Defined in:
[masking.ts:18](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L18)

The type of PII detected (e.g., 'EMAIL', 'NIK', 'PERSON')

---

### value

> **value**: `string`

Defined in:
[masking.ts:20](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/auth/src/masking.ts#L20)

The actual sensitive value found

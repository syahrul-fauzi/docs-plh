[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/rules-engine](../README.md) / RuleTestRunner

# Class: RuleTestRunner

Defined in:
[tester.ts:11](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/tester.ts#L11)

## Constructors

### Constructor

> **new RuleTestRunner**(`customPath?`): `RuleTestRunner`

Defined in:
[tester.ts:14](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/tester.ts#L14)

#### Parameters

##### customPath?

`string`

#### Returns

`RuleTestRunner`

## Methods

### runTests()

> **runTests**(`testCases`): `Promise`\<\{ `failed`: `number`; `passed`:
> `number`; `results`: `any`[]; \}\>

Defined in:
[tester.ts:21](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/tester.ts#L21)

Runs a suite of test cases against the loaded rules.

#### Parameters

##### testCases

`TestCase`[]

#### Returns

`Promise`\<\{ `failed`: `number`; `passed`: `number`; `results`: `any`[]; \}\>

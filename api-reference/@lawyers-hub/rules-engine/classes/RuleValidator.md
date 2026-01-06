[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/rules-engine](../README.md) / RuleValidator

# Class: RuleValidator

Defined in: [validator.ts:10](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/validator.ts#L10)

Core utility for validating and linting Legal Rules in the Lawyers Hub ecosystem.
Supports YAML strings and pre-parsed objects against the standard documentation framework.

## Constructors

### Constructor

> **new RuleValidator**(): `RuleValidator`

#### Returns

`RuleValidator`

## Methods

### validate()

> `static` **validate**(`ruleInput`): `object`

Defined in: [validator.ts:23](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/validator.ts#L23)

Validates a rule object or YAML string against the LH-DOC-RULES-FRAMEWORK schema.

#### Parameters

##### ruleInput

`any`

The rule content to validate (YAML string or parsed Object).

#### Returns

`object`

An object containing the validation result and a list of errors if any.

##### errors

> **errors**: `string`[]

##### valid

> **valid**: `boolean`

#### Example

```typescript
const result = RuleValidator.validate(myYamlString);
if (!result.valid) console.error(result.errors);
```

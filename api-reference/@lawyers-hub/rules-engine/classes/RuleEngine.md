[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/rules-engine](../README.md) / RuleEngine

# Class: RuleEngine

Defined in: enforcement/runtime_enforcer.ts:29

## Constructors

### Constructor

> **new RuleEngine**(`customPath?`): `RuleEngine`

Defined in: enforcement/runtime_enforcer.ts:33

#### Parameters

##### customPath?

`string`

#### Returns

`RuleEngine`

## Methods

### evaluate()

> **evaluate**(`action`, `context`, `taskRules`): `Promise`\<\{ `allowed`:
> `boolean`; `message?`: `string`; `triggeredRule?`: `string`; \}\>

Defined in: enforcement/runtime_enforcer.ts:83

#### Parameters

##### action

`any`

##### context

`any`

##### taskRules

[`Rule`](../interfaces/Rule.md)[] = `[]`

#### Returns

`Promise`\<\{ `allowed`: `boolean`; `message?`: `string`; `triggeredRule?`:
`string`; \}\>

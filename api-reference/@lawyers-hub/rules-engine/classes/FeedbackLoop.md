[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/rules-engine](../README.md) / FeedbackLoop

# Class: FeedbackLoop

Defined in: [feedback.ts:14](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/feedback.ts#L14)

## Constructors

### Constructor

> **new FeedbackLoop**(): `FeedbackLoop`

Defined in: [feedback.ts:18](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/feedback.ts#L18)

#### Returns

`FeedbackLoop`

## Methods

### analyzePatterns()

> **analyzePatterns**(`ruleId`): `Promise`\<\{ `action`: `string`; `confidence`: `number`; `reason`: `string`; `rule_id`: `string`; \} \| `null`\>

Defined in: [feedback.ts:60](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/feedback.ts#L60)

Analyzes feedback patterns to suggest rule adjustments (Automated PDCA).

#### Parameters

##### ruleId

`string`

#### Returns

`Promise`\<\{ `action`: `string`; `confidence`: `number`; `reason`: `string`; `rule_id`: `string`; \} \| `null`\>

***

### getFeedbackForRule()

> **getFeedbackForRule**(`ruleId`): [`RuleFeedback`](../interfaces/RuleFeedback.md)[]

Defined in: [feedback.ts:43](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/feedback.ts#L43)

#### Parameters

##### ruleId

`string`

#### Returns

[`RuleFeedback`](../interfaces/RuleFeedback.md)[]

***

### submitFeedback()

> **submitFeedback**(`feedback`): `void`

Defined in: [feedback.ts:30](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/feedback.ts#L30)

#### Parameters

##### feedback

`Omit`\<[`RuleFeedback`](../interfaces/RuleFeedback.md), `"timestamp"`\>

#### Returns

`void`

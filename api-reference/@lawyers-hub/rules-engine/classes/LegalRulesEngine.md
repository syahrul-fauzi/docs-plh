[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/rules-engine](../README.md) / LegalRulesEngine

# Class: LegalRulesEngine

Defined in: [index.ts:38](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L38)

LegalRulesEngine

Provides deterministic logic for enforcing legal and compliance rules across the platform.
It serves as a complementary layer to AI responses, ensuring high-risk actions are 
validated against codified laws and ethical standards.

Features:
- Deterministic Rule Enforcement (Level 1-3)
- Multi-Agent Oversight (AgentSupervisor)
- Automated Audit Logging
- PDCA (Plan-Do-Check-Act) Feedback Loop
- Telemetry & Performance Monitoring

## Constructors

### Constructor

> **new LegalRulesEngine**(): `LegalRulesEngine`

#### Returns

`LegalRulesEngine`

## Methods

### analyzeRulePatterns()

> `static` **analyzeRulePatterns**(`ruleId`): `Promise`\<\{ `action`: `string`; `confidence`: `number`; `reason`: `string`; `rule_id`: `string`; \} \| `null`\>

Defined in: [index.ts:112](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L112)

Analyzes rule feedback patterns (Automated PDCA).

#### Parameters

##### ruleId

`string`

#### Returns

`Promise`\<\{ `action`: `string`; `confidence`: `number`; `reason`: `string`; `rule_id`: `string`; \} \| `null`\>

***

### evaluateAgentAction()

> `static` **evaluateAgentAction**(`action`, `context`, `taskRules`): `Promise`\<\{ `allowed`: `boolean`; `message?`: `string`; `metadata`: \{ `duration_ms`: `number`; `timestamp`: `string`; \}; `triggeredRule?`: `string`; \}\>

Defined in: [index.ts:58](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L58)

Evaluates an agent's intended action against codified rules.

#### Parameters

##### action

`any`

The action the agent wants to perform (e.g., `{ type: 'delete_user', userId: 123 }`).

##### context

`any`

The execution context (e.g., `{ userRole: 'admin', ip: '1.2.3.4' }`).

##### taskRules

[`Rule`](../interfaces/Rule.md)[] = `[]`

Optional ad-hoc rules specific to the current task.

#### Returns

`Promise`\<\{ `allowed`: `boolean`; `message?`: `string`; `metadata`: \{ `duration_ms`: `number`; `timestamp`: `string`; \}; `triggeredRule?`: `string`; \}\>

An evaluation result containing `allowed: boolean` and optional `message`.

#### Example

```typescript
const result = await LegalRulesEngine.evaluateAgentAction(action, context);
if (!result.allowed) throw new Error(result.message);
```

***

### getAppealDeadline()

> `static` **getAppealDeadline**(`decisionDate`): `Date`

Defined in: [index.ts:156](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L156)

Example rule: Calculate legal deadline for appealing a court decision (Verzet).
Usually 14 days after the decision is notified.

#### Parameters

##### decisionDate

`Date`

#### Returns

`Date`

***

### getFeedbackForRule()

> `static` **getFeedbackForRule**(`ruleId`): [`RuleFeedback`](../interfaces/RuleFeedback.md)[]

Defined in: [index.ts:105](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L105)

Gets all feedback for a specific rule.

#### Parameters

##### ruleId

`string`

#### Returns

[`RuleFeedback`](../interfaces/RuleFeedback.md)[]

***

### getPrometheusMetrics()

> `static` **getPrometheusMetrics**(): `string`

Defined in: [index.ts:119](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L119)

Gets execution metrics for rules in Prometheus format.

#### Returns

`string`

***

### getRecentLogs()

> `static` **getRecentLogs**(`limit`): `AuditEntry`[]

Defined in: [index.ts:91](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L91)

Gets recent audit logs.

#### Parameters

##### limit

`number` = `100`

#### Returns

`AuditEntry`[]

***

### isLegalMarriageAge()

> `static` **isLegalMarriageAge**(`age`): `object`

Defined in: [index.ts:142](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L142)

Example rule: Check if a person is of legal age for marriage in Indonesia.
Based on Law No. 16 of 2019.

#### Parameters

##### age

`number`

#### Returns

`object`

##### allowed

> **allowed**: `boolean`

##### reason?

> `optional` **reason**: `string`

***

### runTests()

> `static` **runTests**(`testCases`): `Promise`\<\{ `failed`: `number`; `passed`: `number`; `results`: `any`[]; \}\>

Defined in: [index.ts:133](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L133)

Runs tests for rules.

#### Parameters

##### testCases

`any`[]

#### Returns

`Promise`\<\{ `failed`: `number`; `passed`: `number`; `results`: `any`[]; \}\>

***

### submitFeedback()

> `static` **submitFeedback**(`feedback`): `void`

Defined in: [index.ts:98](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L98)

Submits feedback for a rule decision (PDCA cycle).

#### Parameters

##### feedback

`Omit`\<[`RuleFeedback`](../interfaces/RuleFeedback.md), `"timestamp"`\>

#### Returns

`void`

***

### validateClauses()

> `static` **validateClauses**(`docType`, `content`): `string`[]

Defined in: [index.ts:165](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L165)

Validates if mandatory clauses are present in the content based on document type.

#### Parameters

##### docType

`string`

##### content

`string`

#### Returns

`string`[]

***

### validateRule()

> `static` **validateRule**(`rule`): `object`

Defined in: [index.ts:126](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/index.ts#L126)

Validates a rule object.

#### Parameters

##### rule

`any`

#### Returns

`object`

##### errors

> **errors**: `string`[]

##### valid

> **valid**: `boolean`

[**Lawyers Hub API Reference**](../../../README.md)

---

[Lawyers Hub API Reference](../../../packages.md) /
[@lawyers-hub/rules-engine](../README.md) / AgentSupervisor

# Class: AgentSupervisor

Defined in:
[supervisor.ts:21](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/supervisor.ts#L21)

AgentSupervisor Coordinates between AI Agents and the LegalRulesEngine.
Implements the "Supervisor Agent" pattern for strategic oversight.

## Constructors

### Constructor

> **new AgentSupervisor**(): `AgentSupervisor`

#### Returns

`AgentSupervisor`

## Methods

### analyzeFeedbackForImprovements()

> `static` **analyzeFeedbackForImprovements**(`ruleId`): `Promise`\<\{ `reason`:
> `string`; `rule_id`: `string`; `suggestion`: `string`; \} \| `null`\>

Defined in:
[supervisor.ts:62](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/supervisor.ts#L62)

Automated PDCA Cycle: Analyzes feedback and suggests rule adjustments.

#### Parameters

##### ruleId

`string`

#### Returns

`Promise`\<\{ `reason`: `string`; `rule_id`: `string`; `suggestion`: `string`;
\} \| `null`\>

---

### oversee()

> `static` **oversee**(`action`, `context`, `taskRules`):
> `Promise`\<[`SupervisorResponse`](../interfaces/SupervisorResponse.md)\>

Defined in:
[supervisor.ts:28](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/supervisor.ts#L28)

Processes an agent's proposed action.

1. Evaluates against deterministic legal rules.
2. If blocked, attempts to suggest a compliant alternative (AI-driven).
3. Logs the entire coordination process.

#### Parameters

##### action

[`AgentAction`](../interfaces/AgentAction.md)

##### context

`any`

##### taskRules

[`Rule`](../interfaces/Rule.md)[] = `[]`

#### Returns

`Promise`\<[`SupervisorResponse`](../interfaces/SupervisorResponse.md)\>

[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/rules-engine](../README.md) / RuleTelemetry

# Class: RuleTelemetry

Defined in: [telemetry.ts:12](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/telemetry.ts#L12)

## Constructors

### Constructor

> **new RuleTelemetry**(): `RuleTelemetry`

Defined in: [telemetry.ts:17](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/telemetry.ts#L17)

#### Returns

`RuleTelemetry`

## Methods

### exportPrometheus()

> **exportPrometheus**(): `string`

Defined in: [telemetry.ts:80](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/telemetry.ts#L80)

Exports metrics in Prometheus text format.

#### Returns

`string`

***

### getMetrics()

> **getMetrics**(`ruleId?`): `RuleMetric` \| `RuleMetric`[] \| `undefined`

Defined in: [telemetry.ts:72](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/telemetry.ts#L72)

#### Parameters

##### ruleId?

`string`

#### Returns

`RuleMetric` \| `RuleMetric`[] \| `undefined`

***

### recordExecution()

> **recordExecution**(`ruleId`, `isViolation`, `durationMs`): `void`

Defined in: [telemetry.ts:43](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/telemetry.ts#L43)

#### Parameters

##### ruleId

`string`

##### isViolation

`boolean`

##### durationMs

`number`

#### Returns

`void`

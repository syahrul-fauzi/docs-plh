[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/rules-engine](../README.md) / AuditLogger

# Class: AuditLogger

Defined in: [logger.ts:18](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/logger.ts#L18)

## Constructors

### Constructor

> **new AuditLogger**(): `AuditLogger`

Defined in: [logger.ts:24](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/logger.ts#L24)

#### Returns

`AuditLogger`

## Methods

### getRecentLogs()

> **getRecentLogs**(`limit`): `AuditEntry`[]

Defined in: [logger.ts:63](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/logger.ts#L63)

Retrieves the last N audit logs.

#### Parameters

##### limit

`number` = `100`

#### Returns

`AuditEntry`[]

***

### log()

> **log**(`entry`): `void`

Defined in: [logger.ts:40](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/rules-engine/src/logger.ts#L40)

Logs a rule execution event with auto-recovery.
Format: JSON Lines (ELK Compatible)

#### Parameters

##### entry

`Omit`\<`AuditEntry`, `"timestamp"` \| `"level"` \| `"service"` \| `"environment"`\>

#### Returns

`void`

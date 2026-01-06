[**Lawyers Hub API Reference**](../../../README.md)

***

[Lawyers Hub API Reference](../../../packages.md) / [@lawyers-hub/database](../README.md) / withTenant

# Function: withTenant()

> **withTenant**(`tenantId`, `operation`): `Promise`\<`any`\>

Defined in: [packages/database/src/index.ts:9](https://github.com/syahrul-fauzi/lawyers-hub/blob/bbe8186c2ef189749847fb3bf25d0d6cbefb2782/packages/database/src/index.ts#L9)

Utility to apply Row Level Security (RLS) in a transaction.
This sets the 'app.current_tenant' local variable in PostgreSQL.

## Parameters

### tenantId

`string`

### operation

(`tx`) => `Promise`\<`any`\>

## Returns

`Promise`\<`any`\>

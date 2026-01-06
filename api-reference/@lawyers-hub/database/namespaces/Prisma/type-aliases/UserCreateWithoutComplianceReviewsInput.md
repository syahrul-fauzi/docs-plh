[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserCreateWithoutComplianceReviewsInput

# Type Alias: UserCreateWithoutComplianceReviewsInput

> **UserCreateWithoutComplianceReviewsInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:25987

## Properties

### auditLogs?

> `optional` **auditLogs**: [`AuditLogCreateNestedManyWithoutUserInput`](AuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25994

***

### comments?

> `optional` **comments**: [`CommentCreateNestedManyWithoutUserInput`](CommentCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25995

***

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25992

***

### email

> **email**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25989

***

### fullName

> **fullName**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25990

***

### id?

> `optional` **id**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25988

***

### piiAuditLogs?

> `optional` **piiAuditLogs**: [`PIIAuditLogCreateNestedManyWithoutUserInput`](PIIAuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25996

***

### role

> **role**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25991

***

### templateVersions?

> `optional` **templateVersions**: [`TemplateVersionCreateNestedManyWithoutUserInput`](TemplateVersionCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25997

***

### tenant

> **tenant**: [`TenantCreateNestedOneWithoutUsersInput`](TenantCreateNestedOneWithoutUsersInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25998

***

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25993

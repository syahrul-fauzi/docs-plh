[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserCreateWithoutTemplateVersionsInput

# Type Alias: UserCreateWithoutTemplateVersionsInput

> **UserCreateWithoutTemplateVersionsInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:25884

## Properties

### auditLogs?

> `optional` **auditLogs**: [`AuditLogCreateNestedManyWithoutUserInput`](AuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25891

***

### comments?

> `optional` **comments**: [`CommentCreateNestedManyWithoutUserInput`](CommentCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25892

***

### complianceReviews?

> `optional` **complianceReviews**: [`ComplianceReviewCreateNestedManyWithoutReviewerInput`](ComplianceReviewCreateNestedManyWithoutReviewerInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25893

***

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25889

***

### email

> **email**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25886

***

### fullName

> **fullName**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25887

***

### id?

> `optional` **id**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25885

***

### piiAuditLogs?

> `optional` **piiAuditLogs**: [`PIIAuditLogCreateNestedManyWithoutUserInput`](PIIAuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25894

***

### role

> **role**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25888

***

### tenant

> **tenant**: [`TenantCreateNestedOneWithoutUsersInput`](TenantCreateNestedOneWithoutUsersInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:25895

***

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:25890

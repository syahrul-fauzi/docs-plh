[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / UserCreateInput

# Type Alias: UserCreateInput

> **UserCreateInput** = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:19601

## Properties

### auditLogs?

> `optional` **auditLogs**: [`AuditLogCreateNestedManyWithoutUserInput`](AuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:19608

***

### comments?

> `optional` **comments**: [`CommentCreateNestedManyWithoutUserInput`](CommentCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:19609

***

### complianceReviews?

> `optional` **complianceReviews**: [`ComplianceReviewCreateNestedManyWithoutReviewerInput`](ComplianceReviewCreateNestedManyWithoutReviewerInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:19610

***

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19606

***

### email

> **email**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19603

***

### fullName

> **fullName**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19604

***

### id?

> `optional` **id**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19602

***

### piiAuditLogs?

> `optional` **piiAuditLogs**: [`PIIAuditLogCreateNestedManyWithoutUserInput`](PIIAuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:19611

***

### role

> **role**: `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19605

***

### templateVersions?

> `optional` **templateVersions**: [`TemplateVersionCreateNestedManyWithoutUserInput`](TemplateVersionCreateNestedManyWithoutUserInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:19612

***

### tenant

> **tenant**: [`TenantCreateNestedOneWithoutUsersInput`](TenantCreateNestedOneWithoutUsersInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:19613

***

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node\_modules/.prisma/client/index.d.ts:19607

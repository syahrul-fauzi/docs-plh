[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserCreateWithoutAuditLogsInput

# Type Alias: UserCreateWithoutAuditLogsInput

> **UserCreateWithoutAuditLogsInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:25404

## Properties

### comments?

> `optional` **comments**:
> [`CommentCreateNestedManyWithoutUserInput`](CommentCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25411

---

### complianceReviews?

> `optional` **complianceReviews**:
> [`ComplianceReviewCreateNestedManyWithoutReviewerInput`](ComplianceReviewCreateNestedManyWithoutReviewerInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25412

---

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25409

---

### email

> **email**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25406

---

### fullName

> **fullName**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25407

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25405

---

### piiAuditLogs?

> `optional` **piiAuditLogs**:
> [`PIIAuditLogCreateNestedManyWithoutUserInput`](PIIAuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25413

---

### role

> **role**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25408

---

### templateVersions?

> `optional` **templateVersions**:
> [`TemplateVersionCreateNestedManyWithoutUserInput`](TemplateVersionCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25414

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutUsersInput`](TenantCreateNestedOneWithoutUsersInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25415

---

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25410

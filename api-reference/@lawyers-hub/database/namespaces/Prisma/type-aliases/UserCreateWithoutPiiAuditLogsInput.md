[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserCreateWithoutPiiAuditLogsInput

# Type Alias: UserCreateWithoutPiiAuditLogsInput

> **UserCreateWithoutPiiAuditLogsInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:26227

## Properties

### auditLogs?

> `optional` **auditLogs**:
> [`AuditLogCreateNestedManyWithoutUserInput`](AuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:26234

---

### comments?

> `optional` **comments**:
> [`CommentCreateNestedManyWithoutUserInput`](CommentCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:26235

---

### complianceReviews?

> `optional` **complianceReviews**:
> [`ComplianceReviewCreateNestedManyWithoutReviewerInput`](ComplianceReviewCreateNestedManyWithoutReviewerInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:26236

---

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:26232

---

### email

> **email**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:26229

---

### fullName

> **fullName**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:26230

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:26228

---

### role

> **role**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:26231

---

### templateVersions?

> `optional` **templateVersions**:
> [`TemplateVersionCreateNestedManyWithoutUserInput`](TemplateVersionCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:26237

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutUsersInput`](TenantCreateNestedOneWithoutUsersInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:26238

---

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:26233

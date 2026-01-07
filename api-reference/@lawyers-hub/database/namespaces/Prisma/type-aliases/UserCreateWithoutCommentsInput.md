[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserCreateWithoutCommentsInput

# Type Alias: UserCreateWithoutCommentsInput

> **UserCreateWithoutCommentsInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:25164

## Properties

### auditLogs?

> `optional` **auditLogs**:
> [`AuditLogCreateNestedManyWithoutUserInput`](AuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25171

---

### complianceReviews?

> `optional` **complianceReviews**:
> [`ComplianceReviewCreateNestedManyWithoutReviewerInput`](ComplianceReviewCreateNestedManyWithoutReviewerInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25172

---

### createdAt?

> `optional` **createdAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25169

---

### email

> **email**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25166

---

### fullName

> **fullName**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25167

---

### id?

> `optional` **id**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25165

---

### piiAuditLogs?

> `optional` **piiAuditLogs**:
> [`PIIAuditLogCreateNestedManyWithoutUserInput`](PIIAuditLogCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25173

---

### role

> **role**: `string`

Defined in: node_modules/.prisma/client/index.d.ts:25168

---

### templateVersions?

> `optional` **templateVersions**:
> [`TemplateVersionCreateNestedManyWithoutUserInput`](TemplateVersionCreateNestedManyWithoutUserInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25174

---

### tenant

> **tenant**:
> [`TenantCreateNestedOneWithoutUsersInput`](TenantCreateNestedOneWithoutUsersInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25175

---

### updatedAt?

> `optional` **updatedAt**: `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25170

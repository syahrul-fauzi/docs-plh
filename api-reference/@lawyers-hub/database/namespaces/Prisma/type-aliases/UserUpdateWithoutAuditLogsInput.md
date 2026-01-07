[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserUpdateWithoutAuditLogsInput

# Type Alias: UserUpdateWithoutAuditLogsInput

> **UserUpdateWithoutAuditLogsInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:25499

## Properties

### comments?

> `optional` **comments**:
> [`CommentUpdateManyWithoutUserNestedInput`](CommentUpdateManyWithoutUserNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25506

---

### complianceReviews?

> `optional` **complianceReviews**:
> [`ComplianceReviewUpdateManyWithoutReviewerNestedInput`](ComplianceReviewUpdateManyWithoutReviewerNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25507

---

### createdAt?

> `optional` **createdAt**:
> [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md)
> \| `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25504

---

### email?

> `optional` **email**:
> [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:25501

---

### fullName?

> `optional` **fullName**:
> [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:25502

---

### id?

> `optional` **id**:
> [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:25500

---

### piiAuditLogs?

> `optional` **piiAuditLogs**:
> [`PIIAuditLogUpdateManyWithoutUserNestedInput`](PIIAuditLogUpdateManyWithoutUserNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25508

---

### role?

> `optional` **role**:
> [`StringFieldUpdateOperationsInput`](StringFieldUpdateOperationsInput.md) \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:25503

---

### templateVersions?

> `optional` **templateVersions**:
> [`TemplateVersionUpdateManyWithoutUserNestedInput`](TemplateVersionUpdateManyWithoutUserNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25509

---

### tenant?

> `optional` **tenant**:
> [`TenantUpdateOneRequiredWithoutUsersNestedInput`](TenantUpdateOneRequiredWithoutUsersNestedInput.md)

Defined in: node_modules/.prisma/client/index.d.ts:25510

---

### updatedAt?

> `optional` **updatedAt**:
> [`DateTimeFieldUpdateOperationsInput`](DateTimeFieldUpdateOperationsInput.md)
> \| `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:25505

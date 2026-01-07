[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
UserWhereInput

# Type Alias: UserWhereInput

> **UserWhereInput** = `object`

Defined in: node_modules/.prisma/client/index.d.ts:18370

## Properties

### AND?

> `optional` **AND**: `UserWhereInput` \| `UserWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:18371

---

### auditLogs?

> `optional` **auditLogs**:
> [`AuditLogListRelationFilter`](AuditLogListRelationFilter.md)

Defined in: node_modules/.prisma/client/index.d.ts:18381

---

### comments?

> `optional` **comments**:
> [`CommentListRelationFilter`](CommentListRelationFilter.md)

Defined in: node_modules/.prisma/client/index.d.ts:18382

---

### complianceReviews?

> `optional` **complianceReviews**:
> [`ComplianceReviewListRelationFilter`](ComplianceReviewListRelationFilter.md)

Defined in: node_modules/.prisma/client/index.d.ts:18383

---

### createdAt?

> `optional` **createdAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"User"`\> \|
> `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18379

---

### email?

> `optional` **email**: [`StringFilter`](StringFilter.md)\<`"User"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:18375

---

### fullName?

> `optional` **fullName**: [`StringFilter`](StringFilter.md)\<`"User"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:18376

---

### id?

> `optional` **id**: [`StringFilter`](StringFilter.md)\<`"User"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18374

---

### NOT?

> `optional` **NOT**: `UserWhereInput` \| `UserWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:18373

---

### OR?

> `optional` **OR**: `UserWhereInput`[]

Defined in: node_modules/.prisma/client/index.d.ts:18372

---

### piiAuditLogs?

> `optional` **piiAuditLogs**:
> [`PIIAuditLogListRelationFilter`](PIIAuditLogListRelationFilter.md)

Defined in: node_modules/.prisma/client/index.d.ts:18384

---

### role?

> `optional` **role**: [`StringFilter`](StringFilter.md)\<`"User"`\> \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18377

---

### templateVersions?

> `optional` **templateVersions**:
> [`TemplateVersionListRelationFilter`](TemplateVersionListRelationFilter.md)

Defined in: node_modules/.prisma/client/index.d.ts:18385

---

### tenant?

> `optional` **tenant**:
> [`XOR`](XOR.md)\<[`TenantRelationFilter`](TenantRelationFilter.md),
> [`TenantWhereInput`](TenantWhereInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:18386

---

### tenantId?

> `optional` **tenantId**: [`StringFilter`](StringFilter.md)\<`"User"`\> \|
> `string`

Defined in: node_modules/.prisma/client/index.d.ts:18378

---

### updatedAt?

> `optional` **updatedAt**: [`DateTimeFilter`](DateTimeFilter.md)\<`"User"`\> \|
> `Date` \| `string`

Defined in: node_modules/.prisma/client/index.d.ts:18380

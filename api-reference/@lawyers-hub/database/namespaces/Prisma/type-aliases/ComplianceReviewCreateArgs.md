[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
ComplianceReviewCreateArgs

# Type Alias: ComplianceReviewCreateArgs\<ExtArgs\>

> **ComplianceReviewCreateArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:16630

ComplianceReview create

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**:
> [`XOR`](XOR.md)\<[`ComplianceReviewCreateInput`](ComplianceReviewCreateInput.md),
> [`ComplianceReviewUncheckedCreateInput`](ComplianceReviewUncheckedCreateInput.md)\>

Defined in: node_modules/.prisma/client/index.d.ts:16642

The data needed to create a ComplianceReview.

---

### include?

> `optional` **include**:
> [`ComplianceReviewInclude`](ComplianceReviewInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:16638

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`ComplianceReviewSelect`](ComplianceReviewSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:16634

Select specific fields to fetch from the ComplianceReview

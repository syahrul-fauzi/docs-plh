[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
GetComplianceReviewAggregateType

# Type Alias: GetComplianceReviewAggregateType\<T\>

> **GetComplianceReviewAggregateType**\<`T`\> = \{ \[P in keyof T & keyof
> AggregateComplianceReview\]: P extends "\_count" \| "count" ? T\[P\] extends
> true ? number : GetScalarType\<T\[P\], AggregateComplianceReview\[P\]\> :
> GetScalarType\<T\[P\], AggregateComplianceReview\[P\]\> \}

Defined in: node_modules/.prisma/client/index.d.ts:15893

## Type Parameters

### T

`T` _extends_
[`ComplianceReviewAggregateArgs`](ComplianceReviewAggregateArgs.md)

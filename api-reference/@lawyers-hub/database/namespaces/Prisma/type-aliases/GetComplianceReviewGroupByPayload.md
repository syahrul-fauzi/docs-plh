[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / GetComplianceReviewGroupByPayload

# Type Alias: GetComplianceReviewGroupByPayload\<T\>

> **GetComplianceReviewGroupByPayload**\<`T`\> = [`PrismaPromise`](PrismaPromise.md)\<[`PickEnumerable`](PickEnumerable.md)\<[`ComplianceReviewGroupByOutputType`](ComplianceReviewGroupByOutputType.md), `T`\[`"by"`\]\> & `{ [P in keyof T & keyof ComplianceReviewGroupByOutputType]: P extends "_count" ? T[P] extends boolean ? number : GetScalarType<T[P], ComplianceReviewGroupByOutputType[P]> : GetScalarType<T[P], ComplianceReviewGroupByOutputType[P]> }`[]\>

Defined in: node\_modules/.prisma/client/index.d.ts:15940

## Type Parameters

### T

`T` *extends* [`ComplianceReviewGroupByArgs`](ComplianceReviewGroupByArgs.md)

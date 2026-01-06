[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewUpdateArgs

# Type Alias: ComplianceReviewUpdateArgs\<ExtArgs\>

> **ComplianceReviewUpdateArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:16678

ComplianceReview update

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`XOR`](XOR.md)\<[`ComplianceReviewUpdateInput`](ComplianceReviewUpdateInput.md), [`ComplianceReviewUncheckedUpdateInput`](ComplianceReviewUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:16690

The data needed to update a ComplianceReview.

***

### include?

> `optional` **include**: [`ComplianceReviewInclude`](ComplianceReviewInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16686

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`ComplianceReviewSelect`](ComplianceReviewSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16682

Select specific fields to fetch from the ComplianceReview

***

### where

> **where**: [`ComplianceReviewWhereUniqueInput`](ComplianceReviewWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16694

Choose, which ComplianceReview to update.

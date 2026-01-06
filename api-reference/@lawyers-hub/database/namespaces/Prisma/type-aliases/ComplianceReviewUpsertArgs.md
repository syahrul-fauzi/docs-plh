[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewUpsertArgs

# Type Alias: ComplianceReviewUpsertArgs\<ExtArgs\>

> **ComplianceReviewUpsertArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:16714

ComplianceReview upsert

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### create

> **create**: [`XOR`](XOR.md)\<[`ComplianceReviewCreateInput`](ComplianceReviewCreateInput.md), [`ComplianceReviewUncheckedCreateInput`](ComplianceReviewUncheckedCreateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:16730

In case the ComplianceReview found by the `where` argument doesn't exist, create a new ComplianceReview with this data.

***

### include?

> `optional` **include**: [`ComplianceReviewInclude`](ComplianceReviewInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16722

Choose, which related nodes to fetch as well

***

### select?

> `optional` **select**: [`ComplianceReviewSelect`](ComplianceReviewSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16718

Select specific fields to fetch from the ComplianceReview

***

### update

> **update**: [`XOR`](XOR.md)\<[`ComplianceReviewUpdateInput`](ComplianceReviewUpdateInput.md), [`ComplianceReviewUncheckedUpdateInput`](ComplianceReviewUncheckedUpdateInput.md)\>

Defined in: node\_modules/.prisma/client/index.d.ts:16734

In case the ComplianceReview was found with the provided `where` argument, update it with this data.

***

### where

> **where**: [`ComplianceReviewWhereUniqueInput`](ComplianceReviewWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16726

The filter to search for the ComplianceReview to update in case it exists.

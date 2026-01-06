[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewFindManyArgs

# Type Alias: ComplianceReviewFindManyArgs\<ExtArgs\>

> **ComplianceReviewFindManyArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:16587

ComplianceReview findMany

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`ComplianceReviewWhereUniqueInput`](ComplianceReviewWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16611

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for listing ComplianceReviews.

***

### distinct?

> `optional` **distinct**: [`ComplianceReviewScalarFieldEnum`](ComplianceReviewScalarFieldEnum.md) \| [`ComplianceReviewScalarFieldEnum`](ComplianceReviewScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:16624

***

### include?

> `optional` **include**: [`ComplianceReviewInclude`](ComplianceReviewInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16595

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`ComplianceReviewOrderByWithRelationInput`](ComplianceReviewOrderByWithRelationInput.md) \| [`ComplianceReviewOrderByWithRelationInput`](ComplianceReviewOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:16605

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of ComplianceReviews to fetch.

***

### select?

> `optional` **select**: [`ComplianceReviewSelect`](ComplianceReviewSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16591

Select specific fields to fetch from the ComplianceReview

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:16623

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` ComplianceReviews.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:16617

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` ComplianceReviews from the position of the cursor.

***

### where?

> `optional` **where**: [`ComplianceReviewWhereInput`](ComplianceReviewWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16599

Filter, which ComplianceReviews to fetch.

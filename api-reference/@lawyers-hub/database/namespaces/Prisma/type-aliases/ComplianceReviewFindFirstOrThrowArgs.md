[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / ComplianceReviewFindFirstOrThrowArgs

# Type Alias: ComplianceReviewFindFirstOrThrowArgs\<ExtArgs\>

> **ComplianceReviewFindFirstOrThrowArgs**\<`ExtArgs`\> = `object`

Defined in: node\_modules/.prisma/client/index.d.ts:16539

ComplianceReview findFirstOrThrow

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### cursor?

> `optional` **cursor**: [`ComplianceReviewWhereUniqueInput`](ComplianceReviewWhereUniqueInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16563

[Cursor Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination#cursor-based-pagination)

Sets the position for searching for ComplianceReviews.

***

### distinct?

> `optional` **distinct**: [`ComplianceReviewScalarFieldEnum`](ComplianceReviewScalarFieldEnum.md) \| [`ComplianceReviewScalarFieldEnum`](ComplianceReviewScalarFieldEnum.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:16581

[Distinct Docs](https://www.prisma.io/docs/concepts/components/prisma-client/distinct)

Filter by unique combinations of ComplianceReviews.

***

### include?

> `optional` **include**: [`ComplianceReviewInclude`](ComplianceReviewInclude.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16547

Choose, which related nodes to fetch as well

***

### orderBy?

> `optional` **orderBy**: [`ComplianceReviewOrderByWithRelationInput`](ComplianceReviewOrderByWithRelationInput.md) \| [`ComplianceReviewOrderByWithRelationInput`](ComplianceReviewOrderByWithRelationInput.md)[]

Defined in: node\_modules/.prisma/client/index.d.ts:16557

[Sorting Docs](https://www.prisma.io/docs/concepts/components/prisma-client/sorting)

Determine the order of ComplianceReviews to fetch.

***

### select?

> `optional` **select**: [`ComplianceReviewSelect`](ComplianceReviewSelect.md)\<`ExtArgs`\> \| `null`

Defined in: node\_modules/.prisma/client/index.d.ts:16543

Select specific fields to fetch from the ComplianceReview

***

### skip?

> `optional` **skip**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:16575

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Skip the first `n` ComplianceReviews.

***

### take?

> `optional` **take**: `number`

Defined in: node\_modules/.prisma/client/index.d.ts:16569

[Pagination Docs](https://www.prisma.io/docs/concepts/components/prisma-client/pagination)

Take `±n` ComplianceReviews from the position of the cursor.

***

### where?

> `optional` **where**: [`ComplianceReviewWhereInput`](ComplianceReviewWhereInput.md)

Defined in: node\_modules/.prisma/client/index.d.ts:16551

Filter, which ComplianceReview to fetch.

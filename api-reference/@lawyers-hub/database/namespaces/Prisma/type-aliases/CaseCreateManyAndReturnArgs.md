[**Lawyers Hub API Reference**](../../../../../README.md)

---

[Lawyers Hub API Reference](../../../../../packages.md) /
[@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) /
CaseCreateManyAndReturnArgs

# Type Alias: CaseCreateManyAndReturnArgs\<ExtArgs\>

> **CaseCreateManyAndReturnArgs**\<`ExtArgs`\> = `object`

Defined in: node_modules/.prisma/client/index.d.ts:6554

Case createManyAndReturn

## Type Parameters

### ExtArgs

`ExtArgs` _extends_ `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

## Properties

### data

> **data**: [`CaseCreateManyInput`](CaseCreateManyInput.md) \|
> [`CaseCreateManyInput`](CaseCreateManyInput.md)[]

Defined in: node_modules/.prisma/client/index.d.ts:6562

The data used to create many Cases.

---

### include?

> `optional` **include**:
> [`CaseIncludeCreateManyAndReturn`](CaseIncludeCreateManyAndReturn.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:6567

Choose, which related nodes to fetch as well

---

### select?

> `optional` **select**:
> [`CaseSelectCreateManyAndReturn`](CaseSelectCreateManyAndReturn.md)\<`ExtArgs`\>
> \| `null`

Defined in: node_modules/.prisma/client/index.d.ts:6558

Select specific fields to fetch from the Case

---

### skipDuplicates?

> `optional` **skipDuplicates**: `boolean`

Defined in: node_modules/.prisma/client/index.d.ts:6563

[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / Decimal

# Class: Decimal

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:327

## Constructors

### Constructor

> **new Decimal**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:353

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

## Properties

### d

> `readonly` **d**: `number`[]

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:349

***

### e

> `readonly` **e**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:350

***

### s

> `readonly` **s**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:351

***

### crypto

> `readonly` `static` **crypto**: `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:579

***

### Decimal?

> `readonly` `static` `optional` **Decimal**: *typeof* [`Decimal`](../namespaces/Decimal/README.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:571

***

### default?

> `readonly` `static` `optional` **default**: *typeof* [`Decimal`](../namespaces/Decimal/README.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:570

***

### EUCLID

> `readonly` `static` **EUCLID**: `9`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:591

***

### maxE

> `readonly` `static` **maxE**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:578

***

### minE

> `readonly` `static` **minE**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:577

***

### modulo

> `readonly` `static` **modulo**: [`Modulo`](../namespaces/Decimal/type-aliases/Modulo.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:580

***

### precision

> `readonly` `static` **precision**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:573

***

### ROUND\_CEIL

> `readonly` `static` **ROUND\_CEIL**: `2`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:584

***

### ROUND\_DOWN

> `readonly` `static` **ROUND\_DOWN**: `1`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:583

***

### ROUND\_FLOOR

> `readonly` `static` **ROUND\_FLOOR**: `3`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:585

***

### ROUND\_HALF\_CEIL

> `readonly` `static` **ROUND\_HALF\_CEIL**: `7`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:589

***

### ROUND\_HALF\_DOWN

> `readonly` `static` **ROUND\_HALF\_DOWN**: `5`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:587

***

### ROUND\_HALF\_EVEN

> `readonly` `static` **ROUND\_HALF\_EVEN**: `6`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:588

***

### ROUND\_HALF\_FLOOR

> `readonly` `static` **ROUND\_HALF\_FLOOR**: `8`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:590

***

### ROUND\_HALF\_UP

> `readonly` `static` **ROUND\_HALF\_UP**: `4`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:586

***

### ROUND\_UP

> `readonly` `static` **ROUND\_UP**: `0`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:582

***

### rounding

> `readonly` `static` **rounding**: [`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:574

***

### toExpNeg

> `readonly` `static` **toExpNeg**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:575

***

### toExpPos

> `readonly` `static` **toExpPos**: `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:576

## Methods

### abs()

> **abs**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:356

#### Returns

`Decimal`

***

### absoluteValue()

> **absoluteValue**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:355

#### Returns

`Decimal`

***

### acos()

> **acos**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:402

#### Returns

`Decimal`

***

### acosh()

> **acosh**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:405

#### Returns

`Decimal`

***

### add()

> **add**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:459

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### asin()

> **asin**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:414

#### Returns

`Decimal`

***

### asinh()

> **asinh**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:408

#### Returns

`Decimal`

***

### atan()

> **atan**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:417

#### Returns

`Decimal`

***

### atanh()

> **atanh**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:411

#### Returns

`Decimal`

***

### cbrt()

> **cbrt**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:370

#### Returns

`Decimal`

***

### ceil()

> **ceil**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:358

#### Returns

`Decimal`

***

### clamp()

> **clamp**(`min`, `max`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:361

#### Parameters

##### min

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### max

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### clampedTo()

> **clampedTo**(`min`, `max`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:360

#### Parameters

##### min

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### max

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### cmp()

> **cmp**(`n`): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:364

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`number`

***

### comparedTo()

> **comparedTo**(`n`): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:363

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`number`

***

### cos()

> **cos**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:367

#### Returns

`Decimal`

***

### cosh()

> **cosh**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:393

#### Returns

`Decimal`

***

### cosine()

> **cosine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:366

#### Returns

`Decimal`

***

### cubeRoot()

> **cubeRoot**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:369

#### Returns

`Decimal`

***

### decimalPlaces()

> **decimalPlaces**(): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:372

#### Returns

`number`

***

### div()

> **div**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:376

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### dividedBy()

> **dividedBy**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:375

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### dividedToIntegerBy()

> **dividedToIntegerBy**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:378

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### divToInt()

> **divToInt**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:379

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### dp()

> **dp**(): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:373

#### Returns

`number`

***

### eq()

> **eq**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:382

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### equals()

> **equals**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:381

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### exp()

> **exp**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:450

#### Returns

`Decimal`

***

### floor()

> **floor**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:384

#### Returns

`Decimal`

***

### greaterThan()

> **greaterThan**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:386

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### greaterThanOrEqualTo()

> **greaterThanOrEqualTo**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:389

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### gt()

> **gt**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:387

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### gte()

> **gte**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:390

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### hyperbolicCosine()

> **hyperbolicCosine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:392

#### Returns

`Decimal`

***

### hyperbolicSine()

> **hyperbolicSine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:395

#### Returns

`Decimal`

***

### hyperbolicTangent()

> **hyperbolicTangent**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:398

#### Returns

`Decimal`

***

### inverseCosine()

> **inverseCosine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:401

#### Returns

`Decimal`

***

### inverseHyperbolicCosine()

> **inverseHyperbolicCosine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:404

#### Returns

`Decimal`

***

### inverseHyperbolicSine()

> **inverseHyperbolicSine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:407

#### Returns

`Decimal`

***

### inverseHyperbolicTangent()

> **inverseHyperbolicTangent**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:410

#### Returns

`Decimal`

***

### inverseSine()

> **inverseSine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:413

#### Returns

`Decimal`

***

### inverseTangent()

> **inverseTangent**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:416

#### Returns

`Decimal`

***

### isFinite()

> **isFinite**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:419

#### Returns

`boolean`

***

### isInt()

> **isInt**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:422

#### Returns

`boolean`

***

### isInteger()

> **isInteger**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:421

#### Returns

`boolean`

***

### isNaN()

> **isNaN**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:424

#### Returns

`boolean`

***

### isNeg()

> **isNeg**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:427

#### Returns

`boolean`

***

### isNegative()

> **isNegative**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:426

#### Returns

`boolean`

***

### isPos()

> **isPos**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:430

#### Returns

`boolean`

***

### isPositive()

> **isPositive**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:429

#### Returns

`boolean`

***

### isZero()

> **isZero**(): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:432

#### Returns

`boolean`

***

### lessThan()

> **lessThan**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:434

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### lessThanOrEqualTo()

> **lessThanOrEqualTo**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:437

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### ln()

> **ln**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:453

#### Returns

`Decimal`

***

### log()

> **log**(`n?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:441

#### Parameters

##### n?

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### logarithm()

> **logarithm**(`n?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:440

#### Parameters

##### n?

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### lt()

> **lt**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:435

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### lte()

> **lte**(`n`): `boolean`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:438

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`boolean`

***

### minus()

> **minus**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:443

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### mod()

> **mod**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:447

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### modulo()

> **modulo**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:446

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### mul()

> **mul**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:476

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### naturalExponential()

> **naturalExponential**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:449

#### Returns

`Decimal`

***

### naturalLogarithm()

> **naturalLogarithm**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:452

#### Returns

`Decimal`

***

### neg()

> **neg**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:456

#### Returns

`Decimal`

***

### negated()

> **negated**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:455

#### Returns

`Decimal`

***

### plus()

> **plus**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:458

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### pow()

> **pow**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:509

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### precision()

> **precision**(`includeZeros?`): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:461

#### Parameters

##### includeZeros?

`boolean`

#### Returns

`number`

***

### round()

> **round**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:464

#### Returns

`Decimal`

***

### sd()

> **sd**(`includeZeros?`): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:462

#### Parameters

##### includeZeros?

`boolean`

#### Returns

`number`

***

### sin()

> **sin**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:467

#### Returns

`Decimal`

***

### sine()

> **sine**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:466

#### Returns

`Decimal`

***

### sinh()

> **sinh**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:396

#### Returns

`Decimal`

***

### sqrt()

> **sqrt**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:470

#### Returns

`Decimal`

***

### squareRoot()

> **squareRoot**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:469

#### Returns

`Decimal`

***

### sub()

> **sub**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:444

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### tan()

> **tan**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:473

#### Returns

`Decimal`

***

### tangent()

> **tangent**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:472

#### Returns

`Decimal`

***

### tanh()

> **tanh**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:399

#### Returns

`Decimal`

***

### times()

> **times**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:475

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### toBinary()

#### Call Signature

> **toBinary**(`significantDigits?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:478

##### Parameters

###### significantDigits?

`number`

##### Returns

`string`

#### Call Signature

> **toBinary**(`significantDigits`, `rounding`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:479

##### Parameters

###### significantDigits

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toDecimalPlaces()

#### Call Signature

> **toDecimalPlaces**(`decimalPlaces?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:481

##### Parameters

###### decimalPlaces?

`number`

##### Returns

`Decimal`

#### Call Signature

> **toDecimalPlaces**(`decimalPlaces`, `rounding`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:482

##### Parameters

###### decimalPlaces

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`Decimal`

***

### toDP()

#### Call Signature

> **toDP**(`decimalPlaces?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:483

##### Parameters

###### decimalPlaces?

`number`

##### Returns

`Decimal`

#### Call Signature

> **toDP**(`decimalPlaces`, `rounding`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:484

##### Parameters

###### decimalPlaces

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`Decimal`

***

### toExponential()

#### Call Signature

> **toExponential**(`decimalPlaces?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:486

##### Parameters

###### decimalPlaces?

`number`

##### Returns

`string`

#### Call Signature

> **toExponential**(`decimalPlaces`, `rounding`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:487

##### Parameters

###### decimalPlaces

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toFixed()

#### Call Signature

> **toFixed**(`decimalPlaces?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:489

##### Parameters

###### decimalPlaces?

`number`

##### Returns

`string`

#### Call Signature

> **toFixed**(`decimalPlaces`, `rounding`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:490

##### Parameters

###### decimalPlaces

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toFraction()

> **toFraction**(`max_denominator?`): `Decimal`[]

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:492

#### Parameters

##### max\_denominator?

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`[]

***

### toHex()

#### Call Signature

> **toHex**(`significantDigits?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:496

##### Parameters

###### significantDigits?

`number`

##### Returns

`string`

#### Call Signature

> **toHex**(`significantDigits`, `rounding?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:497

##### Parameters

###### significantDigits

`number`

###### rounding?

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toHexadecimal()

#### Call Signature

> **toHexadecimal**(`significantDigits?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:494

##### Parameters

###### significantDigits?

`number`

##### Returns

`string`

#### Call Signature

> **toHexadecimal**(`significantDigits`, `rounding`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:495

##### Parameters

###### significantDigits

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toJSON()

> **toJSON**(): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:499

#### Returns

`string`

***

### toNearest()

> **toNearest**(`n`, `rounding?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:501

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### rounding?

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

#### Returns

`Decimal`

***

### toNumber()

> **toNumber**(): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:503

#### Returns

`number`

***

### toOctal()

#### Call Signature

> **toOctal**(`significantDigits?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:505

##### Parameters

###### significantDigits?

`number`

##### Returns

`string`

#### Call Signature

> **toOctal**(`significantDigits`, `rounding`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:506

##### Parameters

###### significantDigits

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toPower()

> **toPower**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:508

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### toPrecision()

#### Call Signature

> **toPrecision**(`significantDigits?`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:511

##### Parameters

###### significantDigits?

`number`

##### Returns

`string`

#### Call Signature

> **toPrecision**(`significantDigits`, `rounding`): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:512

##### Parameters

###### significantDigits

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`string`

***

### toSD()

#### Call Signature

> **toSD**(`significantDigits?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:516

##### Parameters

###### significantDigits?

`number`

##### Returns

`Decimal`

#### Call Signature

> **toSD**(`significantDigits`, `rounding`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:517

##### Parameters

###### significantDigits

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`Decimal`

***

### toSignificantDigits()

#### Call Signature

> **toSignificantDigits**(`significantDigits?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:514

##### Parameters

###### significantDigits?

`number`

##### Returns

`Decimal`

#### Call Signature

> **toSignificantDigits**(`significantDigits`, `rounding`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:515

##### Parameters

###### significantDigits

`number`

###### rounding

[`Rounding`](../namespaces/Decimal/type-aliases/Rounding.md)

##### Returns

`Decimal`

***

### toString()

> **toString**(): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:519

#### Returns

`string`

***

### trunc()

> **trunc**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:522

#### Returns

`Decimal`

***

### truncated()

> **truncated**(): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:521

#### Returns

`Decimal`

***

### valueOf()

> **valueOf**(): `string`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:524

#### Returns

`string`

***

### abs()

> `static` **abs**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:526

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### acos()

> `static` **acos**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:527

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### acosh()

> `static` **acosh**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:528

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### add()

> `static` **add**(`x`, `y`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:529

#### Parameters

##### x

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### y

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### asin()

> `static` **asin**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:530

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### asinh()

> `static` **asinh**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:531

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### atan()

> `static` **atan**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:532

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### atan2()

> `static` **atan2**(`y`, `x`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:534

#### Parameters

##### y

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### x

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### atanh()

> `static` **atanh**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:533

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### cbrt()

> `static` **cbrt**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:535

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### ceil()

> `static` **ceil**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:536

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### clamp()

> `static` **clamp**(`n`, `min`, `max`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:537

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### min

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### max

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### clone()

> `static` **clone**(`object?`): *typeof* [`Decimal`](../namespaces/Decimal/README.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:538

#### Parameters

##### object?

[`Config`](../namespaces/Decimal/interfaces/Config.md)

#### Returns

*typeof* [`Decimal`](../namespaces/Decimal/README.md)

***

### config()

> `static` **config**(`object`): *typeof* [`Decimal`](../namespaces/Decimal/README.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:539

#### Parameters

##### object

[`Config`](../namespaces/Decimal/interfaces/Config.md)

#### Returns

*typeof* [`Decimal`](../namespaces/Decimal/README.md)

***

### cos()

> `static` **cos**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:540

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### cosh()

> `static` **cosh**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:541

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### div()

> `static` **div**(`x`, `y`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:542

#### Parameters

##### x

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### y

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### exp()

> `static` **exp**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:543

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### floor()

> `static` **floor**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:544

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### hypot()

> `static` **hypot**(...`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:545

#### Parameters

##### n

...[`Value`](../namespaces/Decimal/type-aliases/Value.md)[]

#### Returns

`Decimal`

***

### isDecimal()

> `static` **isDecimal**(`object`): `object is Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:546

#### Parameters

##### object

`any`

#### Returns

`object is Decimal`

***

### ln()

> `static` **ln**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:547

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### log()

> `static` **log**(`n`, `base?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:548

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### base?

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### log10()

> `static` **log10**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:550

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### log2()

> `static` **log2**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:549

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### max()

> `static` **max**(...`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:551

#### Parameters

##### n

...[`Value`](../namespaces/Decimal/type-aliases/Value.md)[]

#### Returns

`Decimal`

***

### min()

> `static` **min**(...`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:552

#### Parameters

##### n

...[`Value`](../namespaces/Decimal/type-aliases/Value.md)[]

#### Returns

`Decimal`

***

### mod()

> `static` **mod**(`x`, `y`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:553

#### Parameters

##### x

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### y

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### mul()

> `static` **mul**(`x`, `y`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:554

#### Parameters

##### x

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### y

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### noConflict()

> `static` **noConflict**(): *typeof* [`Decimal`](../namespaces/Decimal/README.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:555

#### Returns

*typeof* [`Decimal`](../namespaces/Decimal/README.md)

***

### pow()

> `static` **pow**(`base`, `exponent`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:556

#### Parameters

##### base

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### exponent

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### random()

> `static` **random**(`significantDigits?`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:557

#### Parameters

##### significantDigits?

`number`

#### Returns

`Decimal`

***

### round()

> `static` **round**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:558

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### set()

> `static` **set**(`object`): *typeof* [`Decimal`](../namespaces/Decimal/README.md)

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:559

#### Parameters

##### object

[`Config`](../namespaces/Decimal/interfaces/Config.md)

#### Returns

*typeof* [`Decimal`](../namespaces/Decimal/README.md)

***

### sign()

> `static` **sign**(`n`): `number`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:560

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`number`

***

### sin()

> `static` **sin**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:561

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### sinh()

> `static` **sinh**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:562

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### sqrt()

> `static` **sqrt**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:563

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### sub()

> `static` **sub**(`x`, `y`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:564

#### Parameters

##### x

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

##### y

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### sum()

> `static` **sum**(...`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:565

#### Parameters

##### n

...[`Value`](../namespaces/Decimal/type-aliases/Value.md)[]

#### Returns

`Decimal`

***

### tan()

> `static` **tan**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:566

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### tanh()

> `static` **tanh**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:567

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

***

### trunc()

> `static` **trunc**(`n`): `Decimal`

Defined in: node\_modules/@prisma/client/runtime/library.d.ts:568

#### Parameters

##### n

[`Value`](../namespaces/Decimal/type-aliases/Value.md)

#### Returns

`Decimal`

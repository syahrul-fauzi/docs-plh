[**Lawyers Hub API Reference**](../../../../../README.md)

***

[Lawyers Hub API Reference](../../../../../packages.md) / [@lawyers-hub/database](../../../README.md) / [Prisma](../README.md) / TypeMap

# Type Alias: TypeMap\<ExtArgs, ClientOptions\>

> **TypeMap**\<`ExtArgs`, `ClientOptions`\> = `object` & `object`

Defined in: node\_modules/.prisma/client/index.d.ts:833

## Type Declaration

### meta

> **meta**: `object`

#### meta.modelProps

> **modelProps**: `"tenant"` \| `"subscription"` \| `"user"` \| `"case"` \| `"document"` \| `"draft"` \| `"comment"` \| `"auditLog"` \| `"usage"` \| `"invitation"` \| `"documentTemplate"` \| `"templateVersion"` \| `"aIModelConfig"` \| `"complianceReview"` \| `"pIIAuditLog"`

#### meta.txIsolationLevel

> **txIsolationLevel**: [`TransactionIsolationLevel`](TransactionIsolationLevel.md)

### model

> **model**: `object`

#### model.AIModelConfig

> **AIModelConfig**: `object`

#### model.AIModelConfig.fields

> **fields**: [`AIModelConfigFieldRefs`](../interfaces/AIModelConfigFieldRefs.md)

#### model.AIModelConfig.operations

> **operations**: `object`

#### model.AIModelConfig.operations.aggregate

> **aggregate**: `object`

#### model.AIModelConfig.operations.aggregate.args

> **args**: [`AIModelConfigAggregateArgs`](AIModelConfigAggregateArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateAIModelConfig`](AggregateAIModelConfig.md)\>

#### model.AIModelConfig.operations.count

> **count**: `object`

#### model.AIModelConfig.operations.count.args

> **args**: [`AIModelConfigCountArgs`](AIModelConfigCountArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.count.result

> **result**: `$Utils.Optional`\<[`AIModelConfigCountAggregateOutputType`](AIModelConfigCountAggregateOutputType.md)\> \| `number`

#### model.AIModelConfig.operations.create

> **create**: `object`

#### model.AIModelConfig.operations.create.args

> **args**: [`AIModelConfigCreateArgs`](AIModelConfigCreateArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>

#### model.AIModelConfig.operations.createMany

> **createMany**: `object`

#### model.AIModelConfig.operations.createMany.args

> **args**: [`AIModelConfigCreateManyArgs`](AIModelConfigCreateManyArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.AIModelConfig.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.AIModelConfig.operations.createManyAndReturn.args

> **args**: [`AIModelConfigCreateManyAndReturnArgs`](AIModelConfigCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>[]

#### model.AIModelConfig.operations.delete

> **delete**: `object`

#### model.AIModelConfig.operations.delete.args

> **args**: [`AIModelConfigDeleteArgs`](AIModelConfigDeleteArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>

#### model.AIModelConfig.operations.deleteMany

> **deleteMany**: `object`

#### model.AIModelConfig.operations.deleteMany.args

> **args**: [`AIModelConfigDeleteManyArgs`](AIModelConfigDeleteManyArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.AIModelConfig.operations.findFirst

> **findFirst**: `object`

#### model.AIModelConfig.operations.findFirst.args

> **args**: [`AIModelConfigFindFirstArgs`](AIModelConfigFindFirstArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\> \| `null`

#### model.AIModelConfig.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.AIModelConfig.operations.findFirstOrThrow.args

> **args**: [`AIModelConfigFindFirstOrThrowArgs`](AIModelConfigFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>

#### model.AIModelConfig.operations.findMany

> **findMany**: `object`

#### model.AIModelConfig.operations.findMany.args

> **args**: [`AIModelConfigFindManyArgs`](AIModelConfigFindManyArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>[]

#### model.AIModelConfig.operations.findUnique

> **findUnique**: `object`

#### model.AIModelConfig.operations.findUnique.args

> **args**: [`AIModelConfigFindUniqueArgs`](AIModelConfigFindUniqueArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\> \| `null`

#### model.AIModelConfig.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.AIModelConfig.operations.findUniqueOrThrow.args

> **args**: [`AIModelConfigFindUniqueOrThrowArgs`](AIModelConfigFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>

#### model.AIModelConfig.operations.groupBy

> **groupBy**: `object`

#### model.AIModelConfig.operations.groupBy.args

> **args**: [`AIModelConfigGroupByArgs`](AIModelConfigGroupByArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`AIModelConfigGroupByOutputType`](AIModelConfigGroupByOutputType.md)\>[]

#### model.AIModelConfig.operations.update

> **update**: `object`

#### model.AIModelConfig.operations.update.args

> **args**: [`AIModelConfigUpdateArgs`](AIModelConfigUpdateArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>

#### model.AIModelConfig.operations.updateMany

> **updateMany**: `object`

#### model.AIModelConfig.operations.updateMany.args

> **args**: [`AIModelConfigUpdateManyArgs`](AIModelConfigUpdateManyArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.AIModelConfig.operations.upsert

> **upsert**: `object`

#### model.AIModelConfig.operations.upsert.args

> **args**: [`AIModelConfigUpsertArgs`](AIModelConfigUpsertArgs.md)\<`ExtArgs`\>

#### model.AIModelConfig.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$AIModelConfigPayload`]($AIModelConfigPayload.md)\>

#### model.AIModelConfig.payload

> **payload**: [`$AIModelConfigPayload`]($AIModelConfigPayload.md)\<`ExtArgs`\>

#### model.AuditLog

> **AuditLog**: `object`

#### model.AuditLog.fields

> **fields**: [`AuditLogFieldRefs`](../interfaces/AuditLogFieldRefs.md)

#### model.AuditLog.operations

> **operations**: `object`

#### model.AuditLog.operations.aggregate

> **aggregate**: `object`

#### model.AuditLog.operations.aggregate.args

> **args**: [`AuditLogAggregateArgs`](AuditLogAggregateArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateAuditLog`](AggregateAuditLog.md)\>

#### model.AuditLog.operations.count

> **count**: `object`

#### model.AuditLog.operations.count.args

> **args**: [`AuditLogCountArgs`](AuditLogCountArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.count.result

> **result**: `$Utils.Optional`\<[`AuditLogCountAggregateOutputType`](AuditLogCountAggregateOutputType.md)\> \| `number`

#### model.AuditLog.operations.create

> **create**: `object`

#### model.AuditLog.operations.create.args

> **args**: [`AuditLogCreateArgs`](AuditLogCreateArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>

#### model.AuditLog.operations.createMany

> **createMany**: `object`

#### model.AuditLog.operations.createMany.args

> **args**: [`AuditLogCreateManyArgs`](AuditLogCreateManyArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.AuditLog.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.AuditLog.operations.createManyAndReturn.args

> **args**: [`AuditLogCreateManyAndReturnArgs`](AuditLogCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>[]

#### model.AuditLog.operations.delete

> **delete**: `object`

#### model.AuditLog.operations.delete.args

> **args**: [`AuditLogDeleteArgs`](AuditLogDeleteArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>

#### model.AuditLog.operations.deleteMany

> **deleteMany**: `object`

#### model.AuditLog.operations.deleteMany.args

> **args**: [`AuditLogDeleteManyArgs`](AuditLogDeleteManyArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.AuditLog.operations.findFirst

> **findFirst**: `object`

#### model.AuditLog.operations.findFirst.args

> **args**: [`AuditLogFindFirstArgs`](AuditLogFindFirstArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\> \| `null`

#### model.AuditLog.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.AuditLog.operations.findFirstOrThrow.args

> **args**: [`AuditLogFindFirstOrThrowArgs`](AuditLogFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>

#### model.AuditLog.operations.findMany

> **findMany**: `object`

#### model.AuditLog.operations.findMany.args

> **args**: [`AuditLogFindManyArgs`](AuditLogFindManyArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>[]

#### model.AuditLog.operations.findUnique

> **findUnique**: `object`

#### model.AuditLog.operations.findUnique.args

> **args**: [`AuditLogFindUniqueArgs`](AuditLogFindUniqueArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\> \| `null`

#### model.AuditLog.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.AuditLog.operations.findUniqueOrThrow.args

> **args**: [`AuditLogFindUniqueOrThrowArgs`](AuditLogFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>

#### model.AuditLog.operations.groupBy

> **groupBy**: `object`

#### model.AuditLog.operations.groupBy.args

> **args**: [`AuditLogGroupByArgs`](AuditLogGroupByArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`AuditLogGroupByOutputType`](AuditLogGroupByOutputType.md)\>[]

#### model.AuditLog.operations.update

> **update**: `object`

#### model.AuditLog.operations.update.args

> **args**: [`AuditLogUpdateArgs`](AuditLogUpdateArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>

#### model.AuditLog.operations.updateMany

> **updateMany**: `object`

#### model.AuditLog.operations.updateMany.args

> **args**: [`AuditLogUpdateManyArgs`](AuditLogUpdateManyArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.AuditLog.operations.upsert

> **upsert**: `object`

#### model.AuditLog.operations.upsert.args

> **args**: [`AuditLogUpsertArgs`](AuditLogUpsertArgs.md)\<`ExtArgs`\>

#### model.AuditLog.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$AuditLogPayload`]($AuditLogPayload.md)\>

#### model.AuditLog.payload

> **payload**: [`$AuditLogPayload`]($AuditLogPayload.md)\<`ExtArgs`\>

#### model.Case

> **Case**: `object`

#### model.Case.fields

> **fields**: [`CaseFieldRefs`](../interfaces/CaseFieldRefs.md)

#### model.Case.operations

> **operations**: `object`

#### model.Case.operations.aggregate

> **aggregate**: `object`

#### model.Case.operations.aggregate.args

> **args**: [`CaseAggregateArgs`](CaseAggregateArgs.md)\<`ExtArgs`\>

#### model.Case.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateCase`](AggregateCase.md)\>

#### model.Case.operations.count

> **count**: `object`

#### model.Case.operations.count.args

> **args**: [`CaseCountArgs`](CaseCountArgs.md)\<`ExtArgs`\>

#### model.Case.operations.count.result

> **result**: `$Utils.Optional`\<[`CaseCountAggregateOutputType`](CaseCountAggregateOutputType.md)\> \| `number`

#### model.Case.operations.create

> **create**: `object`

#### model.Case.operations.create.args

> **args**: [`CaseCreateArgs`](CaseCreateArgs.md)\<`ExtArgs`\>

#### model.Case.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>

#### model.Case.operations.createMany

> **createMany**: `object`

#### model.Case.operations.createMany.args

> **args**: [`CaseCreateManyArgs`](CaseCreateManyArgs.md)\<`ExtArgs`\>

#### model.Case.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Case.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Case.operations.createManyAndReturn.args

> **args**: [`CaseCreateManyAndReturnArgs`](CaseCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Case.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>[]

#### model.Case.operations.delete

> **delete**: `object`

#### model.Case.operations.delete.args

> **args**: [`CaseDeleteArgs`](CaseDeleteArgs.md)\<`ExtArgs`\>

#### model.Case.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>

#### model.Case.operations.deleteMany

> **deleteMany**: `object`

#### model.Case.operations.deleteMany.args

> **args**: [`CaseDeleteManyArgs`](CaseDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Case.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Case.operations.findFirst

> **findFirst**: `object`

#### model.Case.operations.findFirst.args

> **args**: [`CaseFindFirstArgs`](CaseFindFirstArgs.md)\<`ExtArgs`\>

#### model.Case.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\> \| `null`

#### model.Case.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Case.operations.findFirstOrThrow.args

> **args**: [`CaseFindFirstOrThrowArgs`](CaseFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Case.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>

#### model.Case.operations.findMany

> **findMany**: `object`

#### model.Case.operations.findMany.args

> **args**: [`CaseFindManyArgs`](CaseFindManyArgs.md)\<`ExtArgs`\>

#### model.Case.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>[]

#### model.Case.operations.findUnique

> **findUnique**: `object`

#### model.Case.operations.findUnique.args

> **args**: [`CaseFindUniqueArgs`](CaseFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Case.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\> \| `null`

#### model.Case.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Case.operations.findUniqueOrThrow.args

> **args**: [`CaseFindUniqueOrThrowArgs`](CaseFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Case.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>

#### model.Case.operations.groupBy

> **groupBy**: `object`

#### model.Case.operations.groupBy.args

> **args**: [`CaseGroupByArgs`](CaseGroupByArgs.md)\<`ExtArgs`\>

#### model.Case.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`CaseGroupByOutputType`](CaseGroupByOutputType.md)\>[]

#### model.Case.operations.update

> **update**: `object`

#### model.Case.operations.update.args

> **args**: [`CaseUpdateArgs`](CaseUpdateArgs.md)\<`ExtArgs`\>

#### model.Case.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>

#### model.Case.operations.updateMany

> **updateMany**: `object`

#### model.Case.operations.updateMany.args

> **args**: [`CaseUpdateManyArgs`](CaseUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Case.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Case.operations.upsert

> **upsert**: `object`

#### model.Case.operations.upsert.args

> **args**: [`CaseUpsertArgs`](CaseUpsertArgs.md)\<`ExtArgs`\>

#### model.Case.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$CasePayload`]($CasePayload.md)\>

#### model.Case.payload

> **payload**: [`$CasePayload`]($CasePayload.md)\<`ExtArgs`\>

#### model.Comment

> **Comment**: `object`

#### model.Comment.fields

> **fields**: [`CommentFieldRefs`](../interfaces/CommentFieldRefs.md)

#### model.Comment.operations

> **operations**: `object`

#### model.Comment.operations.aggregate

> **aggregate**: `object`

#### model.Comment.operations.aggregate.args

> **args**: [`CommentAggregateArgs`](CommentAggregateArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateComment`](AggregateComment.md)\>

#### model.Comment.operations.count

> **count**: `object`

#### model.Comment.operations.count.args

> **args**: [`CommentCountArgs`](CommentCountArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.count.result

> **result**: `$Utils.Optional`\<[`CommentCountAggregateOutputType`](CommentCountAggregateOutputType.md)\> \| `number`

#### model.Comment.operations.create

> **create**: `object`

#### model.Comment.operations.create.args

> **args**: [`CommentCreateArgs`](CommentCreateArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>

#### model.Comment.operations.createMany

> **createMany**: `object`

#### model.Comment.operations.createMany.args

> **args**: [`CommentCreateManyArgs`](CommentCreateManyArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Comment.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Comment.operations.createManyAndReturn.args

> **args**: [`CommentCreateManyAndReturnArgs`](CommentCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>[]

#### model.Comment.operations.delete

> **delete**: `object`

#### model.Comment.operations.delete.args

> **args**: [`CommentDeleteArgs`](CommentDeleteArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>

#### model.Comment.operations.deleteMany

> **deleteMany**: `object`

#### model.Comment.operations.deleteMany.args

> **args**: [`CommentDeleteManyArgs`](CommentDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Comment.operations.findFirst

> **findFirst**: `object`

#### model.Comment.operations.findFirst.args

> **args**: [`CommentFindFirstArgs`](CommentFindFirstArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\> \| `null`

#### model.Comment.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Comment.operations.findFirstOrThrow.args

> **args**: [`CommentFindFirstOrThrowArgs`](CommentFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>

#### model.Comment.operations.findMany

> **findMany**: `object`

#### model.Comment.operations.findMany.args

> **args**: [`CommentFindManyArgs`](CommentFindManyArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>[]

#### model.Comment.operations.findUnique

> **findUnique**: `object`

#### model.Comment.operations.findUnique.args

> **args**: [`CommentFindUniqueArgs`](CommentFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\> \| `null`

#### model.Comment.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Comment.operations.findUniqueOrThrow.args

> **args**: [`CommentFindUniqueOrThrowArgs`](CommentFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>

#### model.Comment.operations.groupBy

> **groupBy**: `object`

#### model.Comment.operations.groupBy.args

> **args**: [`CommentGroupByArgs`](CommentGroupByArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`CommentGroupByOutputType`](CommentGroupByOutputType.md)\>[]

#### model.Comment.operations.update

> **update**: `object`

#### model.Comment.operations.update.args

> **args**: [`CommentUpdateArgs`](CommentUpdateArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>

#### model.Comment.operations.updateMany

> **updateMany**: `object`

#### model.Comment.operations.updateMany.args

> **args**: [`CommentUpdateManyArgs`](CommentUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Comment.operations.upsert

> **upsert**: `object`

#### model.Comment.operations.upsert.args

> **args**: [`CommentUpsertArgs`](CommentUpsertArgs.md)\<`ExtArgs`\>

#### model.Comment.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$CommentPayload`]($CommentPayload.md)\>

#### model.Comment.payload

> **payload**: [`$CommentPayload`]($CommentPayload.md)\<`ExtArgs`\>

#### model.ComplianceReview

> **ComplianceReview**: `object`

#### model.ComplianceReview.fields

> **fields**: [`ComplianceReviewFieldRefs`](../interfaces/ComplianceReviewFieldRefs.md)

#### model.ComplianceReview.operations

> **operations**: `object`

#### model.ComplianceReview.operations.aggregate

> **aggregate**: `object`

#### model.ComplianceReview.operations.aggregate.args

> **args**: [`ComplianceReviewAggregateArgs`](ComplianceReviewAggregateArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateComplianceReview`](AggregateComplianceReview.md)\>

#### model.ComplianceReview.operations.count

> **count**: `object`

#### model.ComplianceReview.operations.count.args

> **args**: [`ComplianceReviewCountArgs`](ComplianceReviewCountArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.count.result

> **result**: `$Utils.Optional`\<[`ComplianceReviewCountAggregateOutputType`](ComplianceReviewCountAggregateOutputType.md)\> \| `number`

#### model.ComplianceReview.operations.create

> **create**: `object`

#### model.ComplianceReview.operations.create.args

> **args**: [`ComplianceReviewCreateArgs`](ComplianceReviewCreateArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>

#### model.ComplianceReview.operations.createMany

> **createMany**: `object`

#### model.ComplianceReview.operations.createMany.args

> **args**: [`ComplianceReviewCreateManyArgs`](ComplianceReviewCreateManyArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.ComplianceReview.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.ComplianceReview.operations.createManyAndReturn.args

> **args**: [`ComplianceReviewCreateManyAndReturnArgs`](ComplianceReviewCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>[]

#### model.ComplianceReview.operations.delete

> **delete**: `object`

#### model.ComplianceReview.operations.delete.args

> **args**: [`ComplianceReviewDeleteArgs`](ComplianceReviewDeleteArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>

#### model.ComplianceReview.operations.deleteMany

> **deleteMany**: `object`

#### model.ComplianceReview.operations.deleteMany.args

> **args**: [`ComplianceReviewDeleteManyArgs`](ComplianceReviewDeleteManyArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.ComplianceReview.operations.findFirst

> **findFirst**: `object`

#### model.ComplianceReview.operations.findFirst.args

> **args**: [`ComplianceReviewFindFirstArgs`](ComplianceReviewFindFirstArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\> \| `null`

#### model.ComplianceReview.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.ComplianceReview.operations.findFirstOrThrow.args

> **args**: [`ComplianceReviewFindFirstOrThrowArgs`](ComplianceReviewFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>

#### model.ComplianceReview.operations.findMany

> **findMany**: `object`

#### model.ComplianceReview.operations.findMany.args

> **args**: [`ComplianceReviewFindManyArgs`](ComplianceReviewFindManyArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>[]

#### model.ComplianceReview.operations.findUnique

> **findUnique**: `object`

#### model.ComplianceReview.operations.findUnique.args

> **args**: [`ComplianceReviewFindUniqueArgs`](ComplianceReviewFindUniqueArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\> \| `null`

#### model.ComplianceReview.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.ComplianceReview.operations.findUniqueOrThrow.args

> **args**: [`ComplianceReviewFindUniqueOrThrowArgs`](ComplianceReviewFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>

#### model.ComplianceReview.operations.groupBy

> **groupBy**: `object`

#### model.ComplianceReview.operations.groupBy.args

> **args**: [`ComplianceReviewGroupByArgs`](ComplianceReviewGroupByArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`ComplianceReviewGroupByOutputType`](ComplianceReviewGroupByOutputType.md)\>[]

#### model.ComplianceReview.operations.update

> **update**: `object`

#### model.ComplianceReview.operations.update.args

> **args**: [`ComplianceReviewUpdateArgs`](ComplianceReviewUpdateArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>

#### model.ComplianceReview.operations.updateMany

> **updateMany**: `object`

#### model.ComplianceReview.operations.updateMany.args

> **args**: [`ComplianceReviewUpdateManyArgs`](ComplianceReviewUpdateManyArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.ComplianceReview.operations.upsert

> **upsert**: `object`

#### model.ComplianceReview.operations.upsert.args

> **args**: [`ComplianceReviewUpsertArgs`](ComplianceReviewUpsertArgs.md)\<`ExtArgs`\>

#### model.ComplianceReview.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\>

#### model.ComplianceReview.payload

> **payload**: [`$ComplianceReviewPayload`]($ComplianceReviewPayload.md)\<`ExtArgs`\>

#### model.Document

> **Document**: `object`

#### model.Document.fields

> **fields**: [`DocumentFieldRefs`](../interfaces/DocumentFieldRefs.md)

#### model.Document.operations

> **operations**: `object`

#### model.Document.operations.aggregate

> **aggregate**: `object`

#### model.Document.operations.aggregate.args

> **args**: [`DocumentAggregateArgs`](DocumentAggregateArgs.md)\<`ExtArgs`\>

#### model.Document.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateDocument`](AggregateDocument.md)\>

#### model.Document.operations.count

> **count**: `object`

#### model.Document.operations.count.args

> **args**: [`DocumentCountArgs`](DocumentCountArgs.md)\<`ExtArgs`\>

#### model.Document.operations.count.result

> **result**: `$Utils.Optional`\<[`DocumentCountAggregateOutputType`](DocumentCountAggregateOutputType.md)\> \| `number`

#### model.Document.operations.create

> **create**: `object`

#### model.Document.operations.create.args

> **args**: [`DocumentCreateArgs`](DocumentCreateArgs.md)\<`ExtArgs`\>

#### model.Document.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>

#### model.Document.operations.createMany

> **createMany**: `object`

#### model.Document.operations.createMany.args

> **args**: [`DocumentCreateManyArgs`](DocumentCreateManyArgs.md)\<`ExtArgs`\>

#### model.Document.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Document.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Document.operations.createManyAndReturn.args

> **args**: [`DocumentCreateManyAndReturnArgs`](DocumentCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Document.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>[]

#### model.Document.operations.delete

> **delete**: `object`

#### model.Document.operations.delete.args

> **args**: [`DocumentDeleteArgs`](DocumentDeleteArgs.md)\<`ExtArgs`\>

#### model.Document.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>

#### model.Document.operations.deleteMany

> **deleteMany**: `object`

#### model.Document.operations.deleteMany.args

> **args**: [`DocumentDeleteManyArgs`](DocumentDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Document.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Document.operations.findFirst

> **findFirst**: `object`

#### model.Document.operations.findFirst.args

> **args**: [`DocumentFindFirstArgs`](DocumentFindFirstArgs.md)\<`ExtArgs`\>

#### model.Document.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\> \| `null`

#### model.Document.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Document.operations.findFirstOrThrow.args

> **args**: [`DocumentFindFirstOrThrowArgs`](DocumentFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Document.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>

#### model.Document.operations.findMany

> **findMany**: `object`

#### model.Document.operations.findMany.args

> **args**: [`DocumentFindManyArgs`](DocumentFindManyArgs.md)\<`ExtArgs`\>

#### model.Document.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>[]

#### model.Document.operations.findUnique

> **findUnique**: `object`

#### model.Document.operations.findUnique.args

> **args**: [`DocumentFindUniqueArgs`](DocumentFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Document.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\> \| `null`

#### model.Document.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Document.operations.findUniqueOrThrow.args

> **args**: [`DocumentFindUniqueOrThrowArgs`](DocumentFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Document.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>

#### model.Document.operations.groupBy

> **groupBy**: `object`

#### model.Document.operations.groupBy.args

> **args**: [`DocumentGroupByArgs`](DocumentGroupByArgs.md)\<`ExtArgs`\>

#### model.Document.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`DocumentGroupByOutputType`](DocumentGroupByOutputType.md)\>[]

#### model.Document.operations.update

> **update**: `object`

#### model.Document.operations.update.args

> **args**: [`DocumentUpdateArgs`](DocumentUpdateArgs.md)\<`ExtArgs`\>

#### model.Document.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>

#### model.Document.operations.updateMany

> **updateMany**: `object`

#### model.Document.operations.updateMany.args

> **args**: [`DocumentUpdateManyArgs`](DocumentUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Document.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Document.operations.upsert

> **upsert**: `object`

#### model.Document.operations.upsert.args

> **args**: [`DocumentUpsertArgs`](DocumentUpsertArgs.md)\<`ExtArgs`\>

#### model.Document.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentPayload`]($DocumentPayload.md)\>

#### model.Document.payload

> **payload**: [`$DocumentPayload`]($DocumentPayload.md)\<`ExtArgs`\>

#### model.DocumentTemplate

> **DocumentTemplate**: `object`

#### model.DocumentTemplate.fields

> **fields**: [`DocumentTemplateFieldRefs`](../interfaces/DocumentTemplateFieldRefs.md)

#### model.DocumentTemplate.operations

> **operations**: `object`

#### model.DocumentTemplate.operations.aggregate

> **aggregate**: `object`

#### model.DocumentTemplate.operations.aggregate.args

> **args**: [`DocumentTemplateAggregateArgs`](DocumentTemplateAggregateArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateDocumentTemplate`](AggregateDocumentTemplate.md)\>

#### model.DocumentTemplate.operations.count

> **count**: `object`

#### model.DocumentTemplate.operations.count.args

> **args**: [`DocumentTemplateCountArgs`](DocumentTemplateCountArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.count.result

> **result**: `$Utils.Optional`\<[`DocumentTemplateCountAggregateOutputType`](DocumentTemplateCountAggregateOutputType.md)\> \| `number`

#### model.DocumentTemplate.operations.create

> **create**: `object`

#### model.DocumentTemplate.operations.create.args

> **args**: [`DocumentTemplateCreateArgs`](DocumentTemplateCreateArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>

#### model.DocumentTemplate.operations.createMany

> **createMany**: `object`

#### model.DocumentTemplate.operations.createMany.args

> **args**: [`DocumentTemplateCreateManyArgs`](DocumentTemplateCreateManyArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.DocumentTemplate.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.DocumentTemplate.operations.createManyAndReturn.args

> **args**: [`DocumentTemplateCreateManyAndReturnArgs`](DocumentTemplateCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>[]

#### model.DocumentTemplate.operations.delete

> **delete**: `object`

#### model.DocumentTemplate.operations.delete.args

> **args**: [`DocumentTemplateDeleteArgs`](DocumentTemplateDeleteArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>

#### model.DocumentTemplate.operations.deleteMany

> **deleteMany**: `object`

#### model.DocumentTemplate.operations.deleteMany.args

> **args**: [`DocumentTemplateDeleteManyArgs`](DocumentTemplateDeleteManyArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.DocumentTemplate.operations.findFirst

> **findFirst**: `object`

#### model.DocumentTemplate.operations.findFirst.args

> **args**: [`DocumentTemplateFindFirstArgs`](DocumentTemplateFindFirstArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\> \| `null`

#### model.DocumentTemplate.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.DocumentTemplate.operations.findFirstOrThrow.args

> **args**: [`DocumentTemplateFindFirstOrThrowArgs`](DocumentTemplateFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>

#### model.DocumentTemplate.operations.findMany

> **findMany**: `object`

#### model.DocumentTemplate.operations.findMany.args

> **args**: [`DocumentTemplateFindManyArgs`](DocumentTemplateFindManyArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>[]

#### model.DocumentTemplate.operations.findUnique

> **findUnique**: `object`

#### model.DocumentTemplate.operations.findUnique.args

> **args**: [`DocumentTemplateFindUniqueArgs`](DocumentTemplateFindUniqueArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\> \| `null`

#### model.DocumentTemplate.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.DocumentTemplate.operations.findUniqueOrThrow.args

> **args**: [`DocumentTemplateFindUniqueOrThrowArgs`](DocumentTemplateFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>

#### model.DocumentTemplate.operations.groupBy

> **groupBy**: `object`

#### model.DocumentTemplate.operations.groupBy.args

> **args**: [`DocumentTemplateGroupByArgs`](DocumentTemplateGroupByArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`DocumentTemplateGroupByOutputType`](DocumentTemplateGroupByOutputType.md)\>[]

#### model.DocumentTemplate.operations.update

> **update**: `object`

#### model.DocumentTemplate.operations.update.args

> **args**: [`DocumentTemplateUpdateArgs`](DocumentTemplateUpdateArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>

#### model.DocumentTemplate.operations.updateMany

> **updateMany**: `object`

#### model.DocumentTemplate.operations.updateMany.args

> **args**: [`DocumentTemplateUpdateManyArgs`](DocumentTemplateUpdateManyArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.DocumentTemplate.operations.upsert

> **upsert**: `object`

#### model.DocumentTemplate.operations.upsert.args

> **args**: [`DocumentTemplateUpsertArgs`](DocumentTemplateUpsertArgs.md)\<`ExtArgs`\>

#### model.DocumentTemplate.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\>

#### model.DocumentTemplate.payload

> **payload**: [`$DocumentTemplatePayload`]($DocumentTemplatePayload.md)\<`ExtArgs`\>

#### model.Draft

> **Draft**: `object`

#### model.Draft.fields

> **fields**: [`DraftFieldRefs`](../interfaces/DraftFieldRefs.md)

#### model.Draft.operations

> **operations**: `object`

#### model.Draft.operations.aggregate

> **aggregate**: `object`

#### model.Draft.operations.aggregate.args

> **args**: [`DraftAggregateArgs`](DraftAggregateArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateDraft`](AggregateDraft.md)\>

#### model.Draft.operations.count

> **count**: `object`

#### model.Draft.operations.count.args

> **args**: [`DraftCountArgs`](DraftCountArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.count.result

> **result**: `$Utils.Optional`\<[`DraftCountAggregateOutputType`](DraftCountAggregateOutputType.md)\> \| `number`

#### model.Draft.operations.create

> **create**: `object`

#### model.Draft.operations.create.args

> **args**: [`DraftCreateArgs`](DraftCreateArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>

#### model.Draft.operations.createMany

> **createMany**: `object`

#### model.Draft.operations.createMany.args

> **args**: [`DraftCreateManyArgs`](DraftCreateManyArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Draft.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Draft.operations.createManyAndReturn.args

> **args**: [`DraftCreateManyAndReturnArgs`](DraftCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>[]

#### model.Draft.operations.delete

> **delete**: `object`

#### model.Draft.operations.delete.args

> **args**: [`DraftDeleteArgs`](DraftDeleteArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>

#### model.Draft.operations.deleteMany

> **deleteMany**: `object`

#### model.Draft.operations.deleteMany.args

> **args**: [`DraftDeleteManyArgs`](DraftDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Draft.operations.findFirst

> **findFirst**: `object`

#### model.Draft.operations.findFirst.args

> **args**: [`DraftFindFirstArgs`](DraftFindFirstArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\> \| `null`

#### model.Draft.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Draft.operations.findFirstOrThrow.args

> **args**: [`DraftFindFirstOrThrowArgs`](DraftFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>

#### model.Draft.operations.findMany

> **findMany**: `object`

#### model.Draft.operations.findMany.args

> **args**: [`DraftFindManyArgs`](DraftFindManyArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>[]

#### model.Draft.operations.findUnique

> **findUnique**: `object`

#### model.Draft.operations.findUnique.args

> **args**: [`DraftFindUniqueArgs`](DraftFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\> \| `null`

#### model.Draft.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Draft.operations.findUniqueOrThrow.args

> **args**: [`DraftFindUniqueOrThrowArgs`](DraftFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>

#### model.Draft.operations.groupBy

> **groupBy**: `object`

#### model.Draft.operations.groupBy.args

> **args**: [`DraftGroupByArgs`](DraftGroupByArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`DraftGroupByOutputType`](DraftGroupByOutputType.md)\>[]

#### model.Draft.operations.update

> **update**: `object`

#### model.Draft.operations.update.args

> **args**: [`DraftUpdateArgs`](DraftUpdateArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>

#### model.Draft.operations.updateMany

> **updateMany**: `object`

#### model.Draft.operations.updateMany.args

> **args**: [`DraftUpdateManyArgs`](DraftUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Draft.operations.upsert

> **upsert**: `object`

#### model.Draft.operations.upsert.args

> **args**: [`DraftUpsertArgs`](DraftUpsertArgs.md)\<`ExtArgs`\>

#### model.Draft.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$DraftPayload`]($DraftPayload.md)\>

#### model.Draft.payload

> **payload**: [`$DraftPayload`]($DraftPayload.md)\<`ExtArgs`\>

#### model.Invitation

> **Invitation**: `object`

#### model.Invitation.fields

> **fields**: [`InvitationFieldRefs`](../interfaces/InvitationFieldRefs.md)

#### model.Invitation.operations

> **operations**: `object`

#### model.Invitation.operations.aggregate

> **aggregate**: `object`

#### model.Invitation.operations.aggregate.args

> **args**: [`InvitationAggregateArgs`](InvitationAggregateArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateInvitation`](AggregateInvitation.md)\>

#### model.Invitation.operations.count

> **count**: `object`

#### model.Invitation.operations.count.args

> **args**: [`InvitationCountArgs`](InvitationCountArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.count.result

> **result**: `$Utils.Optional`\<[`InvitationCountAggregateOutputType`](InvitationCountAggregateOutputType.md)\> \| `number`

#### model.Invitation.operations.create

> **create**: `object`

#### model.Invitation.operations.create.args

> **args**: [`InvitationCreateArgs`](InvitationCreateArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>

#### model.Invitation.operations.createMany

> **createMany**: `object`

#### model.Invitation.operations.createMany.args

> **args**: [`InvitationCreateManyArgs`](InvitationCreateManyArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Invitation.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Invitation.operations.createManyAndReturn.args

> **args**: [`InvitationCreateManyAndReturnArgs`](InvitationCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>[]

#### model.Invitation.operations.delete

> **delete**: `object`

#### model.Invitation.operations.delete.args

> **args**: [`InvitationDeleteArgs`](InvitationDeleteArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>

#### model.Invitation.operations.deleteMany

> **deleteMany**: `object`

#### model.Invitation.operations.deleteMany.args

> **args**: [`InvitationDeleteManyArgs`](InvitationDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Invitation.operations.findFirst

> **findFirst**: `object`

#### model.Invitation.operations.findFirst.args

> **args**: [`InvitationFindFirstArgs`](InvitationFindFirstArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\> \| `null`

#### model.Invitation.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Invitation.operations.findFirstOrThrow.args

> **args**: [`InvitationFindFirstOrThrowArgs`](InvitationFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>

#### model.Invitation.operations.findMany

> **findMany**: `object`

#### model.Invitation.operations.findMany.args

> **args**: [`InvitationFindManyArgs`](InvitationFindManyArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>[]

#### model.Invitation.operations.findUnique

> **findUnique**: `object`

#### model.Invitation.operations.findUnique.args

> **args**: [`InvitationFindUniqueArgs`](InvitationFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\> \| `null`

#### model.Invitation.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Invitation.operations.findUniqueOrThrow.args

> **args**: [`InvitationFindUniqueOrThrowArgs`](InvitationFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>

#### model.Invitation.operations.groupBy

> **groupBy**: `object`

#### model.Invitation.operations.groupBy.args

> **args**: [`InvitationGroupByArgs`](InvitationGroupByArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`InvitationGroupByOutputType`](InvitationGroupByOutputType.md)\>[]

#### model.Invitation.operations.update

> **update**: `object`

#### model.Invitation.operations.update.args

> **args**: [`InvitationUpdateArgs`](InvitationUpdateArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>

#### model.Invitation.operations.updateMany

> **updateMany**: `object`

#### model.Invitation.operations.updateMany.args

> **args**: [`InvitationUpdateManyArgs`](InvitationUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Invitation.operations.upsert

> **upsert**: `object`

#### model.Invitation.operations.upsert.args

> **args**: [`InvitationUpsertArgs`](InvitationUpsertArgs.md)\<`ExtArgs`\>

#### model.Invitation.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$InvitationPayload`]($InvitationPayload.md)\>

#### model.Invitation.payload

> **payload**: [`$InvitationPayload`]($InvitationPayload.md)\<`ExtArgs`\>

#### model.PIIAuditLog

> **PIIAuditLog**: `object`

#### model.PIIAuditLog.fields

> **fields**: [`PIIAuditLogFieldRefs`](../interfaces/PIIAuditLogFieldRefs.md)

#### model.PIIAuditLog.operations

> **operations**: `object`

#### model.PIIAuditLog.operations.aggregate

> **aggregate**: `object`

#### model.PIIAuditLog.operations.aggregate.args

> **args**: [`PIIAuditLogAggregateArgs`](PIIAuditLogAggregateArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregatePIIAuditLog`](AggregatePIIAuditLog.md)\>

#### model.PIIAuditLog.operations.count

> **count**: `object`

#### model.PIIAuditLog.operations.count.args

> **args**: [`PIIAuditLogCountArgs`](PIIAuditLogCountArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.count.result

> **result**: `$Utils.Optional`\<[`PIIAuditLogCountAggregateOutputType`](PIIAuditLogCountAggregateOutputType.md)\> \| `number`

#### model.PIIAuditLog.operations.create

> **create**: `object`

#### model.PIIAuditLog.operations.create.args

> **args**: [`PIIAuditLogCreateArgs`](PIIAuditLogCreateArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>

#### model.PIIAuditLog.operations.createMany

> **createMany**: `object`

#### model.PIIAuditLog.operations.createMany.args

> **args**: [`PIIAuditLogCreateManyArgs`](PIIAuditLogCreateManyArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.PIIAuditLog.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.PIIAuditLog.operations.createManyAndReturn.args

> **args**: [`PIIAuditLogCreateManyAndReturnArgs`](PIIAuditLogCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>[]

#### model.PIIAuditLog.operations.delete

> **delete**: `object`

#### model.PIIAuditLog.operations.delete.args

> **args**: [`PIIAuditLogDeleteArgs`](PIIAuditLogDeleteArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>

#### model.PIIAuditLog.operations.deleteMany

> **deleteMany**: `object`

#### model.PIIAuditLog.operations.deleteMany.args

> **args**: [`PIIAuditLogDeleteManyArgs`](PIIAuditLogDeleteManyArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.PIIAuditLog.operations.findFirst

> **findFirst**: `object`

#### model.PIIAuditLog.operations.findFirst.args

> **args**: [`PIIAuditLogFindFirstArgs`](PIIAuditLogFindFirstArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\> \| `null`

#### model.PIIAuditLog.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.PIIAuditLog.operations.findFirstOrThrow.args

> **args**: [`PIIAuditLogFindFirstOrThrowArgs`](PIIAuditLogFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>

#### model.PIIAuditLog.operations.findMany

> **findMany**: `object`

#### model.PIIAuditLog.operations.findMany.args

> **args**: [`PIIAuditLogFindManyArgs`](PIIAuditLogFindManyArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>[]

#### model.PIIAuditLog.operations.findUnique

> **findUnique**: `object`

#### model.PIIAuditLog.operations.findUnique.args

> **args**: [`PIIAuditLogFindUniqueArgs`](PIIAuditLogFindUniqueArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\> \| `null`

#### model.PIIAuditLog.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.PIIAuditLog.operations.findUniqueOrThrow.args

> **args**: [`PIIAuditLogFindUniqueOrThrowArgs`](PIIAuditLogFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>

#### model.PIIAuditLog.operations.groupBy

> **groupBy**: `object`

#### model.PIIAuditLog.operations.groupBy.args

> **args**: [`PIIAuditLogGroupByArgs`](PIIAuditLogGroupByArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`PIIAuditLogGroupByOutputType`](PIIAuditLogGroupByOutputType.md)\>[]

#### model.PIIAuditLog.operations.update

> **update**: `object`

#### model.PIIAuditLog.operations.update.args

> **args**: [`PIIAuditLogUpdateArgs`](PIIAuditLogUpdateArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>

#### model.PIIAuditLog.operations.updateMany

> **updateMany**: `object`

#### model.PIIAuditLog.operations.updateMany.args

> **args**: [`PIIAuditLogUpdateManyArgs`](PIIAuditLogUpdateManyArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.PIIAuditLog.operations.upsert

> **upsert**: `object`

#### model.PIIAuditLog.operations.upsert.args

> **args**: [`PIIAuditLogUpsertArgs`](PIIAuditLogUpsertArgs.md)\<`ExtArgs`\>

#### model.PIIAuditLog.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\>

#### model.PIIAuditLog.payload

> **payload**: [`$PIIAuditLogPayload`]($PIIAuditLogPayload.md)\<`ExtArgs`\>

#### model.Subscription

> **Subscription**: `object`

#### model.Subscription.fields

> **fields**: [`SubscriptionFieldRefs`](../interfaces/SubscriptionFieldRefs.md)

#### model.Subscription.operations

> **operations**: `object`

#### model.Subscription.operations.aggregate

> **aggregate**: `object`

#### model.Subscription.operations.aggregate.args

> **args**: [`SubscriptionAggregateArgs`](SubscriptionAggregateArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateSubscription`](AggregateSubscription.md)\>

#### model.Subscription.operations.count

> **count**: `object`

#### model.Subscription.operations.count.args

> **args**: [`SubscriptionCountArgs`](SubscriptionCountArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.count.result

> **result**: `$Utils.Optional`\<[`SubscriptionCountAggregateOutputType`](SubscriptionCountAggregateOutputType.md)\> \| `number`

#### model.Subscription.operations.create

> **create**: `object`

#### model.Subscription.operations.create.args

> **args**: [`SubscriptionCreateArgs`](SubscriptionCreateArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>

#### model.Subscription.operations.createMany

> **createMany**: `object`

#### model.Subscription.operations.createMany.args

> **args**: [`SubscriptionCreateManyArgs`](SubscriptionCreateManyArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Subscription.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Subscription.operations.createManyAndReturn.args

> **args**: [`SubscriptionCreateManyAndReturnArgs`](SubscriptionCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>[]

#### model.Subscription.operations.delete

> **delete**: `object`

#### model.Subscription.operations.delete.args

> **args**: [`SubscriptionDeleteArgs`](SubscriptionDeleteArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>

#### model.Subscription.operations.deleteMany

> **deleteMany**: `object`

#### model.Subscription.operations.deleteMany.args

> **args**: [`SubscriptionDeleteManyArgs`](SubscriptionDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Subscription.operations.findFirst

> **findFirst**: `object`

#### model.Subscription.operations.findFirst.args

> **args**: [`SubscriptionFindFirstArgs`](SubscriptionFindFirstArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\> \| `null`

#### model.Subscription.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Subscription.operations.findFirstOrThrow.args

> **args**: [`SubscriptionFindFirstOrThrowArgs`](SubscriptionFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>

#### model.Subscription.operations.findMany

> **findMany**: `object`

#### model.Subscription.operations.findMany.args

> **args**: [`SubscriptionFindManyArgs`](SubscriptionFindManyArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>[]

#### model.Subscription.operations.findUnique

> **findUnique**: `object`

#### model.Subscription.operations.findUnique.args

> **args**: [`SubscriptionFindUniqueArgs`](SubscriptionFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\> \| `null`

#### model.Subscription.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Subscription.operations.findUniqueOrThrow.args

> **args**: [`SubscriptionFindUniqueOrThrowArgs`](SubscriptionFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>

#### model.Subscription.operations.groupBy

> **groupBy**: `object`

#### model.Subscription.operations.groupBy.args

> **args**: [`SubscriptionGroupByArgs`](SubscriptionGroupByArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`SubscriptionGroupByOutputType`](SubscriptionGroupByOutputType.md)\>[]

#### model.Subscription.operations.update

> **update**: `object`

#### model.Subscription.operations.update.args

> **args**: [`SubscriptionUpdateArgs`](SubscriptionUpdateArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>

#### model.Subscription.operations.updateMany

> **updateMany**: `object`

#### model.Subscription.operations.updateMany.args

> **args**: [`SubscriptionUpdateManyArgs`](SubscriptionUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Subscription.operations.upsert

> **upsert**: `object`

#### model.Subscription.operations.upsert.args

> **args**: [`SubscriptionUpsertArgs`](SubscriptionUpsertArgs.md)\<`ExtArgs`\>

#### model.Subscription.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$SubscriptionPayload`]($SubscriptionPayload.md)\>

#### model.Subscription.payload

> **payload**: [`$SubscriptionPayload`]($SubscriptionPayload.md)\<`ExtArgs`\>

#### model.TemplateVersion

> **TemplateVersion**: `object`

#### model.TemplateVersion.fields

> **fields**: [`TemplateVersionFieldRefs`](../interfaces/TemplateVersionFieldRefs.md)

#### model.TemplateVersion.operations

> **operations**: `object`

#### model.TemplateVersion.operations.aggregate

> **aggregate**: `object`

#### model.TemplateVersion.operations.aggregate.args

> **args**: [`TemplateVersionAggregateArgs`](TemplateVersionAggregateArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateTemplateVersion`](AggregateTemplateVersion.md)\>

#### model.TemplateVersion.operations.count

> **count**: `object`

#### model.TemplateVersion.operations.count.args

> **args**: [`TemplateVersionCountArgs`](TemplateVersionCountArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.count.result

> **result**: `$Utils.Optional`\<[`TemplateVersionCountAggregateOutputType`](TemplateVersionCountAggregateOutputType.md)\> \| `number`

#### model.TemplateVersion.operations.create

> **create**: `object`

#### model.TemplateVersion.operations.create.args

> **args**: [`TemplateVersionCreateArgs`](TemplateVersionCreateArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>

#### model.TemplateVersion.operations.createMany

> **createMany**: `object`

#### model.TemplateVersion.operations.createMany.args

> **args**: [`TemplateVersionCreateManyArgs`](TemplateVersionCreateManyArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.TemplateVersion.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.TemplateVersion.operations.createManyAndReturn.args

> **args**: [`TemplateVersionCreateManyAndReturnArgs`](TemplateVersionCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>[]

#### model.TemplateVersion.operations.delete

> **delete**: `object`

#### model.TemplateVersion.operations.delete.args

> **args**: [`TemplateVersionDeleteArgs`](TemplateVersionDeleteArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>

#### model.TemplateVersion.operations.deleteMany

> **deleteMany**: `object`

#### model.TemplateVersion.operations.deleteMany.args

> **args**: [`TemplateVersionDeleteManyArgs`](TemplateVersionDeleteManyArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.TemplateVersion.operations.findFirst

> **findFirst**: `object`

#### model.TemplateVersion.operations.findFirst.args

> **args**: [`TemplateVersionFindFirstArgs`](TemplateVersionFindFirstArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\> \| `null`

#### model.TemplateVersion.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.TemplateVersion.operations.findFirstOrThrow.args

> **args**: [`TemplateVersionFindFirstOrThrowArgs`](TemplateVersionFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>

#### model.TemplateVersion.operations.findMany

> **findMany**: `object`

#### model.TemplateVersion.operations.findMany.args

> **args**: [`TemplateVersionFindManyArgs`](TemplateVersionFindManyArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>[]

#### model.TemplateVersion.operations.findUnique

> **findUnique**: `object`

#### model.TemplateVersion.operations.findUnique.args

> **args**: [`TemplateVersionFindUniqueArgs`](TemplateVersionFindUniqueArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\> \| `null`

#### model.TemplateVersion.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.TemplateVersion.operations.findUniqueOrThrow.args

> **args**: [`TemplateVersionFindUniqueOrThrowArgs`](TemplateVersionFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>

#### model.TemplateVersion.operations.groupBy

> **groupBy**: `object`

#### model.TemplateVersion.operations.groupBy.args

> **args**: [`TemplateVersionGroupByArgs`](TemplateVersionGroupByArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`TemplateVersionGroupByOutputType`](TemplateVersionGroupByOutputType.md)\>[]

#### model.TemplateVersion.operations.update

> **update**: `object`

#### model.TemplateVersion.operations.update.args

> **args**: [`TemplateVersionUpdateArgs`](TemplateVersionUpdateArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>

#### model.TemplateVersion.operations.updateMany

> **updateMany**: `object`

#### model.TemplateVersion.operations.updateMany.args

> **args**: [`TemplateVersionUpdateManyArgs`](TemplateVersionUpdateManyArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.TemplateVersion.operations.upsert

> **upsert**: `object`

#### model.TemplateVersion.operations.upsert.args

> **args**: [`TemplateVersionUpsertArgs`](TemplateVersionUpsertArgs.md)\<`ExtArgs`\>

#### model.TemplateVersion.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$TemplateVersionPayload`]($TemplateVersionPayload.md)\>

#### model.TemplateVersion.payload

> **payload**: [`$TemplateVersionPayload`]($TemplateVersionPayload.md)\<`ExtArgs`\>

#### model.Tenant

> **Tenant**: `object`

#### model.Tenant.fields

> **fields**: [`TenantFieldRefs`](../interfaces/TenantFieldRefs.md)

#### model.Tenant.operations

> **operations**: `object`

#### model.Tenant.operations.aggregate

> **aggregate**: `object`

#### model.Tenant.operations.aggregate.args

> **args**: [`TenantAggregateArgs`](TenantAggregateArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateTenant`](AggregateTenant.md)\>

#### model.Tenant.operations.count

> **count**: `object`

#### model.Tenant.operations.count.args

> **args**: [`TenantCountArgs`](TenantCountArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.count.result

> **result**: `$Utils.Optional`\<[`TenantCountAggregateOutputType`](TenantCountAggregateOutputType.md)\> \| `number`

#### model.Tenant.operations.create

> **create**: `object`

#### model.Tenant.operations.create.args

> **args**: [`TenantCreateArgs`](TenantCreateArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>

#### model.Tenant.operations.createMany

> **createMany**: `object`

#### model.Tenant.operations.createMany.args

> **args**: [`TenantCreateManyArgs`](TenantCreateManyArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Tenant.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Tenant.operations.createManyAndReturn.args

> **args**: [`TenantCreateManyAndReturnArgs`](TenantCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>[]

#### model.Tenant.operations.delete

> **delete**: `object`

#### model.Tenant.operations.delete.args

> **args**: [`TenantDeleteArgs`](TenantDeleteArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>

#### model.Tenant.operations.deleteMany

> **deleteMany**: `object`

#### model.Tenant.operations.deleteMany.args

> **args**: [`TenantDeleteManyArgs`](TenantDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Tenant.operations.findFirst

> **findFirst**: `object`

#### model.Tenant.operations.findFirst.args

> **args**: [`TenantFindFirstArgs`](TenantFindFirstArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\> \| `null`

#### model.Tenant.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Tenant.operations.findFirstOrThrow.args

> **args**: [`TenantFindFirstOrThrowArgs`](TenantFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>

#### model.Tenant.operations.findMany

> **findMany**: `object`

#### model.Tenant.operations.findMany.args

> **args**: [`TenantFindManyArgs`](TenantFindManyArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>[]

#### model.Tenant.operations.findUnique

> **findUnique**: `object`

#### model.Tenant.operations.findUnique.args

> **args**: [`TenantFindUniqueArgs`](TenantFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\> \| `null`

#### model.Tenant.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Tenant.operations.findUniqueOrThrow.args

> **args**: [`TenantFindUniqueOrThrowArgs`](TenantFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>

#### model.Tenant.operations.groupBy

> **groupBy**: `object`

#### model.Tenant.operations.groupBy.args

> **args**: [`TenantGroupByArgs`](TenantGroupByArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`TenantGroupByOutputType`](TenantGroupByOutputType.md)\>[]

#### model.Tenant.operations.update

> **update**: `object`

#### model.Tenant.operations.update.args

> **args**: [`TenantUpdateArgs`](TenantUpdateArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>

#### model.Tenant.operations.updateMany

> **updateMany**: `object`

#### model.Tenant.operations.updateMany.args

> **args**: [`TenantUpdateManyArgs`](TenantUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Tenant.operations.upsert

> **upsert**: `object`

#### model.Tenant.operations.upsert.args

> **args**: [`TenantUpsertArgs`](TenantUpsertArgs.md)\<`ExtArgs`\>

#### model.Tenant.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$TenantPayload`]($TenantPayload.md)\>

#### model.Tenant.payload

> **payload**: [`$TenantPayload`]($TenantPayload.md)\<`ExtArgs`\>

#### model.Usage

> **Usage**: `object`

#### model.Usage.fields

> **fields**: [`UsageFieldRefs`](../interfaces/UsageFieldRefs.md)

#### model.Usage.operations

> **operations**: `object`

#### model.Usage.operations.aggregate

> **aggregate**: `object`

#### model.Usage.operations.aggregate.args

> **args**: [`UsageAggregateArgs`](UsageAggregateArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateUsage`](AggregateUsage.md)\>

#### model.Usage.operations.count

> **count**: `object`

#### model.Usage.operations.count.args

> **args**: [`UsageCountArgs`](UsageCountArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.count.result

> **result**: `$Utils.Optional`\<[`UsageCountAggregateOutputType`](UsageCountAggregateOutputType.md)\> \| `number`

#### model.Usage.operations.create

> **create**: `object`

#### model.Usage.operations.create.args

> **args**: [`UsageCreateArgs`](UsageCreateArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>

#### model.Usage.operations.createMany

> **createMany**: `object`

#### model.Usage.operations.createMany.args

> **args**: [`UsageCreateManyArgs`](UsageCreateManyArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Usage.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.Usage.operations.createManyAndReturn.args

> **args**: [`UsageCreateManyAndReturnArgs`](UsageCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>[]

#### model.Usage.operations.delete

> **delete**: `object`

#### model.Usage.operations.delete.args

> **args**: [`UsageDeleteArgs`](UsageDeleteArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>

#### model.Usage.operations.deleteMany

> **deleteMany**: `object`

#### model.Usage.operations.deleteMany.args

> **args**: [`UsageDeleteManyArgs`](UsageDeleteManyArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Usage.operations.findFirst

> **findFirst**: `object`

#### model.Usage.operations.findFirst.args

> **args**: [`UsageFindFirstArgs`](UsageFindFirstArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\> \| `null`

#### model.Usage.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.Usage.operations.findFirstOrThrow.args

> **args**: [`UsageFindFirstOrThrowArgs`](UsageFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>

#### model.Usage.operations.findMany

> **findMany**: `object`

#### model.Usage.operations.findMany.args

> **args**: [`UsageFindManyArgs`](UsageFindManyArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>[]

#### model.Usage.operations.findUnique

> **findUnique**: `object`

#### model.Usage.operations.findUnique.args

> **args**: [`UsageFindUniqueArgs`](UsageFindUniqueArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\> \| `null`

#### model.Usage.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.Usage.operations.findUniqueOrThrow.args

> **args**: [`UsageFindUniqueOrThrowArgs`](UsageFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>

#### model.Usage.operations.groupBy

> **groupBy**: `object`

#### model.Usage.operations.groupBy.args

> **args**: [`UsageGroupByArgs`](UsageGroupByArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`UsageGroupByOutputType`](UsageGroupByOutputType.md)\>[]

#### model.Usage.operations.update

> **update**: `object`

#### model.Usage.operations.update.args

> **args**: [`UsageUpdateArgs`](UsageUpdateArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>

#### model.Usage.operations.updateMany

> **updateMany**: `object`

#### model.Usage.operations.updateMany.args

> **args**: [`UsageUpdateManyArgs`](UsageUpdateManyArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.Usage.operations.upsert

> **upsert**: `object`

#### model.Usage.operations.upsert.args

> **args**: [`UsageUpsertArgs`](UsageUpsertArgs.md)\<`ExtArgs`\>

#### model.Usage.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$UsagePayload`]($UsagePayload.md)\>

#### model.Usage.payload

> **payload**: [`$UsagePayload`]($UsagePayload.md)\<`ExtArgs`\>

#### model.User

> **User**: `object`

#### model.User.fields

> **fields**: [`UserFieldRefs`](../interfaces/UserFieldRefs.md)

#### model.User.operations

> **operations**: `object`

#### model.User.operations.aggregate

> **aggregate**: `object`

#### model.User.operations.aggregate.args

> **args**: [`UserAggregateArgs`](UserAggregateArgs.md)\<`ExtArgs`\>

#### model.User.operations.aggregate.result

> **result**: `$Utils.Optional`\<[`AggregateUser`](AggregateUser.md)\>

#### model.User.operations.count

> **count**: `object`

#### model.User.operations.count.args

> **args**: [`UserCountArgs`](UserCountArgs.md)\<`ExtArgs`\>

#### model.User.operations.count.result

> **result**: `$Utils.Optional`\<[`UserCountAggregateOutputType`](UserCountAggregateOutputType.md)\> \| `number`

#### model.User.operations.create

> **create**: `object`

#### model.User.operations.create.args

> **args**: [`UserCreateArgs`](UserCreateArgs.md)\<`ExtArgs`\>

#### model.User.operations.create.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>

#### model.User.operations.createMany

> **createMany**: `object`

#### model.User.operations.createMany.args

> **args**: [`UserCreateManyArgs`](UserCreateManyArgs.md)\<`ExtArgs`\>

#### model.User.operations.createMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.User.operations.createManyAndReturn

> **createManyAndReturn**: `object`

#### model.User.operations.createManyAndReturn.args

> **args**: [`UserCreateManyAndReturnArgs`](UserCreateManyAndReturnArgs.md)\<`ExtArgs`\>

#### model.User.operations.createManyAndReturn.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>[]

#### model.User.operations.delete

> **delete**: `object`

#### model.User.operations.delete.args

> **args**: [`UserDeleteArgs`](UserDeleteArgs.md)\<`ExtArgs`\>

#### model.User.operations.delete.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>

#### model.User.operations.deleteMany

> **deleteMany**: `object`

#### model.User.operations.deleteMany.args

> **args**: [`UserDeleteManyArgs`](UserDeleteManyArgs.md)\<`ExtArgs`\>

#### model.User.operations.deleteMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.User.operations.findFirst

> **findFirst**: `object`

#### model.User.operations.findFirst.args

> **args**: [`UserFindFirstArgs`](UserFindFirstArgs.md)\<`ExtArgs`\>

#### model.User.operations.findFirst.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\> \| `null`

#### model.User.operations.findFirstOrThrow

> **findFirstOrThrow**: `object`

#### model.User.operations.findFirstOrThrow.args

> **args**: [`UserFindFirstOrThrowArgs`](UserFindFirstOrThrowArgs.md)\<`ExtArgs`\>

#### model.User.operations.findFirstOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>

#### model.User.operations.findMany

> **findMany**: `object`

#### model.User.operations.findMany.args

> **args**: [`UserFindManyArgs`](UserFindManyArgs.md)\<`ExtArgs`\>

#### model.User.operations.findMany.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>[]

#### model.User.operations.findUnique

> **findUnique**: `object`

#### model.User.operations.findUnique.args

> **args**: [`UserFindUniqueArgs`](UserFindUniqueArgs.md)\<`ExtArgs`\>

#### model.User.operations.findUnique.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\> \| `null`

#### model.User.operations.findUniqueOrThrow

> **findUniqueOrThrow**: `object`

#### model.User.operations.findUniqueOrThrow.args

> **args**: [`UserFindUniqueOrThrowArgs`](UserFindUniqueOrThrowArgs.md)\<`ExtArgs`\>

#### model.User.operations.findUniqueOrThrow.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>

#### model.User.operations.groupBy

> **groupBy**: `object`

#### model.User.operations.groupBy.args

> **args**: [`UserGroupByArgs`](UserGroupByArgs.md)\<`ExtArgs`\>

#### model.User.operations.groupBy.result

> **result**: `$Utils.Optional`\<[`UserGroupByOutputType`](UserGroupByOutputType.md)\>[]

#### model.User.operations.update

> **update**: `object`

#### model.User.operations.update.args

> **args**: [`UserUpdateArgs`](UserUpdateArgs.md)\<`ExtArgs`\>

#### model.User.operations.update.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>

#### model.User.operations.updateMany

> **updateMany**: `object`

#### model.User.operations.updateMany.args

> **args**: [`UserUpdateManyArgs`](UserUpdateManyArgs.md)\<`ExtArgs`\>

#### model.User.operations.updateMany.result

> **result**: [`BatchPayload`](BatchPayload.md)

#### model.User.operations.upsert

> **upsert**: `object`

#### model.User.operations.upsert.args

> **args**: [`UserUpsertArgs`](UserUpsertArgs.md)\<`ExtArgs`\>

#### model.User.operations.upsert.result

> **result**: `$Utils.PayloadToResult`\<[`$UserPayload`]($UserPayload.md)\>

#### model.User.payload

> **payload**: [`$UserPayload`]($UserPayload.md)\<`ExtArgs`\>

## Type Declaration

### other

> **other**: `object`

#### other.operations

> **operations**: `object`

#### other.operations.$executeRaw

> **$executeRaw**: `object`

#### other.operations.$executeRaw.args

> **args**: \[`TemplateStringsArray` \| [`Sql`](../classes/Sql.md), `any`[]\]

#### other.operations.$executeRaw.result

> **result**: `any`

#### other.operations.$executeRawUnsafe

> **$executeRawUnsafe**: `object`

#### other.operations.$executeRawUnsafe.args

> **args**: \[`string`, `any`[]\]

#### other.operations.$executeRawUnsafe.result

> **result**: `any`

#### other.operations.$queryRaw

> **$queryRaw**: `object`

#### other.operations.$queryRaw.args

> **args**: \[`TemplateStringsArray` \| [`Sql`](../classes/Sql.md), `any`[]\]

#### other.operations.$queryRaw.result

> **result**: `any`

#### other.operations.$queryRawUnsafe

> **$queryRawUnsafe**: `object`

#### other.operations.$queryRawUnsafe.args

> **args**: \[`string`, `any`[]\]

#### other.operations.$queryRawUnsafe.result

> **result**: `any`

#### other.payload

> **payload**: `any`

## Type Parameters

### ExtArgs

`ExtArgs` *extends* `$Extensions.InternalArgs` = `$Extensions.DefaultArgs`

### ClientOptions

`ClientOptions` = \{ \}

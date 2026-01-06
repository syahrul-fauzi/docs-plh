# Workshop: Modern Documentation for Engineering Team

Lawyers Hub — Technical Excellence through Documentation

## 1. Agenda

- **09:00 - 09:15**: Introduction to the 9-Pillar Documentation Structure.
- **09:15 - 09:45**: Engineering Workflow: From Code to Docs.
- **09:45 - 10:15**: Hands-on: Using Templates and Linter.
- **10:15 - 10:30**: Q&A and Feedback.

## 2. The New 9-Pillar Structure

Why the change? To eliminate fragmentation and ensure single-source-of-truth.

1. `00_foundation`: Core strategy, blueprint, and style guide.
2. `01_architecture`: System design, API maps, database schemas.
3. `02_business_logic`: Business rules, legal engine logic.
4. `03_product_features`: PRDs, User Stories, UAT.
5. `04_user_experience`: UI/UX designs, flowcharts.
6. `05_delivery_and_ops`: Project plans, deployment checklists.
7. `06_engineering_execution`: Coding standards, CI/CD, Dev guides.
8. `07_compliance_and_audit`: PDP/GDPR compliance, security audits.
9. `08_archives`: Legacy docs and historical reports.

## 3. Toolchain Integration

Documentation is now part of the definition of "Done".

- **Git Flow**: All docs must be in Markdown.
- **CI/CD**: Every PR triggers `markdownlint` and `link-checker`.
- **Auto-Gen**: API docs are generated from TypeScript decorators.

## 4. Best Practices

- **Atomic Docs**: One concept per file.
- **Visual First**: Use Mermaid.js for diagrams (easier to version control).
- **Linking**: Always use relative paths for internal references.

## 5. Resources

- [Style Guide](../00_foundation/STYLE_GUIDE.md)
- [Templates](../00_foundation/STYLE_GUIDE.md#4-templates)
- [Migration Plan](../05_delivery_and_ops/MIGRATION_PLAN.md)

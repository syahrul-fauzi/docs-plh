---
title: Engineering Best Practices
version: 1.0.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [best-practices, standards, clean-code, security]
agent_context: This document outlines the engineering standards and best practices for the Lawyers Hub project, focusing on code quality, security, and performance.
---

# 🌟 Engineering Best Practices

## 1. Code Quality & Structure

### Clean Architecture
Always separate business logic from infrastructure.
- **Entities**: Pure business objects.
- **Use Cases**: Orchestrate business rules.
- **Repositories**: Abstract data access.

### SOLID Principles
- **SRP**: Each class/function should do one thing well.
- **DIP**: Depend on abstractions, not concretions. Use NestJS Dependency Injection.

## 2. Security (Legal Tech Standard)

### Zero Trust Data Access
Never trust the client-provided `tenantId`. Always extract it from the authenticated JWT on the server side.

### PII Protection
Before logging any data or sending it to an external AI service, always run it through the `@lawyers-hub/security` masking utility.

### Secure Logging
Never log passwords, secrets, or PII. Use the `AuditLogger` for tracking sensitive actions.

## 3. AI & LLM Best Practices

### Prompt Governance
Store all system prompts in version-controlled files (e.g., `.yaml` or `.json`) rather than hardcoding them in the source code.

### Deterministic Validation
AI is probabilistic. Always wrap AI outputs in a validation layer (e.g., Zod for schema, `LegalRulesEngine` for legal compliance).

## 4. Performance Optimization

### Efficient Querying
Avoid `SELECT *`. Always use Prisma's `select` or `include` to fetch only the necessary fields.

### Multi-level Caching
- Use **Redis** for global, shared data (e.g., document templates).
- Use **Local Memory** for frequently accessed, small datasets within a single request cycle.

---
*Following these practices ensures our system remains scalable, secure, and maintainable.*

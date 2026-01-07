---
title: Compliance & Audit Logging Flow
version: 1.0.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [compliance, audit, logging, security, uu-pdp]
agent_context: This document details the mechanism of automated audit logging for every sensitive operation within the Lawyers Hub ecosystem.
---

# 📜 Compliance & Audit Logging Flow

Ensuring a tamper-proof audit trail is a core requirement for legal tech compliance (ISO 27001, UU PDP).

## 1. Automated Audit Interceptor Flow

Every write operation (POST, PUT, DELETE) and sensitive read operation is intercepted by the global `AuditInterceptor`.

```mermaid
sequenceDiagram
    participant User
    participant API as NestJS API Gateway
    participant Interceptor as AuditInterceptor
    participant Sec as Security Package
    participant DB as PostgreSQL (Audit Table)

    User->>API: Request (e.g., Update Case #123)
    API->>Interceptor: Intercept Request
    Interceptor->>Sec: Hash Sensitive Payload (for integrity)
    Interceptor->>DB: Async Log: Who, What, When, Where (IP), tenantId
    API->>API: Process Request Logic
    API-->>User: Success Response
```

### Logged Metadata:
- **Who**: `userId` and `tenantId` extracted from JWT.
- **What**: Endpoint, HTTP Method, Request Body (Masked), and Response Status.
- **When**: Precise timestamp (UTC).
- **Where**: Source IP Address and User-Agent.
- **Integrity**: Each log entry contains a cryptographic hash of the previous entry to prevent tampering (Chained Audit Trail).

## 2. PII Access Logging

When a user views sensitive client data (unmasking), a specific `PII_ACCESS` log is generated.

```mermaid
sequenceDiagram
    participant User
    participant UI as Web/Mobile App
    participant API as API Gateway
    participant Audit as PII Audit Service
    participant DB as DB

    User->>UI: Click "View NIK" (Unmask)
    UI->>API: Request Unmasking
    API->>Audit: Log PII Access Event
    Audit->>DB: Record: User 'X' viewed PII of Client 'Y'
    API-->>UI: Return Unmasked Value
```

## 3. Compliance Reporting
- **Automated Alerts**: The SRE team is notified if more than 10 RLS violations occur within a minute for a specific IP.
- **Retention**: Audit logs are retained for 10 years as per legal regulatory requirements.
- **Immutability**: Once written to the `audit_logs` table, entries cannot be modified or deleted, even by system administrators (enforced by DB triggers).

---
title: System Architecture Overview
version: 1.1.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [architecture, multi-tenancy, security, ai, rag]
agent_context: This document provides a high-level overview of the Lawyers Hub architecture, including multi-tenancy, security standards, and AI orchestration.
---

# ⚖️ Lawyers Hub System Architecture

## 1. Overview
Lawyers Hub is a sophisticated multi-tenant SaaS platform designed for the legal industry. It integrates deterministic legal logic with advanced AI capabilities while ensuring strict compliance with data privacy regulations (e.g., UU PDP No. 27/2022 and GDPR).

## 2. High-Level Architecture
The system follows a **Clean Architecture** approach within a **Turborepo** monorepo structure.

```mermaid
graph TD
    subgraph Frontend
        Web[Next.js Web App]
        Mobile[Expo/React Native]
    end

    subgraph Backend_Services
        API[NestJS API Gateway]
        Worker[BullMQ Workers]
        AIGateway[AI Orchestration Gateway]
    end

    subgraph Shared_Packages
        Security[@lawyers-hub/security - PII Masking & Encryption]
        AI[@lawyers-hub/copilot - RAG Engine]
        Rules[@lawyers-hub/rules-engine - Legal Logic]
        DB[@lawyers-hub/database - Prisma RLS]
    end

    subgraph Data_Storage
        Postgres[(PostgreSQL + RLS)]
        Redis[(Redis - Queue/Cache)]
        VectorDB[(Vector Store - Pinecone/pgvector)]
        S3[(Object Storage - Encrypted)]
    end

    Web --> API
    Mobile --> API
    API --> Security
    API --> AIGateway
    API --> DB
    AIGateway --> AI
    AIGateway --> Rules
    Worker --> AI
    AI --> VectorDB
    DB --> Postgres
    API --> Redis
    Security --> S3
```

## 3. Core Architectural Pillars

### 3.1. Multi-tenancy with Row Level Security (RLS)
We employ **Logical Isolation** to ensure data privacy between different law firms (tenants).
- **Tenant ID**: Every entity (User, Case, Document) is scoped by a `tenantId`.
- **Postgres RLS**: Policies at the database level prevent cross-tenant data access.
- **JWT-Based Scoping**: The `tenantId` is extracted from the JWT and passed through the `PrismaService.withTenant()` helper for all queries.

### 3.2. AI Orchestration & RAG Pipeline
The AI system is designed to be deterministic and explainable.
- **Explainable AI (XAI)**: Every AI action is traceable and auditable. The `AgentSupervisor` logs the reasoning behind rule-based interventions.
- **PII Masking**: Sensitive data (NIK, names, etc.) is masked using Microsoft Presidio before being sent to external LLMs.
- **Deterministic Fallback**: AI outputs are validated against the `LegalRulesEngine` to ensure compliance with rigid legal rules.
- **Contextual Retrieval (RAG)**:
   - Documents are chunked hierarchically (Document -> Chapter -> Article) to preserve legal structure.
   - Vector search is strictly scoped to the tenant's namespace using metadata filters.

### 3.3. Security & Compliance (Legal Tech Standards)
- **Encryption at Rest**: Sensitive data is encrypted using AES-256-GCM.
- **Encryption in Transit**: Mandatory TLS/SSL for all communications.
- **Audit Trail**: Every mutation and sensitive read is logged via a global `AuditInterceptor`, capturing:
    - **Who**: Actor (User ID + Tenant ID)
    - **What**: Action (POST/PUT/DELETE) and Payload
    - **When**: Precise timestamp
    - **Where**: Source IP and Endpoint
- **UU PDP Compliance**: Support for data minimization, automated masking, and the "Right to be Forgotten" via automated deletion scripts.

## 4. Technology Stack
- **Monorepo**: Turborepo
- **Frontend**: Next.js 14, React Native (Expo)
- **Backend**: NestJS, Prisma
- **AI**: LangChain, OpenAI/Anthropic, Yjs (Collaboration)
- **Infrastructure**: PostgreSQL, Redis, Pinecone

---
*For detailed technical specifications, refer to [Technical Specification](technical_spec.md).*

---
title: Detailed Technical Specification
version: 1.0.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [specification, tech-stack, rag, collaboration, security]
agent_context: This document contains the detailed technical specifications for the Lawyers Hub platform, covering the tech stack, data isolation, AI pipelines, and collaboration engines.
---

# Technical Specification: Lawyers Hub

## 1. System Overview
Lawyers Hub is a multi-tenant platform for legal practice management, leveraging AI for document drafting, research, and compliance.

## 2. Core Architecture & Tech Stack
- **Monorepo Management**: Turborepo.
- **Frontend**: Next.js 14 (App Router), Tailwind CSS, TanStack Query.
- **Backend**: NestJS (Modular Monolith, ready for Microservices).
- **Database**: PostgreSQL with Prisma ORM.
- **AI Gateway**: Custom implementation using LangChain, OpenAI, and Anthropic.
- **Security**: Microsoft Presidio for PII masking, AES-256-GCM for document encryption.

## 3. Data Isolation (Multi-tenancy)
- **Database Level**: Postgres Row Level Security (RLS) ensures tenant isolation.
- **Application Level**: All API requests must include a `tenantId` (derived from JWT), which is passed to the `PrismaService.withTenant()` helper.
- **Vector Level**: Each tenant has a dedicated namespace/metadata filter in the vector database to prevent cross-tenant data leakage during RAG.

## 4. AI & RAG Pipeline
1. **Ingestion**: Documents are chunked hierarchically (Document -> Chapter -> Article) to preserve legal context.
2. **Embedding**: Chunks are embedded using `text-embedding-3-small`.
3. **Storage**: Vectors are stored in Pinecone or pgvector with mandatory `tenantId` filtering.
4. **Retrieval**: Hybrid search (Semantic + Keyword) provides the most relevant legal context.
5. **Generation**:
    - PII is masked from the prompt and context using `PresidioMaskingService`.
    - Output is validated against deterministic legal rules (Level 0-2) using the `LegalRulesEngine`.

## 5. Real-time Collaboration
- **Engine**: Yjs (CRDT) for conflict-free concurrent editing.
- **Transport**: WebSockets via Socket.io.
- **Editor**: Tiptap with Collaboration extension.
- **Consistency**: CRDTs ensure that all collaborators see the same state without centralized locking.

## 6. Security & Compliance
- **PII Masking**: Custom regex and NER models for Indonesian-specific data (NIK, NPWP, Nama Lengkap).
- **Audit Trail**: Every document access and modification is logged in the `audit_logs` table.
- **Encryption**: Documents in Object Storage (S3) are encrypted at rest using tenant-specific keys (where applicable).
- **GDPR/UU PDP**: Automated scripts handle data deletion requests to support the "Right to be Forgotten".

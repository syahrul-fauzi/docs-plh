# Technical Specification: Lawyers Hub

## 1. System Overview
Lawyers Hub is a multi-tenant platform for legal practice management, leveraging AI for document drafting, research, and compliance.

## 2. Core Architecture
- **Frontend**: Next.js 14 (App Router), Tailwind CSS, TanStack Query.
- **Backend**: NestJS (Monolithic Core with Microservice-ready structure).
- **Database**: PostgreSQL with Prisma ORM.
- **AI Gateway**: Custom implementation using LangChain, OpenAI, and Anthropic.
- **Security**: Microsoft Presidio for PII masking, AES-256-GCM for document encryption.

## 3. Data Isolation (Multi-tenancy)
- **Database Level**: Row Level Security (RLS) is used to ensure that users can only access data belonging to their tenant.
- **Application Level**: All API requests must include a `tenantId` (derived from JWT), which is passed to the `PrismaService.withTenant()` helper.
- **Vector Level**: Each tenant has a dedicated namespace in the vector database to prevent cross-tenant data leakage during RAG.

## 4. AI & RAG Pipeline
1.  **Ingestion**: Documents are chunked hierarchically (Document -> Chapter -> Article).
2.  **Embedding**: Chunks are embedded using `text-embedding-3-small`.
3.  **Storage**: Vectors are stored in Pinecone/pgvector with `tenantId` namespaces.
4.  **Retrieval**: Hybrid search (Semantic + Keyword) is used to find relevant context.
5.  **Generation**: 
    - PII is masked from the prompt and context using `PresidioMaskingService`.
    - Prompt is sent to LLM.
    - Output is validated against deterministic legal rules (Level 0-2).

## 5. Real-time Collaboration
- **Engine**: Yjs (CRDT).
- **Transport**: Socket.io.
- **Editor**: Tiptap with Collaboration extension.
- **Consistency**: Conflict-free replicated data types ensure no data loss during concurrent edits.

## 6. Security & Compliance
- **PII Masking**: Custom regex and NER for Indonesian-specific data (NIK, NPWP).
- **Audit Trail**: Every document access and modification is logged in `audit_logs`.
- **Encryption**: Documents in S3/Storage are encrypted at rest.
- **GDPR/UU PDP**: Support for "Right to be Forgotten" via automated data deletion scripts.

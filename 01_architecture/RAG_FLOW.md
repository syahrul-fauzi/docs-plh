---
title: AI & RAG Pipeline Flow
version: 1.0.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [ai, rag, pipeline, flow, security]
agent_context: This document details the step-by-step flow of the Retrieval-Augmented Generation (RAG) pipeline, from document ingestion to validated AI response.
---

# 🧠 AI & RAG Pipeline Flow

This document outlines the end-to-step process of how Lawyers Hub processes legal documents and generates AI-assisted content while maintaining strict data privacy and legal accuracy.

## 1. Document Ingestion Flow (Background)

```mermaid
sequenceDiagram
    participant User
    participant API as API Gateway (NestJS)
    participant Sec as Security Package (@lawyers-hub/security)
    participant Worker as Background Worker (BullMQ)
    participant Vector as Vector Store (Pinecone/pgvector)
    participant S3 as Object Storage (Encrypted)

    User->>API: Upload Document (.pdf, .docx)
    API->>Sec: Extract PII & Masking (Metadata Only)
    API->>S3: Store Original Encrypted File
    API->>Worker: Dispatch "process_document" Job
    Worker->>Worker: Chunking (Hierarchical: Doc -> Art -> Sec)
    Worker->>Sec: Mask PII in Chunks (Presidio)
    Worker->>Vector: Generate Embeddings & Store with tenantId Metadata
```

### Key Technical Details:
- **Hierarchical Chunking**: Unlike standard chunking, legal documents are split based on their structural hierarchy (e.g., Articles, Paragraphs) to ensure that the AI understands the context of a specific legal clause.
- **Tenant Isolation**: Every vector stored in the database is tagged with a `tenantId`. RLS-like filtering is applied at the query level.

## 2. Retrieval & Generation Flow (User Request)

```mermaid
sequenceDiagram
    participant User
    participant API as API Gateway
    participant AI as AI Orchestrator (LangChain)
    participant Vector as Vector Store
    participant Rules as Rules Engine (@lawyers-hub/rules-engine)
    participant LLM as External LLM (OpenAI/Anthropic)

    User->>API: Query (e.g., "Draft a termination clause")
    API->>AI: Initialize Chain with tenantId
    AI->>Vector: Semantic Search (Filter by tenantId)
    Vector-->>AI: Return Relevant Legal Context (Masked)
    AI->>LLM: Augmented Prompt (Context + Query + System Rules)
    LLM-->>AI: Probabilistic Response
    AI->>Rules: Validate Output against LegalRulesEngine
    Rules-->>AI: Approved / Adjusted Action
    AI-->>API: Final Validated Response
    API-->>User: Display Response with Citations
```

### Strategic Oversight:
- **Masked Retrieval**: We retrieve masked data from the vector store. The LLM never sees the raw PII of the client.
- **Deterministic Validation**: The `LegalRulesEngine` checks if the AI-generated clause violates any rigid firm policies or local laws.

## 3. Best Practices for RAG
- **Hybrid Search**: We combine semantic search with keyword matching (BM25) to ensure that specific legal citations are found even if they are semantically distant.
- **Explainability**: Every response must include citations back to the source document chunks to allow human verification.
- **Cost Optimization**: Chunks are cached in Redis to avoid redundant embedding generation and vector search for common legal queries.

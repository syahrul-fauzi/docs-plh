# Technical Architecture Detail — Lawyers Hub

**Status:** DRAFT **Versi:** 1.0.0 **Tanggal:** 2026-01-07

## 1. Arsitektur Komponen (Monorepo)
Lawyers Hub menggunakan struktur monorepo berbasis Turborepo untuk memastikan konsistensi kode antara Web dan Desktop.

### 1.1 Frontend (Web & Desktop)
- **Web App (`apps/web`)**: Next.js 14 dengan App Router, Tailwind CSS, dan CopilotKit.
- **Desktop App (`apps/desktop`)**: Tauri 2.0 membungkus aplikasi web dengan Rust backend untuk akses sistem file native.

### 1.2 Backend Services (`apps/api`)
- **Framework**: NestJS (Node.js).
- **ORM**: Prisma dengan database PostgreSQL.
- **Worker**: BullMQ untuk pemrosesan latar belakang (OCR, AI Ingestion).

### 1.3 AI Interaction Layer
- **CopilotKit**: Digunakan sebagai orkestrator interaksi AI di frontend.
- **AI Gateway**: Bertindak sebagai proxy untuk masking PII (Personally Identifiable Information) sebelum mengirim prompt ke LLM.

## 2. Alur Data (Data Flow)
### 2.1 Alur Pembuatan Dokumen (AI-Assisted)
1. User memasukkan prompt di UI.
2. CopilotKit mengirimkan konteks perkara ke AI Gateway.
3. AI Gateway melakukan masking data sensitif.
4. LLM menghasilkan draf dokumen.
5. AI Gateway melakukan unmasking dan mengirimkan draf ke UI.
6. User melakukan review dan menyimpan dokumen ke Case Vault.

## 3. Keamanan & Skalabilitas
- **Tenant Isolation**: Menggunakan Row Level Security (RLS) di database.
- **Encryption**: Enkripsi AES-256 untuk dokumen yang disimpan di cloud.
- **Scalability**: Stateless API design yang mendukung deployment di cluster Kubernetes.

---
*Dokumen ini merupakan spesifikasi teknis resmi untuk pengembangan Lawyers Hub.*

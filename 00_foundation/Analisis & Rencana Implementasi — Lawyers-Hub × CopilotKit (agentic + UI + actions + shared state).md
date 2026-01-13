# Analisis & Rencana Implementasi — **Lawyers-Hub** × **CopilotKit (agentic + UI + actions + shared state)**

## Metadata

- **Document ID**: LH-IMP-COPILOT-001
- **Status**: Implemented v1.0 (Verified)
- **Last Updated**: 2026-01-08
- **Implementation Files**:
  - Web Wrapper (Tenant-aware + Auth headers + UI theming):
    [CopilotWrapper.tsx](file:///home/inbox/smart-ai/lawyers-hub/apps/web/src/features/chat/ui/CopilotWrapper.tsx)
  - Chat UI (Headless + Generative UI + HITL):
    [HeadlessChat.tsx](file:///home/inbox/smart-ai/lawyers-hub/apps/web/src/features/chat/ui/HeadlessChat.tsx)
  - Chat Feature (Composition + workflow orchestration):
    [ChatFeature.tsx](file:///home/inbox/smart-ai/lawyers-hub/apps/web/src/features/chat/ui/ChatFeature.tsx)
  - Chat Page (Tenant route):
    [page.tsx](file:///home/inbox/smart-ai/lawyers-hub/apps/web/src/app/(tenant)/dashboard/chat/page.tsx)
  - CopilotKit Proxy Endpoint (Web → AI Gateway):
    [route.ts](file:///home/inbox/smart-ai/lawyers-hub/apps/web/src/app/api/copilotkit/route.ts)
  - AI Gateway (Backend actions + governance + metrics):
    [copilotkit.controller.ts](file:///home/inbox/smart-ai/lawyers-hub/apps/ai-gateway/src/copilotkit.controller.ts)
  - Tests:
    [HeadlessChat.test.tsx](file:///home/inbox/smart-ai/lawyers-hub/apps/web/src/features/chat/ui/HeadlessChat.test.tsx)
- **Owner**: Lead AI Architect
- **Stakeholders**: Engineering, AI Team, UX Design, Legal Compliance

---

## 1. Strategi Pengembangan Antarmuka Chat AI (Agentic Chat UI)

_Ref: <https://docs.copilotkit.ai/agentic-chat-ui>_

### 1.1 Kemampuan Inti

- **Eksekusi Dinamis**: Tools dieksekusi melalui AI Gateway (`/copilotkit`) dan dipanggil dari UI via `/api/copilotkit` (proxy) untuk menjaga isolasi dan kontrol.
- **State Management**: Konteks aplikasi disuntikkan sebagai shared state dengan `useCopilotReadable` agar agent memahami kondisi kerja (kasus, dokumen, role, quota).
- **NLP & LLM**: Adapter backend menggunakan model terbaru (default: `gpt-4o`) dan dapat difallback ke mode mock saat API key belum tersedia.
- **Integrasi Backend**: Backend actions berjalan di AI Gateway (NestJS) dengan guard auth + tenant serta pencatatan metrik.

---

## 2. Kustomisasi UI & Pengalaman Pengguna (Custom Look and Feel)

_Ref: <https://docs.copilotkit.ai/custom-look-and-feel>_

### 2.1 Audit & Modifikasi Komponen

- **Headless UI**: Chat dirender dengan kontrol penuh (headless) di layer `features/chat/ui` dan mendukung komponen generatif untuk hasil tools.
- **Brand Alignment**: Kustomisasi total menggunakan Tailwind CSS (`indigo-900`, `amber-500`) sesuai brand guideline Lawyers Hub.
- **Custom Components**: Penggunaan komponen kustom untuk message bubbles, action previews, dan agent state agar sesuai brand guideline.

---

## 3. Sistem Saran Cerdas (Copilot Suggestions)

_Ref: <https://docs.copilotkit.ai/copilot-suggestions>_

### 3.1 Mekanisme Proaktif

- **Integrasi Hook**: Saran dihasilkan berbasis konteks aplikasi (shared state) menggunakan `useCopilotChatSuggestions`.

---

## 4. Kolaborasi Human-AI (Human-in-the-Loop)

_Ref: <https://docs.copilotkit.ai/human-in-the-loop>_

### 4.1 Workflow Verifikasi

- **Multi-step Task Completion**: Aksi sensitif menggunakan mekanisme konfirmasi eksplisit sebelum dieksekusi (approval UI).
- **Confidence Score**: Keputusan dapat digate berdasarkan skor keyakinan untuk memaksa verifikasi pengguna pada operasi kritis.

---

## 5. UI Generatif (Generative UI)

_Ref: <https://docs.copilotkit.ai/generative-ui>_

### 5.1 Adaptivitas Komponen

- **Dynamic Rendering**: Tool calls divisualisasikan sebagai komponen React (action previews / cards) agar hasil lebih operasional daripada teks mentah.
- **Real-time UI Updates**: Status eksekusi tool (`inProgress` → `complete`) dipresentasikan sebagai state UI yang jelas.

---

## 6. Aksi Frontend & Backend (Actions System)

_Ref: <https://docs.copilotkit.ai/frontend-actions> | <https://docs.copilotkit.ai/backend-actions>_

### 6.1 Frontend Actions
- Tool sisi klien dipakai untuk aksi UI (navigasi, scroll, update state editor) yang tidak memerlukan akses data sensitif.

### 6.2 Backend Actions
- Tool sisi server didefinisikan di AI Gateway untuk operasi yang butuh autentikasi, akses database, dan auditability.

---

## 7. Manajemen State Terbagi (Shared State)

_Ref: <https://docs.copilotkit.ai/shared-state>_

### 7.1 Sinkronisasi Dua Arah
- **`useCopilotReadable`**: Memastikan AI selalu sadar akan ID kasus, judul, dan status terkini yang sedang dibuka oleh pengguna di dashboard.

---

## 8. Status Penguncian

✅ **Locked — Implementasi Selesai & Terverifikasi**
File implementasi telah dibuat dan disesuaikan dengan struktur Next.js App Router yang valid.

# Project Plan: Lawyers Hub Go-Live (Januari 2026)

## 1. Timeline & Milestones

| Minggu       | Fokus               | Milestone                                                            | Status          |
| :----------- | :------------------ | :------------------------------------------------------------------- | :-------------- |
| **Minggu 1** | Audit & Stabilitas  | Finalisasi audit kode, perbaikan type safety, dan optimasi build.    | [x] Selesai     |
| **Minggu 2** | QA & Testing        | Uji coba fungsional (E2E), audit UI/UX, dan pengujian performa.      | [ ] In Progress |
| **Minggu 3** | Dokumentasi & Infra | Finalisasi teknis dokumentasi dan persiapan pipeline CI/CD produksi. | [ ] Pending     |
| **Minggu 4** | Go-Live             | Final security audit (OWASP) dan deployment canary ke produksi.      | [ ] Pending     |

## 2. Alokasi Resource (Role Based)

| Role                               | Tanggung Jawab Utama                                    | Alokasi       |
| :--------------------------------- | :------------------------------------------------------ | :------------ |
| **Senior Developer (AI/Security)** | PII Masking Engine, RAG Optimization, Security Audit.   | 40 jam/minggu |
| **Frontend Lead (UI/UX)**          | Dashboard Next.js, Framer Motion, Accessibility (WCAG). | 30 jam/minggu |
| **Backend Engineer (API)**         | NestJS Microservices, Prisma ORM, BullMQ Worker.        | 30 jam/minggu |
| **QA/DevOps**                      | CI/CD Pipeline, E2E Testing, Monitoring (Grafana).      | 20 jam/minggu |

## 3. Strategi Pengujian (QA Strategy)

### A. Fungsional

- **Unit Testing**: Jest (Backend/Frontend).
- **E2E Testing**: Playwright (Compliance Flow, Document Lifecycle).
- **Manual UAT**: Verifikasi skenario hukum nyata.

### B. Non-Fungsional

- **Performa**: Load testing dengan k6 (Target: 500 concurrent users).
- **Keamanan**: OWASP Top 10 Audit & Penetration Testing.
- **Cross-platform**: Testing pada Chrome, Safari, Firefox, iOS, dan Android.

## 4. Detil Rencana Finalisasi (Phase 4)

Berikut adalah rincian untuk 4 langkah penyelesaian akhir:

### 1. Deployment ke Environment Staging

- **Timeline**: 5 - 7 Januari 2026
- **Penanggung Jawab**: QA/DevOps Lead
- **Kriteria Keberhasilan**:
  - Build aplikasi berhasil tanpa error di environment staging.
  - Semua tes kesehatan (Smoke Test) lulus 100%.
  - Akses UAT tersedia untuk stakeholder dengan kredensial yang valid.
- **Dokumen Pendukung**:
  - [deploy-staging.sh](file:///home/inbox/smart-ai/lawyers-hub/scripts/deploy-staging.sh)
  - [verify-staging.ts](file:///home/inbox/smart-ai/lawyers-hub/scripts/verify-staging.ts)
  - [DEPLOYMENT.md](file:///home/inbox/smart-ai/lawyers-hub/docs/deployment/DEPLOYMENT.md)

### 2. Penyusunan Manual Pengguna (User Guide)

- **Timeline**: 8 - 10 Januari 2026
- **Penanggung Jawab**: Frontend Lead / Technical Writer
- **Kriteria Keberhasilan**:
  - Dokumentasi mencakup seluruh fitur stabil (Dashboard, AI Drafting, PII
    Masking).
  - Tersedia panduan instalasi dan tabel troubleshooting yang jelas.
  - Dokumen disetujui oleh tim produk.
- **Dokumen Pendukung**:
  - [USER_GUIDE.md](file:///home/inbox/smart-ai/lawyers-hub/docs/USER_GUIDE.md)

### 3. Pelaksanaan Load Testing menggunakan k6

- **Timeline**: 11 - 13 Januari 2026
- **Penanggung Jawab**: Backend Engineer / QA
- **Kriteria Keberhasilan**:
  - Sistem mampu menangani 100 concurrent users.
  - Response time P95 < 2 detik.
  - Error rate < 1% selama durasi pengujian.
- **Dokumen Pendukung**:
  - [k6-load-test.js](file:///home/inbox/smart-ai/lawyers-hub/test/load/k6-load-test.js)

### 4. Persiapan & Riset Best Practices

- **Timeline**: 5 - 13 Januari 2026 (Berkelanjutan)
- **Penanggung Jawab**: Senior Developer
- **Kriteria Keberhasilan**:
  - Laporan riset mencakup teknik deployment dan load testing terbaru.
  - Rekomendasi optimasi (seperti caching PII Masking) didokumentasikan.
- **Dokumen Pendukung**:
  - [DEPLOYMENT_RESEARCH.md](file:///home/inbox/smart-ai/lawyers-hub/docs/deployment/DEPLOYMENT_RESEARCH.md)

## 5. Daily Standup Focus

- **Hari 1-3**: Penyelesaian sisa linting errors di `apps/web`.
- **Hari 4-5**: Eksekusi audit aksesibilitas (WCAG).
- **Hari 6-7**: Penulisan Technical Guide lengkap.

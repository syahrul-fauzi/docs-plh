# Kriteria Penerimaan (Acceptance Criteria) - Lawyers Hub
 
 Dokumen ini mendefinisikan kriteria terukur untuk memastikan solusi memenuhi kebutuhan bisnis dan standar kualitas industri.
 
 ## 1. Kriteria Fitur Inti (P0 - MVP)
 
 ### 1.1 AI Legal Assistant (Copilot)
 - [ ] **Disclaimer**: Setiap output AI wajib menyertakan disclaimer "Draft/Rekomendasi".
 - [ ] **Citation**: AI mampu memberikan referensi (link/dokumen) untuk klaim hukum.
 - [ ] **Refusal**: AI menolak memberikan "Keputusan Hukum Final" (Red Zone).
 - [ ] **Context**: AI hanya memiliki akses ke data tenant yang sedang login.
 
 ### 1.2 Case Management
 - [ ] **CRUD**: Lawyer dapat membuat, mengupdate, dan menutup perkara.
 - [ ] **Timeline**: Setiap perubahan status case tercatat otomatis dalam timeline.
 - [ ] **Attachment**: Sistem mendukung upload bukti/dokumen dengan enkripsi saat istirahat (at rest).
 
 ### 1.3 Document Automation
 - [ ] **Template**: Pengguna dapat memilih template standar (e.g., NDA, Somasi).
 - [ ] **Versioning**: Setiap perubahan pada draft dokumen tersimpan sebagai versi baru.
 - [ ] **Export**: Dokumen dapat diekspor ke format PDF/Docx dengan formatting yang benar.
 
 ### 1.4 Onboarding & Verification
 - [ ] **KYC/KYB**: Lawyer wajib mengupload bukti kartu anggota (KAI/PERADI) sebelum akun aktif.
 - [ ] **Multi-tenancy**: Data antar Law Firm terisolasi secara database (Row Level Security).
 
 ### 1.5 Audit & Compliance
 - [ ] **AI Logs**: Setiap interaksi AI tersimpan dalam log audit (immutable).
 - [ ] **Access Logs**: Setiap akses ke dokumen sensitif tercatat (User, IP, Timestamp).
 
 ## 2. Keamanan & Privasi (UU PDP No. 27/2022)
 | Kriteria | Metrik Target | Metode Verifikasi |
 | :--- | :--- | :--- |
 | **PII Masking Accuracy** | > 95% untuk data terstruktur (NIK, NPWP, Email) | Unit Testing & Manual Audit |
 | **Data Isolation** | 0% kebocoran data antar tenant | Penetration Testing / RLS Audit |
 | **Audit Logging** | 100% akses data sensitif tercatat | Verifikasi tabel `PIIAuditLog` |
 | **Compliance Reporting** | Mampu menghasilkan laporan insiden dalam < 24 jam | Simulasi Incident Response |
 
 ## 3. Performa Sistem (RAG Engine)
 | Kriteria | Metrik Target | Metode Verifikasi |
 | :--- | :--- | :--- |
 | **Latency Query** | < 2 detik (termasuk masking & retrieval) | Load Testing (k6/JMeter) |
 | **Accuracy Retrieval** | Top-3 relevansi > 80% | Benchmarking dengan set data hukum |
 | **Embedding Speed** | < 500ms per dokumen standar | Profiling AI Package |
 | **Concurrency** | Mendukung 50+ user simultan per tenant | Stress Testing |
 
 ## 4. Kualitas Kode (Quality Gates)
 | Kriteria | Metrik Target | Metode Verifikasi |
 | :--- | :--- | :--- |
 | **Test Coverage** | > 80% line coverage di semua package | Jest Coverage Report |
 | **Static Analysis** | 0 Critical/High issues | ESLint & SonarQube |
 | **Documentation** | 100% API terdokumentasi | Swagger / OpenAPI Check |
 | **Build Success** | 100% pass di CI/CD pipeline | Turborepo build log |
 
 ---
 *Terakhir Diperbarui: 2026-01-06 (Aligned with Core Features Spec v0.1)*

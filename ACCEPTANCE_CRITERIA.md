# Kriteria Penerimaan (Acceptance Criteria) - Lawyers Hub

Dokumen ini mendefinisikan kriteria terukur untuk memastikan solusi memenuhi kebutuhan bisnis dan standar kualitas industri.

## 1. Keamanan & Privasi (UU PDP No. 27/2022)
| Kriteria | Metrik Target | Metode Verifikasi |
| :--- | :--- | :--- |
| **PII Masking Accuracy** | > 95% untuk data terstruktur (NIK, NPWP, Email) | Unit Testing & Manual Audit |
| **Data Isolation** | 0% kebocoran data antar tenant | Penetration Testing / RLS Audit |
| **Audit Logging** | 100% akses data sensitif tercatat | Verifikasi tabel `PIIAuditLog` |
| **Compliance Reporting** | Mampu menghasilkan laporan insiden dalam < 24 jam | Simulasi Incident Response |

## 2. Performa Sistem (RAG Engine)
| Kriteria | Metrik Target | Metode Verifikasi |
| :--- | :--- | :--- |
| **Latency Query** | < 2 detik (termasuk masking & retrieval) | Load Testing (k6/JMeter) |
| **Accuracy Retrieval** | Top-3 relevansi > 80% | Benchmarking dengan set data hukum |
| **Embedding Speed** | < 500ms per dokumen standar | Profiling AI Package |
| **Concurrency** | Mendukung 50+ user simultan per tenant | Stress Testing |

## 3. Kualitas Kode (Quality Gates)
| Kriteria | Metrik Target | Metode Verifikasi |
| :--- | :--- | :--- |
| **Test Coverage** | > 80% line coverage di semua package | Jest Coverage Report |
| **Static Analysis** | 0 Critical/High issues | ESLint & SonarQube |
| **Documentation** | 100% API terdokumentasi | Swagger / OpenAPI Check |
| **Build Success** | 100% pass di CI/CD pipeline | Turborepo build log |

## 4. Kebutuhan Fungsional (User Experience)
- **Dashboard**: Memuat dalam < 1 detik untuk metadata awal.
- **RAG Interface**: Memberikan sitasi yang valid ke dokumen sumber.
- **Drafting**: Menghasilkan dokumen hukum yang mematuhi aturan (mandatory clauses).
- **Multi-tenancy**: Admin tenant dapat mengelola user dalam organisasinya tanpa akses ke organisasi lain.

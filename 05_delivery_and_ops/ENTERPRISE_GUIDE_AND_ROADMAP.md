# Arsitektur & Roadmap Lawyers Hub Enterprise

## 1. Arsitektur Multi-Tenant

Sistem menggunakan pendekatan **Logical Isolation** pada level database:

- **PostgreSQL RLS (Row Level Security)**: Memastikan data antar tenant tidak
  bocor.
- **Tenant Context**: Setiap request melalui `AuthGuard` mengekstrak `tenantId`
  dari JWT terenkripsi.
- **Prisma withTenant Helper**: Middleware otomatis yang menyuntikkan
  `SET LOCAL app.current_tenant` pada setiap transaksi database.

## 2. Keamanan & Kepatuhan Hukum

- **Audit Trail**: Setiap tindakan sensitif (pembuatan kasus, penagihan, akses
  dokumen) dicatat menggunakan `AuditService` dengan metadata terenkripsi.
- **Data Encryption**: PII (Personally Identifiable Information) dienkripsi saat
  istirahat (at rest) menggunakan standar AES-256.
- **Mobile Security**: Token disimpan menggunakan `expo-secure-store` yang
  memanfaatkan Keychain (iOS) atau Keystore (Android).

## 3. Strategi Deployment Enterprise

- **Scalability**: Backend NestJS didesain stateless untuk mendukung
  auto-scaling di Kubernetes/AWS ECS.
- **High Availability**: Multi-AZ deployment untuk PostgreSQL dengan read
  replicas guna optimasi laporan analitik.
- **CI/CD**: Pipeline otomatis menggunakan GitHub Actions untuk pengujian unit,
  integrasi, dan build Expo EAS.

## 4. Roadmap Pengembangan Fitur

### Fase 1: Fondasi (Selesai)

- Multi-tenant auth & RLS.
- Core Case Management & Billing API.
- Mobile App Scaffold & Offline Caching.

### Fase 2: Enterprise Enhancements (Q1 2026)

- **Push Notifications**: Pengingat jadwal sidang dan jatuh tempo invoice.
- **Advanced Analytics**: Dashboard performa firma hukum dan laporan keuangan
  bulanan.
- **Document OCR**: Ekstraksi otomatis data dari dokumen hukum yang diunggah.

### Fase 3: AI Integration (Q2 2026)

- **Legal Research AI**: Asisten cerdas untuk riset yurisprudensi.
- **Contract Analyzer**: Deteksi otomatis klausul berisiko dalam kontrak.

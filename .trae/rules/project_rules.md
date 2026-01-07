# Aturan Proyek Lawyers Hub (Legal Tech Standard)

Dokumen ini mendefinisikan standar koding, proses pengembangan, dan protokol keamanan untuk ekosistem **Lawyers Hub**. Sebagai platform legal tech, kepatuhan (compliance) terhadap **GDPR**, **ISO 27001**, serta keamanan data klien dan integritas audit adalah prioritas utama.

---

## **Riwayat Versi**

| Versi | Tanggal | Deskripsi Perubahan | Penulis |
| :--- | :--- | :--- | :--- |
| 1.0.0 | 2026-01-07 | Inisialisasi aturan proyek (Agentic Implementation) | World-Class Super Agent |
| 1.1.0 | 2026-01-07 | Update kepatuhan GDPR/ISO, Git Hooks, & Security Scanning | World-Class Super Agent |

---

## **1. Struktur Direktori dan File**
Workspace ini adalah bagian dari monorepo **Lawyers Hub** yang menggunakan Turborepo. Direktori `docs/` berfungsi sebagai pusat pengetahuan (knowledge base) dan dokumentasi teknis.

### **Hierarki Monorepo Utama**
```text
/ (root)
├── apps/                 # Aplikasi mandiri (deployable units)
│   ├── api/              # Backend API (NestJS)
│   ├── web/              # Frontend Web (Next.js)
│   ├── mobile/           # Mobile App (Expo/React Native)
│   └── worker/           # Background Job Processor (BullMQ)
├── packages/             # Shared libraries & business logic
│   ├── core/             # Utilitas dasar, logger, error handling
│   ├── database/         # Prisma schema & database clients
│   ├── security/         # Enkripsi (AES-256-GCM), PII masking
│   ├── audit-log/        # Sistem pencatatan audit legal
│   └── ui/               # Shared components & theme
├── docs/                 # Pusat Dokumentasi (Workspace Saat Ini)
│   ├── 00_foundation/    # Dasar hukum & bisnis
│   ├── 01_architecture/  # Diagram & spek teknis
│   ├── 02_onboarding/    # Panduan developer baru
│   ├── api-reference/    # Dokumentasi endpoint (OpenAPI)
│   ├── legal/            # Kebijakan privasi & compliance (GDPR)
│   └── .trae/rules/      # Aturan khusus IDE Trae
└── .trae/rules/          # Aturan global monorepo
```

**Tanggung Jawab**: @Architecture-Lead

### **File Wajib dalam Docs**
- `README.md`: Index dokumentasi dan panduan navigasi.
- `ARCHITECTURE.md`: Gambaran besar sistem & desain multi-tenant.
- `CONTRIBUTING.md`: Panduan kontribusi teknis.
- `PROJECT_PLAN.md`: Roadmap pengembangan jangka pendek & panjang.
- `SECURITY.md`: Kebijakan pelaporan kerentanan.

**Checklist Verifikasi Section 1:**
- [ ] Apakah dokumen baru diletakkan di sub-direktori yang relevan?
- [ ] Apakah setiap folder memiliki `README.md` deskriptif?
- [ ] Apakah file menggunakan format Markdown dengan hierarchy yang benar?

---

## **2. Konvensi Penamaan**

### **Komponen & File**
- **React Components**: `PascalCase` (Contoh: `CaseDocumentViewer.tsx`).
- **Files/Folders**: `kebab-case` (Contoh: `audit-log/`, `use-case-handler.ts`).
- **Styles**: `camelCase` untuk CSS Modules atau Tailwind utility classes.

### **Fungsi & Variabel (JS/TS)**
- **Variabel/Fungsi**: `camelCase` (Contoh: `getTenantData()`).
- **Boolean**: Prefix `is`, `has`, atau `should` (Contoh: `isEncrypted`).
- **Constants**: `UPPER_SNAKE_CASE` (Contoh: `MAX_ENCRYPTION_RETRY`).
- **Interfaces/Types**: `PascalCase` tanpa prefix (Contoh: `UserSession`).

### **Contoh Implementasi**
```typescript
// ✅ BAIK
interface CaseDetails {
  caseId: string;
  isClosed: boolean;
}

const fetchCaseDetails = (id: string): CaseDetails => { ... };

// ❌ BURUK
interface ICase { // Hindari prefix I
  Case_ID: string; // Snake case
  Closed: boolean; // Tidak deskriptif
}
```

**Tanggung Jawab**: @Frontend-Lead & @Backend-Lead

**Checklist Verifikasi Section 2:**
- [ ] Apakah nama file menggunakan kebab-case?
- [ ] Apakah interface menggunakan PascalCase?
- [ ] Apakah variabel boolean memiliki prefix yang benar?

---

## **3. Standar Koding**

### **Format & Indentasi**
- **Indentasi**: 2 spasi (Standard JS/TS/MD).
- **Line Length**: Maksimal 100 karakter (kecuali tabel markdown).
- **Quotes**: Single quotes `'` untuk kode TS, double quotes `"` untuk JSON.

### **Komentar & Dokumentasi**
- **JSDoc**: Wajib untuk fungsi publik di `packages/`.
```typescript
/**
 * Mengenkripsi data sensitif menggunakan AES-256-GCM (ISO 27001 compliant).
 * @param data - String mentah yang akan dienkripsi.
 * @returns Object berisi ciphertext, iv, dan authTag.
 */
export function encryptSensitiveData(data: string): EncryptedPayload { ... }
```

### **Linter & Prettier**
- **ESLint**: Menggunakan konfigurasi `@typescript-eslint/recommended`.
- **Prettier**: Wajib dijalankan sebelum commit (`npm run format`).

**Tanggung Jawab**: @Core-Engineering-Team

**Checklist Verifikasi Section 3:**
- [ ] Apakah JSDoc sudah mencakup parameter dan return value?
- [ ] Apakah linter menunjukkan error/warning?
- [ ] Apakah indentasi sudah konsisten 2 spasi?

---

## **4. Proses Pengembangan**

### **Branching Strategy (Git Flow)**
1. **`main`**: Produksi (Stabil).
2. **`staging`**: Mirroring produksi untuk QA/UAT.
3. **`develop`**: Integrasi fitur harian.
4. **`feature/*`**: Fitur baru (Contoh: `feature/ai-pii-masking`).
5. **`fix/*`**: Perbaikan bug mendesak.

### **Commit Messages (Conventional Commits)**
Format: `<type>(<scope>): <description>`
- `feat`: Fitur baru.
- `fix`: Perbaikan bug.
- `security`: Perubahan terkait keamanan/compliance legal.
- `chore`: Update build process atau library.

### **Git Hooks (Husky + lint-staged)**
- **Pre-commit**: Menjalankan `lint` dan `format` pada file yang diubah.
- **Pre-push**: Menjalankan `test` untuk memastikan tidak ada regresi.

**Tanggung Jawab**: @Lead-Developer

**Checklist Verifikasi Section 4:**
- [ ] Apakah branch name sudah sesuai prefix?
- [ ] Apakah commit message mengikuti format conventional?
- [ ] Apakah lint & format sudah lolos via Husky?

---

## **5. Testing & QA**

### **Persyaratan Minimum**
- **Coverage**: Minimal 80% untuk logika di `packages/core` dan `packages/security`.
- **Jenis Test**:
  - **Unit**: Logika bisnis & utilitas (Jest).
  - **Integration**: API & Database flows (Supertest).
  - **E2E**: Flow kritis pengguna (Playwright).

### **QA Checklist (Legal Tech Specific)**
- [ ] Uji isolasi data (Tenant Isolation) berhasil.
- [ ] Log audit tercatat lengkap (Who, What, When, Where).
- [ ] PII redaction/masking berfungsi di logs & UI.

**Tanggung Jawab**: @QA-Specialist

**Checklist Verifikasi Section 5:**
- [ ] Apakah coverage report sudah diperbarui?
- [ ] Apakah skenario kegagalan (unauthorized access) sudah diuji?

---

## **6. Deployment & Environment**

### **Konfigurasi Environment**
- **Dev**: Local environment, Mock AI services.
- **Staging**: Mirroring Prod, integrasi Sandbox (Stripe, Clerk).
- **Production**: High Availability, AWS/GCP dengan enkripsi volume (ISO 27001).

### **Akses & Izin**
- Akses produksi dibatasi melalui RBAC (*Role-Based Access Control*).
- Penggunaan VPN/Zero Trust Network wajib untuk akses infrastruktur.

**Tanggung Jawab**: @DevOps-Engineer

**Checklist Verifikasi Section 6:**
- [ ] Apakah environment variables baru sudah didaftarkan di Doppler/Vault?
- [ ] Apakah akses ke produksi sudah dibatasi hanya untuk personel yang berwenang?

---

## **7. Dokumentasi**

### **Standar API**
- Menggunakan **Swagger/OpenAPI 3.0**.
- Endpoint sensitif wajib memiliki tag `@Security('TenantAuth')`.

### **Architecture Decision Records (ADR)**
- Setiap keputusan besar (misal: ganti database, integrasi LLM baru) wajib mencatat ADR di `docs/adr/`.

### **Onboarding Docs**
- Panduan setup local, struktur database, dan flow autentikasi wajib ada di `docs/02_onboarding/`.

**Tanggung Jawab**: @Technical-Writer & @Architecture-Lead

**Checklist Verifikasi Section 7:**
- [ ] Apakah ADR sudah diperbarui untuk perubahan arsitektur?
- [ ] Apakah panduan onboarding sudah mencakup langkah instalasi dependensi baru?

---

## **8. Integrasi Tools**

### **CI/CD Pipeline**
- **Build & Test**: Turbo build & GitHub Actions.
- **Security Scanning**:
  - **Snyk**: Scan kerentanan open-source & license compliance.
  - **TruffleHog/GitLeaks**: Scan secret/token yang tidak sengaja ter-commit.
- **Compliance Scan**: Otomatisasi pengecekan PII dalam output logs.

### **Monitoring**
- **Sentry**: Tracking error runtime & performance monitoring.
- **Grafana/Prometheus**: Metrik infrastruktur & query latency database.

**Tanggung Jawab**: @Site-Reliability-Engineer

**Checklist Verifikasi Section 8:**
- [ ] Apakah pipeline CI hijau (lulus lint, test, security scan)?
- [ ] Apakah ada dependensi baru dengan lisensi yang dilarang (misal: AGPL)?

---

## **Glossary**
- **AES-256-GCM**: Standar enkripsi simetris untuk perlindungan data klien.
- **PII**: Personally Identifiable Information (Nama, Alamat, NIK, dll).
- **RLS**: Row Level Security (Mekanisme isolasi tenant di PostgreSQL).
- **UPL**: Unauthorized Practice of Law (Batasan etika agar AI tidak menggantikan peran pengacara).
- **GDPR**: General Data Protection Regulation (Standar privasi data global).

---
**Owner**: @Engineering-Lead | **Last Updated**: 2026-01-07

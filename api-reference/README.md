# ⚖️ Lawyers Hub (PLH) API Reference

***

Lawyers Hub adalah platform manajemen hukum cerdas yang mengintegrasikan AI
Agents dengan logika hukum deterministik. Proyek ini menggunakan arsitektur
monorepo untuk mengelola frontend, backend, worker, dan paket-paket logika inti
secara efisien.

## 🚀 Fitur Utama

- **Agentic Rules Engine**: Memastikan AI bekerja sesuai dengan batasan etika
  dan hukum (Level 0-3).
- **Deterministic Fallback**: Mengurangi halusinasi AI dengan memvalidasi
  jawaban terhadap aturan hukum yang kaku.
- **Explainable AI (XAI)**: Setiap tindakan AI dapat dilacak dan diaudit.
- **Multi-Agent Coordination**: Kolaborasi antara berbagai spesialis AI
  (Logic, Structure, Synergy).
- **Compliance by Design**: Kepatuhan otomatis terhadap regulasi (seperti
  UU PDP No. 27/2022).

## 🏗️ Struktur Proyek

Proyek ini menggunakan **Turborepo** dengan struktur sebagai berikut:

- `apps/`
  - `web/`: Frontend utama menggunakan Next.js + Tailwind CSS.
  - `api/`: Core API menggunakan NestJS.
  - `worker/`: Background worker untuk tugas-tugas asinkron.
- `packages/`
  - `rules/`: Logika hukum deterministik (YAML + Engine).
  - `core/`: Utilitas dan logika bisnis bersama.
  - `database/`: Skema Prisma dan akses data.
  - `ui/`: Komponen UI bersama menggunakan React.
  - `security/`: Implementasi keamanan dan enkripsi.
  - `domain/`: Definisi domain hukum dan entitas.
  - `observability/`: Logging, metrik, dan monitoring (Prometheus/ELK).

## 🛠️ Teknologi Utama

- **Monorepo Management**: [Turborepo](https://turbo.build/)
- **Frontend**: [Next.js](https://nextjs.org/), [React](https://reactjs.org/),
  [TanStack Query](https://tanstack.com/query)
- **Backend**: [NestJS](https://nestjs.com/), [Prisma](https://www.prisma.io/)
- **Auth**: [Clerk](https://clerk.com/)
- **Payments**: [Stripe](https://stripe.com/)
- **Testing**: [Jest](https://jestjs.io/), [Playwright](https://playwright.dev/)
- **Validation**: [Zod](https://zod.dev/)

### 📑 Dokumentasi & SOP

- [Rule PRD Template](file:///home/inbox/smart-ai/lawyers-hub/rule_prd_template.md):
  Standar penulisan aturan hukum baru.
- [Panduan Audit Trail](file:///home/inbox/smart-ai/lawyers-hub/docs/monitoring/audit_trail_guide.md):
  Monitoring kepatuhan hukum via Grafana/ELK.
- [Template Laporan Deployment](file:///home/inbox/smart-ai/lawyers-hub/docs/deployment/staging_report_template.md):
  Standar pelaporan deployment staging.

## 🏁 Memulai

### Prasyarat

- Node.js >= 18.0.0
- npm >= 9.0.0

### Instalasi

1. Clone repositori ini.
2. Instal dependensi:
   ```bash
   npm install
   ```
3. Salin file environment:
   ```bash
   cp .env.example .env
   ```
4. Isi nilai-nilai di `.env` dengan kredensial yang sesuai.

### Menjalankan Development

Gunakan perintah turbo untuk menjalankan semua aplikasi sekaligus:

```bash
npx turbo dev
```

### Testing

Jalankan semua test di seluruh monorepo:

```bash
npx turbo test
```

## ⚖️ Implementasi Aturan (Rules)

Setiap aturan hukum baru harus mengikuti standar berikut:

1. **Definisi YAML**: Simpan di `.trae/rules/core/` atau `.trae/rules/domains/`.
2. **Metadata**: Sertakan `rule_id`, `priority`, dan `description`.
3. **Validasi**: Gunakan `LegalRulesEngine.evaluateAgentAction()` untuk
   integrasi.

Contoh penambahan aturan baru dapat dilihat di
[.trae/rules/core/privacy.yaml](file:///home/inbox/smart-ai/lawyers-hub/.trae/rules/core/privacy.yaml).

## 📜 Dokumentasi Tambahan

- [Panduan Deployment](_media/DEPLOYMENT.md)
- [Framework Dokumentasi Aturan](docs/Design%20Document:%20Rules%20Documentation%20Framework.md)
- [Panduan Kolaborasi Agent](docs/COLLABORATION.md)

***

*Dikembangkan oleh @WorldClassAgent untuk masa depan hukum digital.*

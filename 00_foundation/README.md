# Lawyers Hub — Foundation README

**Status:** LOCKED – Foundation v1.0 **Tanggal Penguncian:** 2026-01-05
**Pemilik Dokumen:** Product Owner / System Architect

Dokumen ini adalah **fondasi resmi dan tidak berubah** (_non-negotiable
foundation_) untuk seluruh pengembangan, pengambilan keputusan, dan Go-To-Market
platform **Lawyers Hub**.

Semua dokumen lain **HARUS** konsisten dan tidak boleh bertentangan dengan isi
dokumen ini.

---

## 1. Tujuan Dokumen

- Menetapkan **visi, misi, dan ruang lingkup final** Lawyers Hub
- Menjadi _single source of truth_ tingkat tertinggi
- Mengunci prinsip produk, AI, hukum, dan operasional
- Menjadi referensi utama untuk engineering, legal, GTM, dan investor

---

## 2. Visi Lawyers Hub

> **Menjadi platform legal berbasis AI paling terpercaya di Indonesia yang
> memperkuat pengacara dan firma hukum — bukan menggantikannya.**

Lawyers Hub hadir untuk:

- meningkatkan produktivitas profesional hukum
- memperluas akses layanan hukum secara etis
- memastikan penggunaan AI yang patuh hukum, aman, dan bertanggung jawab

---

## 3. Misi

1. Menyediakan **AI assistant legal-grade** yang membantu riset, drafting, dan
   workflow hukum
2. Membangun **legal operating system** untuk lawyer dan firma hukum Indonesia
3. Menjaga **kepatuhan UU PDP, etika profesi, dan auditability AI** sejak desain
   awal
4. Menjadi **hub kolaborasi** antara lawyer, klien, dan komunitas hukum

---

## 4. Ruang Lingkup Platform (Scope)

### 4.1 Termasuk dalam Scope

- Manajemen perkara (case management)
- Drafting & review dokumen hukum
- Legal research berbasis hukum Indonesia
- AI assistant berbasis CopilotKit (assistive only)
- Integrasi komunikasi (WhatsApp, web inbox)
- Multi-tenant law firm workspace
- Audit trail, logging, dan compliance

### 4.2 Di Luar Scope (Explicitly Excluded)

- Pengambilan keputusan hukum final
- Pemberian nasihat hukum final kepada publik
- Representasi klien di pengadilan
- Penandatanganan dokumen hukum otomatis
- AI sebagai pengganti advokat

---

## 5. Prinsip Produk (Product Principles)

1. **Trust > Automation** Setiap fitur harus meningkatkan kepercayaan, bukan
   sekadar otomatisasi.

2. **Assistive AI, Not Autonomous AI** AI membantu manusia, tidak bertindak
   sendiri.

3. **Lawyer-in-the-Loop** Semua output AI berisiko harus direview manusia.

4. **Indonesia-First Legal Context** Hukum Indonesia adalah konteks utama.

5. **Enterprise-Grade from Day One** Security, audit, dan scalability bukan
   fitur tambahan.

---

## 6. Prinsip AI & Etika

- AI **tidak memiliki otoritas hukum**
- Semua prompt dan output AI dapat diaudit
- Data sensitif diminimalkan dan dimask
- Tidak ada AI tanpa governance

AI digunakan sebagai:

---

## 7. Dokumen Terkait

- [System Architecture Overview](../01_architecture/system_overview.md)
- [Core Features Specification](../03_product_features/core_features_spec.md)
- [Prompt Governance](../02_ai_and_rules/prompt_governance.md)
- [User Journey & Interaction Flows](../03_product_features/user_journey_and_flows.md)
- [Analisis & Rencana Implementasi CopilotKit](<Analisis%20&%20Rencana%20Implementasi%20%E2%80%94%20Lawyers-Hub%20%C3%97%20CopilotKit%20(agentic%20+%20UI%20+%20actions%20+%20shared%20state).md>)

---

## 7. Prinsip Arsitektur Teknis

- Modular & domain-driven
- Multi-tenant by design
- API-first
- Event-driven untuk integrasi
- Observable & traceable

Stack utama:

- AG-UI (frontend)
- CopilotKit (AI interaction layer)
- Next.js + NestJS (platform core)
- PostgreSQL + audit log immutable

---

## 8. Prinsip Go-To-Market

- Edukasi pasar sebelum monetisasi
- Pilot & community-driven adoption
- Compliance sebagai keunggulan kompetitif
- AI sebagai value, bukan gimmick

Target awal:

- Individual lawyer
- Small–mid law firm

---

## 9. Stakeholder Kunci

- Product Owner
- Engineering Lead
- AI Governance Lead
- Legal & Compliance Advisor
- GTM & Partnership Lead

---

## 10. Status Penguncian (LOCK POLICY)

- Dokumen ini **tidak boleh diubah** tanpa:
  - persetujuan Product Owner
  - review Legal & AI Governance

- Perubahan besar = versi mayor baru (v2.0)

---

## 11. Versi & Riwayat Perubahan

| Versi | Tanggal    | Catatan            |
| ----- | ---------- | ------------------ |
| 1.0.0 | 2026-01-05 | Foundation dikunci |

---

## 12. Referensi Terkait

- 01_architecture/system_overview.md
- 02_ai_and_rules/prompt_governance.md
- 07_compliance_and_audit/uu_pdp_compliance.md

---

**Dokumen ini adalah kontrak konseptual tertinggi Lawyers Hub.**

# 📋 Corporate Law Rule PRD: [Nama Aturan Korporasi]

| Field | Value |
| :--- | :--- |
| **Rule ID** | [Contoh: CORP-OWN-00X] |
| **Domain** | Corporate Law |
| **Sub-Domain** | [Investment / M&A / Governance / Compliance] |
| **Status** | Draft / Review / Approved |
| **Owner** | [Nama Product Owner] |
| **Legal Reviewer** | [Nama Legal Counsel] |
| **Last Updated** | 2026-01-04 |

---

## 1. Executive Summary
*Jelaskan tujuan aturan korporasi ini (misal: membatasi kepemilikan asing pada sektor tertentu sesuai Daftar Positif Investasi/DPI).*

## 2. Dasar Hukum (Legal Basis)
*Referensi hukum korporasi dan investasi.*
*   **UU/Peraturan**: [Contoh: UU No. 40 Tahun 2007 tentang PT / Perpres No. 10 Tahun 2021 tentang Bidang Usaha Penanaman Modal]
*   **Interpretasi**: [Jelaskan batasan persentase kepemilikan atau syarat modal minimal]
*   **Yurisprudensi/SE**: [Jika ada Surat Edaran atau praktek umum]

## 3. Analisis Risiko (Risk Assessment)
*   **Risiko Hukum**: [Contoh: Penolakan pengesahan Akta oleh Kemenkumham / Pencabutan Izin Usaha]
*   **Risiko Bisnis**: [Contoh: Inefisiensi struktur permodalan]
*   **Mitigasi**: [Contoh: Verifikasi KBLI otomatis sebelum pengisian data pemegang saham]

## 4. Persyaratan Teknis & Logika
### 4.1 Trigger
*   Context: `shareholder_management`
*   Action: `add_shareholder` / `update_equity`

### 4.2 Struktur Data Perusahaan (Corporate Context)
| Variabel | Sumber Data | Tipe Data |
| :--- | :--- | :--- |
| `{{KBLI_CODE}}` | `company.profile.kbli` | String |
| `{{ENTITY_TYPE}}` | `company.profile.type` | Enum (PT_BIASA, PT_PMA) |
| `{{SHAREHOLDER_NATIONALITY}}` | `shareholder.identity.country` | String (ISO Code) |

### 4.3 Kondisi Logika (Logic Conditions)
*   Input Data: KBLI, Persentase Saham, Kewarganegaraan.
*   Logic: `IF KBLI in [LIST_TERBATAS] AND SHAREHOLDER_NATIONALITY != 'ID' AND TOTAL_FOREIGN_PERCENTAGE > [MAX_VAL] THEN BLOCK`

### 4.4 Aksi & Pesan (Actions & Messages)
*   **Action Type**: `BLOCK` / `WARN`
*   **Pesan Kegagalan**: "Pelanggaran Batasan Kepemilikan Asing: Sektor {{KBLI_CODE}} membatasi kepemilikan asing maksimal {{MAX_VAL}}%."

## 5. User Stories & Acceptance Criteria
*   **As a** Corporate Lawyer
*   **I want** sistem memvalidasi struktur kepemilikan saham terhadap KBLI perusahaan
*   **So that** struktur PT tetap sesuai dengan regulasi penanaman modal yang berlaku.

**Acceptance Criteria:**
1.  [ ] Sistem mengenali batasan asing berdasarkan kode KBLI.
2.  [ ] Sistem menghitung total akumulasi saham asing secara real-time.
3.  [ ] Sistem memblokir penambahan pemegang saham jika melampaui ambang batas regulasi.

---
**Approval:**
*   [ ] Product Owner
*   [ ] Legal Counsel (Corporate Specialist)
*   [ ] Compliance Officer

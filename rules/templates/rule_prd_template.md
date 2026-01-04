# 📋 Rule PRD: [Nama Aturan/Fitur]

| Field | Value |
| :--- | :--- |
| **Rule ID** | [Contoh: CORP-CONT-00X] |
| **Domain** | [Contoh: Corporate / Litigation / IP] |
| **Status** | Draft / Review / Approved |
| **Owner** | [Nama Product Owner] |
| **Legal Reviewer** | [Nama Legal Counsel] |
| **Last Updated** | YYYY-MM-DD |

---

## 1. Executive Summary
*Jelaskan secara singkat apa tujuan dari aturan ini dan masalah bisnis yang diselesaikannya.*

## 2. Dasar Hukum (Legal Basis)
*Sebutkan referensi hukum spesifik yang mendasari aturan ini.*
*   **UU/Peraturan**: [Contoh: Pasal 1320 KUHPerdata]
*   **Interpretasi**: [Jelaskan bagaimana pasal ini diterjemahkan menjadi logika sistem]
*   **Yurisprudensi**: [Jika ada putusan pengadilan terkait]

## 3. Analisis Risiko (Risk Assessment)
*Identifikasi risiko jika aturan ini gagal atau salah dieksekusi.*
*   **Risiko Hukum**: [Contoh: Kontrak batal demi hukum]
*   **Risiko Bisnis**: [Contoh: Kerugian reputasi firma]
*   **Mitigasi**: [Contoh: Double-check oleh Compliance Agent]

## 4. Persyaratan Fungsional (Functional Requirements)
### 4.1 Trigger
*Kapan aturan ini harus aktif?*
*   Context: [Contoh: `contract_analysis`]
*   Action: [Contoh: `validate_draft`]

### 4.2 Kondisi (Conditions)
*Logika apa yang harus dipenuhi?*
*   Input Data: [Data apa yang dibutuhkan?]
*   Logic: [Contoh: `IF age < 21 THEN block`]

### 4.3 Aksi (Actions)
*Apa yang dilakukan sistem jika kondisi terpenuhi/gagal?*
*   **Pass**: [Izinkan proses lanjut]
*   **Fail**: [Block / Warn / Flag for Review]
*   **Message**: [Pesan error yang user-friendly]

## 5. User Stories & Acceptance Criteria
*   **As a** [Lawyer]
*   **I want** [Sistem memvalidasi klausul arbitrase otomatis]
*   **So that** [Saya tidak melewatkan syarat formal sengketa]

**Acceptance Criteria:**
1.  [ ] Sistem mendeteksi ketiadaan klausul arbitrase.
2.  [ ] Sistem memberikan peringatan "High Risk".
3.  [ ] Audit log mencatat validasi ini.

---
**Approval:**
*   [ ] Product Owner
*   [ ] Legal Counsel
*   [ ] Compliance Officer

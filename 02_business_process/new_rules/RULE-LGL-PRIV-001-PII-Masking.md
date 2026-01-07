# 📋 Rule PRD: LGL-PRIV-001 - PII Sanitization Requirement

| Field                | Value                     |
| :------------------- | :------------------------ |
| **Rule ID**          | LGL-PRIV-001              |
| **Domain**           | Privacy & Data Protection |
| **Data Sensitivity** | RESTRICTED                |
| **Retention Period** | Permanent (Audit Trail)   |
| **Status**           | Active                    |
| **Last Updated**     | 2026-01-06                |

---

## 1. Konteks Regulasi

- **UU No. 27 Tahun 2022 (UU PDP)**: Kewajiban pengendali data untuk menjaga
  kerahasiaan data pribadi dan melakukan perlindungan teknis.
- **ISO/IEC 27701**: Standar manajemen informasi privasi.
- **Kebijakan Internal Lawyers Hub**: Seluruh data klien yang masuk ke engine AI
  wajib melalui proses anonimisasi atau masking.

## 2. Klasifikasi Data & Privasi

- **Sensitivitas**: Data yang diproses mencakup NIK, Nama Klien, Alamat, dan
  Informasi Keuangan yang dikategorikan sebagai **RESTRICTED**.
- **Masa Retensi**:
  - Log audit penyamaran data: **5 TAHUN**.
  - Metadata masking (untuk proses de-masking oleh authorized user): Sesuai masa
    berlaku kasus.

## 3. Logika Aturan (Logic Engine)

### 3.1 Trigger

- **Context**: `ai_processing` / `document_indexing`
- **Action**: `process_client_data`

### 3.2 Kondisi

```yaml
condition:
  contains_pii: true
  data_source: 'external_upload'
  target_engine: 'llm_external'
```

### 3.3 Pesan Respon (Response Messages)

- **Success (ALLOW)**: "Data berhasil disanitasi. Melanjutkan ke pemrosesan AI."
- **Warning (WARN)**: "Perhatian: Beberapa entitas mungkin tidak terdeteksi
  sempurna. Mohon tinjau hasil masking."
- **Failure (BLOCK)**: "Akses ditolak: Data mengandung PII yang tidak dapat
  disanitasi. Pemrosesan dihentikan untuk keamanan."

## 4. Skenario Pengujian

### Skenario A: Deteksi NIK dalam Kontrak

- **Input**: Dokumen PDF berisi NIK 16 digit.
- **Expected**: Sistem mendeteksi `contains_pii: true`, menerapkan
  `ENFORCE_MASKING`, dan mengganti NIK dengan `[REDACTED]`.

### Skenario B: Pengiriman Data Anonim

- **Input**: Dokumen hukum publik yang tidak mengandung data pribadi.
- **Expected**: Sistem mendeteksi `contains_pii: false`, memberikan akses
  `ALLOW` tanpa masking.

## 5. Implementasi Teknis

- **Metode Masking**: AES-256 (untuk data yang perlu dikembalikan) dan Redaction
  (untuk pemrosesan LLM satu arah).
- **Audit Logging**: Setiap kejadian masking harus dicatat di tabel
  `PIIAuditLog` dengan menyertakan `user_id` dan `timestamp`.

---

Dokumen ini dimigrasikan dari
`.trae/rules/core/privacy_and_security/pii_handling.yaml` sebagai bagian dari
standarisasi dokumentasi v1.1.

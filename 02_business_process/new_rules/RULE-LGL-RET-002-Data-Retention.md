# 📋 Data Retention Rule PRD (UU PDP Compliance)

| Field | Value |
| :--- | :--- |
| **Rule ID** | LGL-RET-002 |
| **Domain** | Privacy & Compliance |
| **Data Sensitivity** | RESTRICTED |
| **Retention Period** | 5 Years (Standard) / Permanent (Litigation) |
| **Status** | Draft |
| **Last Updated** | 2026-01-06 |

---

## 1. Konteks Regulasi

*Aturan ini disusun berdasarkan kepatuhan terhadap:*

- **UU No. 27 Tahun 2022** tentang Pelindungan Data Pribadi (UU PDP).
- **PP No. 71 Tahun 2019** tentang Penyelenggaraan Sistem dan Transaksi
  Elektronik (PSTE).
- **Permenkominfo No. 20 Tahun 2016** tentang Perlindungan Data Pribadi dalam
  Sistem Elektronik.

## 2. Klasifikasi Data & Privasi

- **Sensitivitas**: Data pribadi pengguna dan dokumen hukum yang mengandung
  identitas individu diklasifikasikan sebagai **RESTRICTED**.
- **Masa Retensi**:
  - Data Pribadi Umum: **5 TAHUN** setelah masa keanggotaan/layanan berakhir.
  - Data Litigasi/Kasus Hukum: **PERMANENT** atau sampai kasus dinyatakan selesai
    secara hukum plus 10 tahun.
  - Log Akses Keamanan: **2 TAHUN**.

## 3. Logika Aturan (Logic Engine)

### 3.1 Trigger

- **Context**: `data_lifecycle_management`
- **Action**: `evaluate_retention_policy` / `purge_expired_data`

### 3.2 Kondisi

```yaml
condition:
  data_category:
    in: ["PII", "LEGAL_DOC", "AUDIT_LOG"]
  last_activity_date:
    operator: "<"
    value: "now() - retention_period"
  litigation_hold:
    value: false
  manual_override:
    role: "DATA_PROTECTION_OFFICER"
    allow_extension: true
```

### 3.3 Pesan Respon (Response Messages)

- **Success (ALLOW)**: "Data telah melewati masa retensi dan aman untuk
  dihapus/diarsipkan."
- **Warning (WARN)**: "Data akan segera kedaluwarsa dalam 30 hari. Mohon tinjau
  apakah diperlukan perpanjangan masa retensi (Litigation Hold)."
- **Failure (BLOCK)**: "Penghapusan ditolak: Data berada dalam status 'Litigation
  Hold' atau masa retensi belum tercapai."

## 4. Skenario Penggunaan

### Skenario A: Pembersihan Otomatis Data User Lama

- **Input**: User yang sudah tidak aktif selama 5 tahun 1 hari.
- **Expected**: Sistem memberikan status `ALLOW` untuk penghapusan data pribadi
  sesuai UU PDP.

### Skenario B: Perlindungan Data Kasus Aktif

- **Input**: Dokumen hukum terkait kasus yang masih berjalan (`litigation_hold: true`).
- **Expected**: Sistem memberikan status `BLOCK` meskipun dokumen sudah berusia
  lebih dari 5 tahun.

### Skenario C: Intervensi DPO (Data Protection Officer)

- **Input**: Permintaan penghapusan data oleh user sebelum masa retensi berakhir.
- **Expected**: Sistem memberikan status `BLOCK` secara default, namun DPO dapat
  memberikan `manual_override` jika ada dasar hukum yang kuat (misal: penarikan
  persetujuan/consent).

## 5. Implementasi Teknis

*Implementasi aturan ini dapat ditemukan di:*

- [retention.yaml](file:///home/inbox/smart-ai/lawyers-hub/.trae/rules/domains/retention.yaml)
- [retention_engine.spec.ts](file:///home/inbox/smart-ai/lawyers-hub/packages/rules-engine/test/retention_engine.spec.ts)

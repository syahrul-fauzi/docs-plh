# 📋 Rule PRD: ADV-COMPLEX-001 - Access Control for High-Complexity Advisory

| Field                | Value                        |
| :------------------- | :--------------------------- |
| **Rule ID**          | ADV-COMPLEX-001              |
| **Domain**           | Advisory / Litigation        |
| **Data Sensitivity** | RESTRICTED                   |
| **Retention Period** | Permanent (for Case History) |
| **Status**           | Under Review (Trial Version) |
| **Last Updated**     | 2026-01-06                   |

---

## 1. Konteks Regulasi

- **Kode Etik Advokat Indonesia**: Kerahasiaan hubungan antara advokat dan
  klien.
- **Kebijakan Internal Lawyers Hub**: Pembatasan akses ke dokumen "Complex
  Advisory" hanya untuk partner dan senior associate yang ditugaskan.

## 2. Klasifikasi Data & Privasi

- **Sensitivitas**: Dokumen ini berisi strategi hukum yang sangat rahasia. Akses
  yang tidak sah dapat membahayakan posisi klien dalam litigasi.
- **Masa Retensi**: Data dipertahankan selamanya sebagai bagian dari
  yurisprudensi internal firma.

## 3. Logika Aturan (Logic Engine)

### 3.1 Trigger

- **Context**: `document_access`
- **Action**: `view_case_file`

### 3.2 Kondisi (Logic Fix)

Berdasarkan feedback sebelumnya, logic ini diperbaiki untuk memastikan Partner
selalu memiliki akses, sedangkan Senior Associate memerlukan penugasan
eksplisit.

```yaml
condition:
  case_complexity: 'HIGH'
  user_role:
    in: ['PARTNER', 'SENIOR_ASSOCIATE']
  is_assigned:
    if_role: 'SENIOR_ASSOCIATE'
    required: true
  override_access:
    role: 'PARTNER'
    allow: true
```

## 4. Skenario Penggunaan

### Skenario A: Akses oleh Partner

- **Input**: User dengan role `PARTNER` mencoba membuka file dengan label
  `HIGH_COMPLEXITY`.
- **Expected**: Sistem memberikan akses (`ALLOW`) karena Partner memiliki hak
  akses universal untuk audit dan pengawasan.

### Skenario B: Akses oleh Senior Associate yang Ditugaskan

- **Input**: User `SENIOR_ASSOCIATE` yang terdaftar dalam `assigned_team` pada
  metadata kasus.
- **Expected**: Sistem memberikan akses (`ALLOW`).

### Skenario C: Akses oleh Junior Associate (Unauthorized)

- **Input**: User `JUNIOR_ASSOCIATE` mencoba membuka file.
- **Expected**: Sistem memblokir (`BLOCK`) dan memberikan pesan: "Akses terbatas
  pada Partner dan tim yang ditugaskan."

## 5. Implementasi Teknis & Feedback

- Aturan ini akan diuji di environment `staging` sebelum di-push ke
  `core/rules.yaml`.
- **Feedback Tim Legal**: "Pastikan pesan penolakan menyertakan informasi siapa
  yang harus dihubungi untuk meminta akses." (Akan diupdate di versi 1.1).

---

Dokumen ini dibuat sebagai bagian dari uji coba Rule PRD Template v1.0

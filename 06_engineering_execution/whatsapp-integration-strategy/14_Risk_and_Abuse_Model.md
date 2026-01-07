# 🛡️ 14. Risk and Abuse Model — WhatsApp Integration

## 🎯 1. Overview

Dokumen ini mendefinisikan model ancaman, risiko penyalahgunaan (abuse), dan
strategi mitigasi untuk integrasi WhatsApp di Lawyers-Hub. Mengingat sifat
layanan hukum yang sensitif, perlindungan terhadap spam, penipuan, dan
penyalahgunaan AI sangatlah krusial.

---

## 🚀 2. Threat Modeling (STRIDE)

| Ancaman                     | Deskripsi                                            | Mitigasi                                                               |
| --------------------------- | ---------------------------------------------------- | ---------------------------------------------------------------------- |
| **Spoofing**                | Penyerang berpura-pura menjadi pengacara atau klien. | Verifikasi tanda tangan Webhook Meta, OTP untuk binding nomor telepon. |
| **Tampering**               | Perubahan pesan saat transit atau di database.       | HMAC-SHA256 untuk integritas pesan, Audit Trail immutable.             |
| **Repudiation**             | Pengguna menyangkal telah mengirim pesan hukum.      | Immutable logging dengan timestamp tersertifikasi, Consent Record.     |
| **Information Disclosure**  | Kebocoran data PII klien melalui WhatsApp.           | PII Masking, Enkripsi data at-rest (AES-256), TLS 1.3 in-transit.      |
| **Denial of Service (DoS)** | Bombardir webhook dengan pesan sampah.               | Rate Limiting per-IP, Tenant-specific quotas, Meta IP whitelisting.    |
| **Elevation of Privilege**  | User mengakses data tenant lain via API.             | Row-Level Security (RLS), WABA-to-Tenant mapping strict validation.    |

---

## 🚫 3. Abuse Detection & Prevention

### 3.1 Spam & Bulk Messaging

- **Kriteria:** Pengiriman pesan masif tanpa interaksi user (di luar template
  marketing).
- **Mitigasi:**
  - Batasi jumlah pesan outbound per-menit per-tenant.
  - Deteksi pola pesan berulang yang identik dari inbound.
  - Integrasi dengan WhatsApp Quality Rating API.

### 3.2 AI Hallucination & Misuse

- **Risiko:** AI memberikan saran hukum yang salah atau berbahaya.
- **Mitigasi:**
  - AI Guardrails (Safety Filter) untuk kata kunci sensitif.
  - Disclaimer otomatis pada setiap respon AI.
  - Manual override oleh pengacara manusia.

### 3.3 Social Engineering

- **Risiko:** Penipu menggunakan platform untuk meminta uang atau data pribadi.
- **Mitigasi:**
  - Labeling "Verified Lawyer" untuk akun resmi.
  - Alert sistem jika ada deteksi nomor rekening atau permintaan transfer dalam
    chat yang tidak melalui sistem billing resmi.

---

## 📈 4. Monitoring & Response

### 4.1 Alerting Thresholds

- **Spam Alert:** > 50 pesan inbound dari nomor baru dalam 5 menit.
- **Security Breach:** > 3 kegagalan verifikasi signature berturut-turut.
- **AI Abuse:** > 5 trigger safety filter dalam 1 jam untuk satu user.

### 4.2 Incident Response Plan

1. **Detection:** Alert dipicu ke dashboard admin.
2. **Containment:** Otomatis blokir nomor telepon atau IP yang mencurigakan.
3. **Investigation:** Audit log diperiksa oleh tim security.
4. **Remediation:** Perbaikan celah keamanan atau update blacklist.
5. **Recovery:** Pemulihan layanan dan notifikasi ke pihak terdampak (jika ada
   kebocoran PII).

---

## ⚖️ 5. Compliance & Ethics

- **UU PDP:** Semua deteksi abuse harus menghormati hak privasi subjek data.
- **Etika Profesi:** Tidak ada pemblokiran sepihak tanpa alasan yang sah untuk
  klien yang sedang dalam proses hukum aktif.

---

_Dokumen ini merupakan bagian dari WhatsApp Integration Strategy — Lawyers-Hub._

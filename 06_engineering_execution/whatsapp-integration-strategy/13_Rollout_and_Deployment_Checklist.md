Berikut **13_Rollout_and_Deployment_Checklist.md** yang rapih, lengkap, dan siap
jadi dokumentasi eksekusi untuk _WhatsApp Cloud API integration_ di
_Lawyers-Hub_. Ini mencakup semua pemeriksaan penting dari **pre-deploy →
go-live → post-launch**, termasuk keamanan, webhook, templates, observability,
dan compliance.

---

```markdown
# 📘 13_Rollout_and_Deployment_Checklist.md

## Rollout & Deployment Checklist — WhatsApp Integration

_Version: 1.0 | Last Updated: 2026-01-12_

---

## 🎯 Tujuan Dokumen

Dokumen ini memberikan **daftar langkah terstruktur dan terperinci** yang harus
dilalui sebelum, selama, dan setelah  
_deployment_ integrasi WhatsApp Cloud API di _Lawyers-Hub_ agar:

✔ Sistem stabil saat go-live  
✔ Risiko operasional minimal  
✔ Kepatuhan teknis dan compliance terpenuhi  
✔ Team Engineering & DevOps bisa mengikuti SOP konsisten

---

### 📍 1️⃣ Pre-Deployment (Before Production)

### 🧱 A) Infrastructure & Environment

☑ Server / container siap  
☑ HTTPS / TLS valid & enforced (no HTTP)  
☑ Environment variables set (prod staging dev)  
☑ Webhook URL reachable & not localhost/ngrok only  
☑ Database migrations applied  
☑ Secret management untuk tokens / keys  
☑ **Firewall Whitelisting:** IP ranges resmi Meta sudah di-whitelist di Load
Balancer/WAF. ☑ Capacity Planning (Server CPU/RAM cukup untuk beban puncak)  
☑ **Stress Test:** Webhook Gateway mampu menangani 10x beban normal (spike test)

### 🔐 B) Security & Compliance Hardening

☑ Signature verification implemented  
☑ HMAC secret stored securely  
☑ Rate limiting & IP filtering evaluated  
☑ Token rotation policy defined  
☑ **PDP Compliance:** Pendaftaran PSE (Penyelenggara Sistem Elektronik) dan
sistem manajemen data pribadi telah disetujui tim Legal  
☑ **PII Masking Test:** Verifikasi bahwa data sensitif ter-masking dengan benar
sebelum dikirim ke AI provider  
☑ **LPP Verification:** Verifikasi bahwa data 'Privileged' tidak bocor ke log
atau storage yang tidak aman

---

### 📥 C) WhatsApp Readiness

☑ WhatsApp Business Account approved  
☑ Phone number provisioned & verified  
☑ Meta Business verified (if required)  
☑ Webhook registered & verified with verify token  
☑ Subscribed events: messages, message_status  
☑ Templates created & approved  
☑ **Messaging Tier:** Pantau status limit (Tier 1/2/3) di Meta Business Suite

⚠ Pastikan webhook subscription mencakup semua field yang dibutuhkan,  
termasuk event status (delivered/read). :contentReference[oaicite:2]{index=2}

### 🏢 D) Multi-Tenant Configuration

☑ **WABA-Tenant Mapping:** Verifikasi setiap `WABA_ID` terhubung ke `tenantId`
yang benar di database produksi. ☑ **Tenant Isolation:** Pastikan schema
database per tenant sudah terisolasi (Row-Level Security aktif). ☑ **Billing
Mapping:** Verifikasi kartu kredit/metode pembayaran di Meta Business Suite
sudah terpasang untuk setiap WABA. ☑ **Tenant-Specific Webhooks:** Jika
menggunakan multi-webhook, pastikan routing URL sudah benar.

---

## 📉 1.5 Rollback Plan

Jika terjadi kegagalan kritis setelah deployment:

1. **Infrastructure:** Revert ke image/container version sebelumnya (Blue/Green
   switch).
2. **Database:** Jalankan script migrasi `down` jika skema berubah secara
   breaking.
3. **Webhook:** Segera update Webhook URL di Meta Business Suite jika Gateway
   lama harus digunakan kembali.
4. **Communication:** Informasikan tim support/lawyer bahwa sistem WhatsApp
   dalam pemeliharaan darurat.

---

## 📢 1.6 Communication & Post-Mortem

- **Internal Comm:** Update status di Slack channel `#ops-status`.
- **External Comm:** Jika downtime > 30 menit, tampilkan banner di Dashboard
  Lawyer.
- **Post-Mortem:** Jika terjadi insiden selama rollout, tim wajib melakukan
  blameless post-mortem dalam 48 jam untuk mendokumentasikan root cause dan
  rencana perbaikan permanen.

---

## 📍 2️⃣ Deployment (Go-Live) Tasks

### 🧪 A) Traffic Routing

☑ DNS configured  
☑ Load balancer rules ready  
☑ Zero downtime deployment strategy (blue/green / canary)

---

### 📡 B) Webhook Activation

☑ Gateway endpoint active  
☑ 200 OK returned for initial events  
☑ Webhook verified in Meta dashboard (GET challenge)

⚠️ Ingat: WhatsApp akan **retry webhook** sampai 200 OK dikembalikan.
:contentReference[oaicite:3]{index=3}

---

### 📤 C) Outbound Templates

☑ Approved templates uploaded to Meta  
☑ Template naming consistent & documented  
☑ Parameter placeholders tested

---

### 📊 D) Monitoring & Alerts

☑ Metrics collection active (latency, error rate, queue depth)  
☑ Alerts configured (DLQ high volume, webhook failures)  
☑ Dashboards created (webhook health, outbound delivery)

👉 Monitoring harus aktif **sebelum menerima traffic produksi** supaya  
problem dapat di-detect sejak awal. :contentReference[oaicite:4]{index=4}

---

## 📍 3️⃣ Post-Launch Validation

### 🧪 A) Smoke Tests

☑ Inbound test message received  
☑ Outbound test template sent  
☑ Delivery receipt logged  
☑ Status webhook confirmed

Gunakan tools seperti Postman atau webhook.site untuk memvalidasi  
flow end-to-end sebelum pengguna real masuk.
:contentReference[oaicite:5]{index=5}

---

### 📈 B) SLA Monitoring

☑ Webhook latency within SLO  
☑ Error rates within threshold  
☑ Queue backlog cleared

---

### 📌 C) Compliance Checks

☑ Consent logging verified  
☑ Audit log records flowing  
☑ Data retention policy enforced

---

## 📍 4️⃣ Fallback & Rollback

### 🔄 A) Rollback Plan

☑ Ability to roll back to staging config  
☑ Rollback scripts tested  
☑ Versioned API & config stored in repo

---

### 🚨 B) Fallback Channels

☑ Secondary channel configured (SMS/Email) if WhatsApp fails  
☑ Fallback strategy documented

👉 Banyak sistem enterprise memakai fallback SMS untuk komunikasi kritikal jika
WhatsApp tidak bisa deliver. :contentReference[oaicite:6]{index=6}

---

## 📍 5️⃣ Performance & Scaling

☑ Load/Burst test conducted  
☑ Rate limiting thresholds tested  
☑ Queue workers scaled & auto-scaling enabled  
☑ AI assist throughput evaluated

---

## 📍 6️⃣ Team & Support Readiness

### 📚 A) Training

☑ Engineering on oncall & incident response  
☑ Legal/Support teams briefed on messaging handling & policies

---

### 📞 B) Support Tools

☑ Alert notifications integrated (Slack/PagerDuty)  
☑ Playbooks available for common issues

---

## 📍 7️⃣ Known Risks & Confirmations

☑ Webhook duplicate events workaround in place  
☑ Retry logic verified  
☑ Idempotency ensured  
☑ Temporary token expiry handling implemented

**Catatan:**  
WhatsApp webhook may send repeated ghost pings if 200 OK is not returned. Ensure
dedup logic early in the pipeline. :contentReference[oaicite:7]{index=7}

---

## 📍 8️⃣ Go-Live Approval (Sign-off)

Checklist must be approved by:

- Engineering lead
- Security/Compliance owner
- Product owner
- DevOps/SRE lead

---

## 📌 Deployment Variables Cheat Sheet
```

# WhatsApp

WHATSAPP_API_URL WHATSAPP_ACCESS_TOKEN WHATSAPP_PHONE_NUMBER_ID
WHATSAPP_BUSINESS_ACCOUNT_ID WHATSAPP_WEBHOOK_VERIFY_TOKEN

# Infrastructure

NODE_ENV=production WEBHOOK_SECRET_KEY RATE_LIMIT_CONFIG

```

---

## 🧾 Post-Launch Audit & Maintenance

- Monthly webhook subscription validation
- Template re-approval checks
- Security token rotation
- Periodic penetration testing

---

## 🧩 Summary

Checklist ini memastikan **deployment WhatsApp integration dapat dilakukan dengan aman, terukur, dan stabil** dari pre-deploy sampai post-launch.
Tujuannya: **zero downtime**, **compliance**, **observability**, dan **resilience** di platform.

---

## 📎 Referensi

- Pre-launch checklist (infrastructure + webhook) :contentReference[oaicite:8]{index=8}
- WhatsApp integration best practices (security, testing, monitoring) :contentReference[oaicite:9]{index=9}
- Meta webhook retry pattern & dedup behavior (community feedback) :contentReference[oaicite:10]{index=10}

```

---

Daftar ini jadi **kontrak operasional** bagi tim engineering & DevOps saat Anda
menjalankan integrasi WhatsApp ke produksi. Siap lanjut ke
**14_Risk_and_Abuse_Model.md** jika Anda ketik “lanjut”.

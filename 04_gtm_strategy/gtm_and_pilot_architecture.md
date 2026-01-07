# Go-To-Market (GTM) & Pilot Conversion Architecture — Lawyers Hub `\home\inbox\smart-ai\lawyers-hub\docs\04_gtm_strategy\gtm_and_pilot_architecture.md`

## Metadata

- **Document ID**: LH-GTM-ARCH-001
- **Status**: Draft v0.1 (Post-Lock v1.0)
- **Owner**: GTM Lead / Product Strategy
- **Stakeholders**: Founders, Sales, Legal Ops, Engineering, AI
- **Derived From**:
  [README.md](file:///home/inbox/smart-ai/lawyers-hub/docs/00_foundation/README.md),
  [system_overview.md](file:///home/inbox/smart-ai/lawyers-hub/docs/01_architecture/system_overview.md),
  [core_features_spec.md](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/core_features_spec.md),
  [prompt_governance.md](file:///home/inbox/smart-ai/lawyers-hub/docs/02_ai_and_rules/prompt_governance.md),
  [user_journey_and_flows.md](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/user_journey_and_flows.md)

---

## 1. Tujuan Dokumen

Mendefinisikan **arsitektur Go-To-Market (GTM)** Lawyers Hub secara operasional
dan teknis untuk:

- Akuisisi pengguna awal (pilot & early adopters)
- Konversi trial → paid
- Menjaga kepatuhan legal & AI selama proses penjualan

Dokumen ini menjadi penghubung antara **produk, sales, dan implementasi
teknis**.

---

## 2. Target Market & ICP (Initial)

### 2.1 Primary ICP (Pilot Phase)

- Firma hukum kecil–menengah (2–20 lawyer)
- Boutique law firm (corporate, compliance, litigation ringan)
- Legal in-house UMKM / startup

### 2.2 Secondary ICP

- Paralegal services
- Legal consultant (non-litigasi)

---

## 3. GTM Phases

### Phase 1 — Closed Pilot

**Tujuan**:

- Validasi produk
- Validasi AI trust
- Validasi workflow

**Ciri**:

- Invitation-only
- White-glove onboarding
- Direct feedback loop

---

### Phase 2 — Public Beta

**Tujuan**:

- Scale onboarding
- Validate pricing
- Marketing activation

**Ciri**:

- Self-serve signup
- Limited AI quota
- Feature gating

---

### Phase 3 — Commercial Launch

**Tujuan**:

- Monetisasi penuh
- Partnership

---

## 4. Pilot Architecture (Technical)

### 4.1 Demo / Sandbox Mode

**Fungsi**:

- Sales demo
- Investor demo

**Karakteristik**:

- Dummy data
- AI restricted
- No real client data

**AG-UI State**:

- `workspace.demo`

---

### 4.2 Pilot Tenant

**Fitur**:

- Real data
- Limited users
- Enhanced audit

**Restrictions**:

- No production billing
- AI quota capped

---

## 5. Onboarding Conversion Flow

### 5.1 Sales-Assisted Onboarding

1. Lead qualification
2. Demo workspace
3. Pilot tenant creation
4. Training & activation

### 5.2 Self-Serve Onboarding (Beta)

1. Signup
2. Verification
3. Trial start

---

## 6. Pricing & Packaging (Initial)

### Models

- Per-seat (lawyer)
- AI usage add-on
- Case volume tier

### Pilot Incentive

- Discounted rate
- Extended trial

---

## 7. Metrics & KPIs

### Activation

- Time to first case
- Time to first AI usage

### Engagement

- DAU / MAU (lawyer)
- AI interaction per case

### Conversion

- Trial → paid
- Pilot → contract

---

## 8. Compliance & Risk Control (GTM)

- No AI legal advice marketing claim
- Explicit AI disclaimer in sales material
- Consent during onboarding

---

## 9. GTM Tooling Integration

- CRM (HubSpot / custom)
- Product analytics
- Audit dashboard

---

## 10. Out of Scope

- Open marketplace
- Revenue sharing v1

---

## 11. Dokumen Terkait

- [Core Features Spec](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/core_features_spec.md)
- [User Journey](file:///home/inbox/smart-ai/lawyers-hub/docs/03_product_features/user_journey_and_flows.md)
- [Deployment Docs](file:///home/inbox/smart-ai/lawyers-hub/docs/deployment/DEPLOYMENT.md)

---

## 12. Status

🚧 **Draft — Ready for GTM review & lock**

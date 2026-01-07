# Strategi Integrasi WhatsApp - Lawyers Hub

**Status:** DRAFT v1.0 **Tanggal:** 2026-01-06 **Referensi:** Foundation v1.0

## 1. Pendahuluan

Dokumen ini menguraikan strategi komprehensif untuk mengintegrasikan WhatsApp
Business API ke dalam platform Lawyers Hub. Strategi ini dirancang untuk
mematuhi prinsip "Lawyer-in-the-Loop", memastikan keamanan data (UU PDP & GDPR),
dan memanfaatkan pembaruan terbaru API WhatsApp 2025 (pricing & policy).

## 2. Prinsip Utama

Sesuai dengan `docs/00_foundation/README.md`:

1. **Assistive, Not Autonomous**: WhatsApp bot bertindak sebagai resepsionis
    cerdas (intake, scheduling, basic FAQ), BUKAN penasehat hukum.
2. **Trust & Security**: Enkripsi end-to-end dipertahankan dari sisi user ke
    Meta, dengan enkripsi tambahan dan audit trail penuh di sisi server Lawyers
    Hub.
3. **Scalability**: Arsitektur event-driven untuk menangani volume pesan tinggi
    tanpa blocking.
4. **Compliance First**: Mekanisme opt-in eksplisit dan data minimization untuk
    melindungi privasi klien.

## 3. Daftar Isi Dokumentasi

Strategi ini dipecah menjadi dokumen-dokumen berikut:

- **[01_Arsitektur_Teknis_WhatsApp_End-to-End.md](./01_Arsitektur_Teknis_WhatsApp_End-to-End.md)**:
  Gambaran arsitektur sistem, keamanan, dan aliran data.
- **[02_Diagram_Sequence_Inbound_Outbound.md](./02_Diagram_Sequence_Inbound_Outbound.md)**:
  Diagram alur pesan masuk dan keluar.
- **[03_WhatsApp_Gateway_Blueprint.md](./03_WhatsApp_Gateway_Blueprint.md)**:
  Spesifikasi teknis Gateway Service (NestJS).
- **[04_Message_Ingestor_and_Normalization.md](./04_Message_Ingestor_and_Normalization.md)**:
  Standardisasi format pesan (text, media, location).
- **[05_Event_Bus_and_Async_Workflow.md](./05_Event_Bus_and_Async_Workflow.md)**:
  Pengelolaan antrian dan pemrosesan asinkron.
- **[06_AI_Assist_Integration_Policy.md](./06_AI_Assist_Integration_Policy.md)**:
  Kebijakan penggunaan AI (CopilotKit) dalam percakapan WhatsApp.
- **[07_Intake_PreCase_Workflow.md](./07_Intake_PreCase_Workflow.md)**: Alur
  kerja spesifik untuk pendaftaran klien baru (Pre-Case).

## 4. Kepatuhan Regulasi & Pembaruan API 2025-2026

- **Pricing Update (2025)**:
  - **Service Conversations**: 1.000 percakapan pertama per bulan gratis.
    Setelah itu dikenakan biaya per percakapan (24-hour window).
  - **Utility & Authentication**: Fokus pada efisiensi biaya dengan template
    yang tepat.
- **Meta AI Policy 2026**:
  - **Strict Task-Oriented AI**: Larangan keras terhadap chatbot AI umum. AI di
    Lawyers Hub difokuskan pada _Business Flow_ (Intake, Scheduling, Case
    Status).
  - **Explicit Disclosure**: Kewajiban transparansi penggunaan AI kepada
    pengguna.
- **GDPR & UU PDP**:
  - **Explicit Opt-in**: Wajib sebelum pengiriman pesan template.
  - **Data Minimization**: Penggunaan Presigned URL untuk media (S3) dan
    enkripsi kolom AES-256 untuk data chat.
  - **Right to be Forgotten**: Implementasi endpoint penghapusan data otomatis.

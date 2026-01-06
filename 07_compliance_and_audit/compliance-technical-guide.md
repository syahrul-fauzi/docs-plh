# Compliance & PII Review System Documentation

## Overview
Sistem ini dirancang untuk menangani deteksi PII (Personally Identifiable Information) hibrida (Regex + NER), menyediakan antarmuka Human Review untuk verifikasi, dan mekanisme sinkronisasi otomatis untuk retraining model AI berdasarkan feedback manusia.

## Arsitektur Teknis

### 1. Database Schema (`ComplianceReview`)
Tabel `compliance_reviews` menyimpan hasil review dari dashboard admin:
- `id`: UUID unik.
- `piiType`: Jenis entitas (misal: PERSON, NIK, PHONE).
- `originalValue`: Nilai asli yang dideteksi.
- `correctedValue`: Koreksi dari reviewer (jika ada).
- `confidenceScore`: Skor kepercayaan dari model asli.
- `status`: `VERIFIED` (benar) atau `FALSE_POSITIVE` (salah deteksi).
- `isProcessed`: Flag untuk menandai apakah data sudah dikirim ke pipeline retraining.

### 2. API Endpoints
- `POST /compliance/review`: Menyimpan hasil review baru.
- `GET /compliance/reviews`: Mengambil daftar review untuk tenant saat ini.
- `GET /compliance/export/pdf`: Ekspor laporan kepatuhan dalam format PDF.
- `GET /compliance/export/csv`: Ekspor data review dalam format CSV.

### 3. Pipeline Retraining
Mekanisme sinkronisasi menggunakan **BullMQ** dan **NestJS Schedule**:
- **Scheduler**: `ComplianceScheduler` memicu job `compliance-retraining` setiap tengah malam.
- **Processor**: `ComplianceProcessor` mengambil semua record `VERIFIED` yang belum diproses, mensimulasikan sinkronisasi ke pipeline AI (misal: SageMaker/HuggingFace), dan menandainya sebagai `isProcessed`.
- **Audit**: Setiap proses retraining dicatat di `AuditLog` untuk kebutuhan audit kepatuhan.

## Prosedur Audit Compliance (GDPR & UU PDP)

### Integritas Data
- Semua ekspor laporan menyertakan timestamp dan informasi tenant.
- Metadata audit disimpan secara terenkripsi di database.
- Akses ke fitur ekspor dibatasi melalui RBAC (Role-Based Access Control) - hanya `FIRM_ADMIN` dan `SUPER_ADMIN`.

### Alur Audit Eksternal
1. Auditor meminta laporan kepatuhan untuk periode tertentu.
2. Admin mengunduh laporan melalui dashboard menggunakan filter tanggal.
3. Laporan menyertakan ringkasan deteksi PII, tindakan yang diambil (Masking/Blocking), dan hasil verifikasi manusia.
4. Log audit dapat digunakan untuk memverifikasi siapa yang melakukan review dan kapan retraining model dilakukan.

## Monitoring
Monitoring proses retraining dapat dipantau melalui:
- **NestJS Logger**: Log level `INFO` dan `DEBUG` di `ComplianceProcessor`.
- **Audit Dashboard**: Mencari aksi `COMPLIANCE_RETRAINING_SYNC`.
- **Database**: Memeriksa jumlah record dengan `isProcessed: false`.

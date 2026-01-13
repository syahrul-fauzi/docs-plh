# Blueprint Pengembangan Mobile App Pengacara

**(lawyers-apps – Expo / React Native)**

## 1. Ringkasan Eksekutif

Aplikasi **Lawyers Mobile** adalah aplikasi mobile lintas platform (iOS &
Android) berbasis **Expo (React Native + TypeScript)** yang dirancang khusus
untuk:

- Pengacara individu
- Firma hukum
- Legal assistant / paralegal
- Konsultan hukum internal (in-house)

Tujuan utama aplikasi:

- Manajemen perkara (case lifecycle)
- Manajemen dokumen hukum secara aman
- Produktivitas pengacara (agenda sidang, deadline, catatan hukum)
- Akses cepat dan aman ke data hukum kapan pun

Aplikasi dibangun dengan prinsip:

- **Clean Architecture**
- **Type-safe**
- **Secure-by-design**
- **Offline-first (terbatas)**
- **Scalable untuk SaaS multi-tenant**

---

## 2. Tech Stack & Alasan Pemilihan

### Core Framework

- **Expo (Managed Workflow)**
- **React Native + TypeScript**

> Expo dipilih karena:
>
> - Cepat untuk pengembangan
> - SDK lengkap (document picker, secure store, camera, notifications)
> - Build iOS & Android terintegrasi (EAS)
> - Cocok untuk tim kecil–menengah dan SaaS MVP → production

---

### Navigation

- **React Navigation (Native Stack + Bottom Tabs)**

Alasan:

- Stabil
- Mature
- Type-safe
- Cocok untuk flow kompleks (auth → dashboard → detail kasus)

---

### State Management

Rekomendasi utama:

- **Redux Toolkit + RTK Query**

Digunakan untuk:

- Auth state
- Daftar kasus
- Dokumen
- Sinkronisasi API
- Cache & invalidation otomatis

> UI state kecil (modal, toggle) boleh menggunakan hook lokal atau Zustand.

---

### File & Document Handling

- `expo-document-picker`
- `expo-file-system`
- `expo-camera` (scan dokumen)
- PDF viewer (WebView / native)

Digunakan untuk:

- Upload dokumen perkara
- Scan dokumen fisik
- Download & preview dokumen
- Offline read (encrypted)

---

### Security

- `expo-secure-store`
- Token JWT / OAuth
- Enkripsi file lokal
- Role-based access (ditangani backend)

---

### Build & Release

- **EAS Build**
- **EAS Submit**
- Konfigurasi terpisah: staging & production

---

## 3. Struktur Direktori (`apps/mobile`)

```
apps/mobile/
├─ app.json
├─ eas.json
├─ package.json
├─ tsconfig.json
├─ src/
│  ├─ assets/
│  ├─ components/        # UI kecil reusable
│  ├─ screens/
│  │  ├─ auth/
│  │  ├─ dashboard/
│  │  ├─ cases/
│  │  ├─ case-details/
│  │  ├─ documents/
│  │  ├─ calendar/
│  │  └─ settings/
│  ├─ navigation/
│  │  ├─ index.tsx
│  │  └─ types.ts
│  ├─ features/          # Redux slices (case, document, user)
│  ├─ services/          # API, upload, secure storage
│  ├─ hooks/
│  ├─ utils/
│  ├─ constants/
│  ├─ types/
│  └─ tests/
│     ├─ unit/
│     └─ integration/
├─ e2e/
└─ README.md
```

---

## 4. Use Case Terbaik (Best Use Cases)

### Use Case 1 — Manajemen Perkara (Core)

**Aktor:** Pengacara **Alur:**

1. Login
2. Melihat daftar perkara aktif
3. Filter berdasarkan:
   - Klien
   - Status (aktif, sidang, selesai)
   - Jenis perkara

4. Masuk ke detail perkara
5. Akses:
   - Ringkasan
   - Timeline
   - Dokumen
   - Catatan hukum

**Nilai bisnis:**

- Semua informasi perkara terpusat
- Mengurangi ketergantungan spreadsheet / WhatsApp

---

### Use Case 2 — Manajemen Dokumen Hukum

**Aktor:** Pengacara / Paralegal **Alur:**

1. Upload dokumen (PDF, Word, scan kamera)
2. Otomatis terhubung ke perkara
3. Preview dokumen
4. Download / share (izin terbatas)
5. Offline read (read-only)

**Fitur penting:**

- Metadata dokumen
- Versi dokumen
- Audit trail (siapa upload / akses)

---

### Use Case 3 — Agenda Sidang & Deadline

**Aktor:** Pengacara **Alur:**

1. Kalender terintegrasi
2. Reminder sidang
3. Deadline dokumen
4. Push notification

**Nilai:**

- Menghindari missed deadline
- Produktivitas meningkat

---

### Use Case 4 — Catatan & Analisis Kasus

**Aktor:** Pengacara **Alur:**

1. Menulis catatan pribadi per perkara
2. Tidak terlihat klien
3. Sinkronisasi aman

---

### Use Case 5 — Mode Offline (Terbatas)

**Aktor:** Pengacara di lapangan **Alur:**

1. Dokumen yang pernah dibuka tersimpan encrypted
2. Bisa dibaca tanpa koneksi
3. Sinkronisasi ulang saat online

---

## 5. Navigasi Aplikasi (Contoh)

```
Auth
 └─ Dashboard
     ├─ Kasus
     │   └─ Detail Kasus
     │       ├─ Ringkasan
     │       ├─ Dokumen
     │       └─ Catatan
     ├─ Kalender
     ├─ Dokumen
     └─ Pengaturan
```

---

## 6. Error Handling & Observability

### Error Handling

- Try/catch di semua async action
- UI error state (retry)
- Network error fallback

### Logging

- Client-side logging
- Error tracking (Sentry)
- Performance metrics (upload time, API latency)

---

## 7. Testing Strategy

### Unit Test

- Komponen UI
- Redux slices
- Utility functions

### Integration Test

- Flow:
  - Login → dashboard
  - Case list → case detail
  - Upload dokumen

### End-to-End (E2E)

- Login
- Buka perkara
- Upload dokumen
- Logout

### Performance Test

- Cold start
- Document open time
- Memory usage

---

## 8. Build & CI/CD

### Build

- `eas build -p android`
- `eas build -p ios`

### CI Pipeline (rekomendasi)

1. Install dependencies
2. Type check
3. Unit test
4. Integration test
5. EAS build

---

## 9. Dokumentasi Wajib

File `apps/mobile/README.md` harus mencakup:

- Setup environment
- Cara menjalankan di device
- Build iOS & Android
- Struktur arsitektur
- Testing guide
- Security guideline
- Upgrade Expo SDK

---

## 10. Checklist Deliverables

✅ Aplikasi Expo (TypeScript) ✅ Struktur modular & scalable ✅ Manajemen
perkara & dokumen ✅ Navigation & state management rapi ✅ Error handling &
logging ✅ Unit, integration, E2E test ✅ Build config iOS & Android ✅
Dokumentasi lengkap

# Laporan Analisis Arsitektur Hybrid (Phase 1 Beta)

**Tanggal:** 2026-01-15
**Status:** Draft / Parallel Beta
**Referensi:** `PHASE_1_BETA_GUIDE.md`, `middleware.ts`, `api.ts`

## 1. Ringkasan Eksekutif
Dokumen ini menyajikan hasil analisis terhadap implementasi arsitektur routing hybrid (Subdomain + URL-based) di Lawyers Hub. Analisis mencakup tinjauan kode internal, perbandingan dengan praktik terbaik industri (Industry Best Practices), dan evaluasi risiko keamanan serta performa.

Temuan utama menunjukkan bahwa transisi ke **Path-based Routing** (`/tenant-id/...`) sejalan dengan tren modern SaaS untuk penyederhanaan infrastruktur dan otorisasi, namun memerlukan penanganan konteks (Context Propagation) yang ketat di sisi klien dan server.

## 2. Analisis Implementasi Internal

### 2.1 Mekanisme Dual-Routing (Middleware)
Sistem saat ini menggunakan `apps/web/src/middleware.ts` untuk mendeteksi konteks tenant melalui dua jalur:
1.  **Legacy (Subdomain):** Mengekstrak `subdomain` dari header `Host`.
2.  **Modern (URL Path):** Mengekstrak segmen ke-2 dari URL path (`/:locale/:tenantId/...`).

**Insight:** Pendekatan ini memungkinkan koeksistensi tanpa downtime. Middleware bertindak sebagai "Traffic Controller" yang menormalisasi kedua input menjadi satu header standar `x-tenant-id` yang dikonsumsi oleh API.

### 2.2 Client-Side Context Propagation (`api.ts`)
Tantangan utama dalam migrasi ke URL-based adalah hilangnya konteks implisit (cookie/subdomain) pada request `fetch` di sisi klien.
*   **Solusi Diterapkan:** *Smart Fallback Injection*. Wrapper `fetchApi` di `api.ts` secara otomatis mendeteksi `tenantId` dari `window.location.pathname` jika header `x-tenant-id` belum tersedia.
*   **Keunggulan:** Menghindari refactoring masif pada ratusan komponen React yang memanggil API.
*   **Risiko:** Ketergantungan tinggi pada struktur URL yang konsisten (`/:locale/:tenantId`). Perubahan struktur URL di masa depan harus menyertakan update pada logika ini.

### 2.3 Telemetri & Observabilitas
Implementasi logging terstruktur di middleware (`PHASE_1_ROUTING` event) memberikan visibilitas real-time terhadap adopsi rute baru vs lama. Ini krusial untuk memutuskan kapan "Legacy Route" dapat dimatikan sepenuhnya.

## 3. Komparasi dengan Praktik Terbaik Industri (External Search)

Berdasarkan penelusuran referensi teknis (Vercel, AWS SaaS Factory, Studi Kasus Migrasi):

| Aspek | Subdomain (Legacy) | Path-based (Modern) | Temuan & Rekomendasi |
|-------|-------------------|---------------------|----------------------|
| **SEO** | Otoritas domain terpecah. Bagus untuk isolasi konten total. | Otoritas terkonsolidasi. Lebih baik untuk SEO global. | **Validasi:** Pindah ke Path-based menguntungkan branding Lawyers Hub jangka panjang. |
| **Auth & Cookies** | Rumit (Wildcard Cookies, Cross-site issues). | Sederhana (Same-origin cookies). | **Insight:** Path-based menghilangkan kompleksitas manajemen session lintas subdomain. |
| **Infrastruktur** | Membutuhkan Wildcard SSL & DNS management. | Standar SSL, tidak perlu konfigurasi DNS per tenant. | **Efisiensi:** Mengurangi biaya operasional dan kompleksitas sertifikat SSL. |
| **Caching (CDN)** | Cache key berdasarkan Hostname. | Cache key berdasarkan URL Path. | **Performa:** Modern CDN lebih optimal menangani path-based purging/caching. |

**Kesimpulan:** Langkah Lawyers Hub menuju Path-based Routing (`/:tenantId`) adalah langkah yang tepat dan valid secara teknis (Industry Standard).

## 4. Identifikasi Risiko & Mitigasi

### 4.1 Risiko Keamanan (Cross-Tenant Access)
*   **Isu:** Pada model URL-based, pengguna dapat dengan mudah memanipulasi URL dari `/tenant-A/` ke `/tenant-B/`.
*   **Mitigasi Saat Ini:** Middleware menyuntikkan `x-tenant-id`.
*   **Rekomendasi Kritis:** Pastikan **Row Level Security (RLS)** di database dan **Guard** di NestJS memvalidasi bahwa `user_id` yang sedang login *memiliki izin akses* ke `tenant_id` yang dikirim di header. Jangan hanya mempercayai header semata.

### 4.2 Konsistensi Data Frontend
*   **Isu:** Perpindahan antar tenant dalam satu sesi browser (SPA navigation) bisa menyisakan "stale state" (state lama) di React Query atau Context.
*   **Rekomendasi:** Pastikan `key` pada provider React Query menyertakan `tenantId` agar cache otomatis di-invalidate saat pengguna berpindah tenant.

## 5. Rekomendasi Langkah Selanjutnya

1.  **Security Audit (Backend):** Lakukan audit pada `apps/api` untuk memastikan setiap endpoint memverifikasi relasi `User <-> Tenant` sebelum mengeksekusi query, bukan hanya mengandalkan keberadaan header `x-tenant-id`.
2.  **React Query Cache Busting:** Tambahkan `tenantId` sebagai bagian dari query key global di konfigurasi React Query.
3.  **Deployment Staging:** Deploy kode saat ini ke lingkungan Staging untuk mulai mengumpulkan data telemetri riil sesuai rencana `PHASE_1_BETA_GUIDE.md`.

---
*Dokumen ini disusun oleh AI Assistant sebagai bagian dari fase analisis migrasi arsitektur.*

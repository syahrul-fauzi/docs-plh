# Laporan Audit Keamanan Backend & Rekomendasi

**Tanggal:** 2026-01-15
**Auditor:** AI Assistant (Trae IDE)
**Scope:** `apps/api` (AuthGuard, TenantGuard)

## 1. Temuan Kritis (Critical Findings)

### 1.1 Insecure Context Propagation via Header (Fixed)
*   **Deskripsi:** `AuthGuard` sebelumnya mempercayai header `x-tenant-id` untuk memperbarui kolom `tenantId` pengguna di database.
*   **Risiko:** Pengguna dengan token valid (tanpa klaim tenant) dapat mengirim header `x-tenant-id: target-tenant` dan secara efektif "memindahkan" akun mereka ke tenant target, mendapatkan akses penuh.
*   **Status:** **FIXED**.
*   **Tindakan Perbaikan:**
    *   Memodifikasi `AuthGuard` untuk *hanya* menggunakan `tenantId` dari payload token JWT/Clerk sebagai sumber kebenaran (Source of Truth).
    *   Menghapus logika auto-update `user.tenantId` di database berdasarkan header request.

### 1.2 Missing Tenant Context Validation (Fixed)
*   **Deskripsi:** `TenantGuard` sebelumnya mengizinkan akses (return `true`) jika `request.user.tenantId` tidak ada (undefined), dengan asumsi pengguna tersebut adalah "Global User" atau belum terautentikasi (diserahkan ke AuthGuard).
*   **Risiko:** Pengguna yang berhasil login tetapi tidak memiliki `tenantId` (misal: miskonfigurasi) dapat mengakses resource tenant manapun karena Guard melewati pemeriksaan.
*   **Status:** **FIXED**.
*   **Tindakan Perbaikan:**
    *   Memodifikasi `TenantGuard` untuk memblokir akses (`ForbiddenException`) jika `user.tenantId` kosong TETAPI request menargetkan tenant spesifik (via body/query/params).
    *   Pengecualian diberikan hanya untuk role `ADMIN` dan `SUPER_ADMIN`.

## 2. Verifikasi & Pengujian
Unit test baru telah ditambahkan di `apps/api/src/auth/guards/tenant.guard.spec.ts` untuk memvalidasi skenario berikut:
1.  **Global Admin Bypass:** Sukses.
2.  **User No-Tenant Accessing Tenant Resource:** Blocked (Forbidden).
3.  **Cross-Tenant Access (Tenant A -> Tenant B):** Blocked (Forbidden).
4.  **Valid Tenant Access (Tenant A -> Tenant A):** Allowed.

## 3. Rekomendasi Lanjutan
1.  **Token Claims:** Pastikan semua JWT yang diterbitkan oleh Auth Service (Clerk/Internal) selalu menyertakan klaim `tenantId` untuk pengguna non-global.
2.  **Regular Audit:** Lakukan audit serupa pada `guards` lain seperti `RolesGuard` dan `FeatureGuard`.

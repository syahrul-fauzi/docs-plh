# Mapping Type Safety: Backend DTOs to Frontend Interfaces

Dokumen ini menjelaskan pemetaan antara Data Transfer Objects (DTO) di backend (NestJS) dan interface di frontend (Next.js) untuk memastikan konsistensi tipe data di seluruh aplikasi.

## Case (Perkara)

### Backend Entity (Domain)
Interface: `Case`
File: `packages/domain/src/entities/case.entity.ts`

```typescript
export interface Case {
  id: string;
  title: string;
  description?: string;
  status: 'OPEN' | 'CLOSED' | 'ARCHIVED';
  tenantId: string;
  clientId?: string;
  lawyerId?: string;
  createdAt: Date;
  updatedAt: Date;
  _count?: {
    documents: number;
  };
}
```

### Backend DTOs
File: `apps/api/src/cases/dto/case.dto.ts` (Uses Zod schemas from `@lawyers-hub/core`)

| DTO Name | Base Interface | Fields |
|----------|----------------|--------|
| `CreateCaseDto` | `CreateCase` | `title`, `description?`, `status?`, `clientId?` |
| `UpdateCaseDto` | `UpdateCase` | `title?`, `description?`, `status?` |

### Frontend Interfaces
File: `apps/web/src/features/cases/ui/CaseList.tsx`

```typescript
interface CaseUI extends Case {
  _count?: {
    documents: number;
  };
}
```

## Sinkronisasi & Validasi

1. **Validasi Schema**: Backend menggunakan `ZodValidationPipe` dengan schema yang didefinisikan di `packages/core/src/validation.ts`. Schema ini dibagi (shared) antara frontend dan backend untuk memastikan aturan validasi yang sama.
2. **Transformasi Data**: `PrismaCaseRepository` bertanggung jawab untuk melakukan mapping dari Prisma model ke domain `Case` entity, termasuk dekripsi data sensitif (deskripsi) dan penyertaan metadata seperti `_count`.
3. **Strict Typing**: Penggunaan `any` telah dihilangkan dari komponen utama `CaseList.tsx` dan digantikan dengan `CaseUI` untuk dukungan IntelliSense yang lebih baik dan pencegahan error saat kompilasi.

## Rekomendasi Pengembangan Mendalam

- Selalu gunakan shared schema dari `@lawyers-hub/core` untuk validasi form di frontend.
- Pastikan setiap penambahan field baru di database tercermin di `Case` entity (Domain) dan dipetakan dengan benar di repository.

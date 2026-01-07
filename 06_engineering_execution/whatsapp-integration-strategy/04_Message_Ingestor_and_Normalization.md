# Message Ingestor & Normalization Strategy

## 1. Tantangan

Payload Webhook WhatsApp sangat nested dan bervariasi tergantung tipe pesan
(text, image, location, interactive, system). Kita perlu menormalisasi ini
menjadi format internal yang konsisten agar mudah dikonsumsi oleh Core Service
dan AI.

## 2. Schema Internal (`NormalizedMessage`)

Setiap pesan yang masuk harus dikonversi ke struktur ini sebelum masuk ke Core
Logic:

```typescript
interface NormalizedMessage {
  id: string; // Internal UUID (v4)
  tenantId: string; // Law Firm ID (Mapping from Phone Number ID)
  wamid: string; // WhatsApp Message ID (wamid.HBgM...)
  from: string; // E.164 format (+62812...)
  to: string; // Business Phone Number
  timestamp: Date; // ISO 8601
  type:
    | 'text'
    | 'image'
    | 'document'
    | 'location'
    | 'interactive'
    | 'flow'
    | 'system';
  content: {
    text?: string; // Isi pesan teks atau caption
    mediaUrl?: string; // Internal URL (S3) setelah download
    mimeType?: string;
    latitude?: number;
    longitude?: number;
    actionId?: string; // Untuk button/list reply
    flowData?: object; // Data hasil WhatsApp Flow (v22.0)
  };
  metadata: {
    userName: string; // Nama profil pengirim
    isForwarded: boolean;
    replyToMessageId?: string; // Context threading
  };
}
```

## 3. Strategi Normalisasi

### 3.1 Tenant Mapping

- **Source**: `metadata.display_phone_number` atau `PHONE_NUMBER_ID` dari
  payload webhook.
- **Action**: Look up `tenantId` dari Redis/DB. Jika tidak ditemukan, log
  sebagai `UNAUTHORIZED_SOURCE` dan drop pesan (security measure).

### 3.2 Phone Number

- WhatsApp API mengirim format tanpa `+` (misal: `62812345`).
- **Rule**: Tambahkan `+` jika belum ada. Pastikan selalu format E.164.

### 3.3 Text & Flow Extraction

- **Text Message**: Ambil `entry[0].changes[0].value.messages[0].text.body`.
- **Interactive Button**: Ambil `interactive.button_reply.id` (untuk logic) dan
  `title` (untuk display).
- **Interactive List**: Ambil `interactive.list_reply.id`.
- **WhatsApp Flows (v22.0)**: Ambil
  `messages[0].interactive.nfm_reply.response_json` untuk mendapatkan data
  intake terstruktur.

### 3.3 Media Handling

- Jangan simpan binary di Database.
- Ingestor service bertanggung jawab mendownload media dari Meta, upload ke S3
  (Private), dan hanya menyimpan URL S3 di field `content.mediaUrl`.
- **Security**: Strip metadata (EXIF) dari gambar jika memungkinkan untuk
  privasi user.

### 3.4 Deduplikasi

- Gunakan `wamid` sebagai key untuk idempotency.
- Jika `wamid` sudah ada di Redis/DB dalam 24 jam terakhir, abaikan pesan
  (return 200 OK) untuk mencegah double-processing jika Meta melakukan retry
  webhook.

# WhatsApp Gateway Blueprint

## 1. Teknologi Stack

- **Framework**: NestJS (Node.js)
- **Language**: TypeScript
- **HTTP Client**: Axios / NestJS HttpModule
- **Validation**: class-validator
- **Security**: helmet, crypto (untuk signature verification)

## 2. Struktur Module (`WhatsappModule`)

```typescript
// whatsapp.module.ts
@Module({
  imports: [HttpModule, ConfigModule, QueueModule],
  controllers: [WhatsappController],
  providers: [WhatsappService, WhatsappWebhookGuard, MediaService],
  exports: [WhatsappService],
})
export class WhatsappModule {}
```

## 3. Endpoint Specifications

### 3.1 Webhook Verification (GET)

Digunakan oleh Meta untuk memverifikasi callback URL saat setup.

- **Path**: `/api/whatsapp/webhook`
- **Method**: `GET`
- **Query Params**:
  - `hub.mode`: harus "subscribe"
  - `hub.verify_token`: token rahasia internal (simpan di ENV)
  - `hub.challenge`: string random
- **Response**: Return `hub.challenge` plain text (INT) jika valid.

### 3.2 Webhook Event Receiver (POST)

Menerima notifikasi pesan dan status.

- **Path**: `/api/whatsapp/webhook`
- **Method**: `POST`
- **Headers**:
  - `X-Hub-Signature-256`: Signature HMAC-SHA256 dari payload + App Secret.
- **Body**: JSON object standar WhatsApp Cloud API.

## 4. Service Implementation Details

### 4.1 Sending Messages

Menggunakan endpoint
`https://graph.facebook.com/v22.0/{PHONE_NUMBER_ID}/messages`.

```typescript
// Interface untuk Outbound Message
interface SendMessageDto {
  to: string; // Format: 628123456789
  type: 'text' | 'template' | 'image' | 'interactive' | 'flow';
  text?: { body: string };
  template?: { name: string; language: { code: string } };
  flow?: { flow_token: string; flow_id: string; flow_action: string };
  // ... field lain
}
```

### 4.2 Handling Media (Security Focused)

Jika pesan berisi gambar/dokumen:

1. Dapatkan `media_id` dari payload.
2. Call API `/v22.0/{media_id}` untuk dapatkan URL download sementara.
3. Download binary dengan Header `Authorization: Bearer {TOKEN}`.
4. **Security Check**: Validasi Magic Bytes/MIME Type (jangan hanya percaya
    ekstensi).
5. Upload ke internal storage (S3 Private Bucket).
6. Simpan URL internal ke Database.

### 4.3 Tenant Isolation & Security

- Setiap request webhook harus divalidasi `X-Hub-Signature-256`.
- Identifikasi `tenantId` (Law Firm ID) berdasarkan `PHONE_NUMBER_ID` yang
  menerima pesan.
- Simpan mapping `PHONE_NUMBER_ID` -> `tenantId` di cache (Redis) untuk performa
  tinggi.
- Gunakan `TenantContext` dalam NestJS untuk memastikan data tidak bocor antar
  firma hukum.

### 4.4 Error Handling & Retry

- **Rate Limit Meta**: Handle HTTP 429. Implementasi token bucket atau leaky
  bucket di Gateway.
- **Server Error**: Jika API Meta down (5xx), lakukan **Exponential Backoff
  Retry** (e.g., 1s, 2s, 4s, 8s).
- **Dead Letter Queue**: Pesan yang gagal dikirim setelah max retry masuk ke
  DLQ.

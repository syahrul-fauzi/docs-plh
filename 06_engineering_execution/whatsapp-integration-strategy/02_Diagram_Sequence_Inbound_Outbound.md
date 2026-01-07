# Diagram Sequence Inbound & Outbound

## 1. Inbound Message Flow (Pesan Masuk)

Alur ketika klien mengirim pesan ke nomor WhatsApp bisnis. Fokus pada
_responsivitas webhook_ dan _pemrosesan asinkron_.

```mermaid
sequenceDiagram
    participant U as User (WhatsApp App)
    participant M as Meta Cloud API
    participant G as WA Gateway (NestJS)
    participant Q as Message Queue
    participant C as Core Service
    participant D as Database

    U->>M: Kirim Pesan ("Halo")
    M->>G: POST /webhook (Payload)
    activate G
    G->>G: Validasi Signature (X-Hub-Signature)
    G->>G: Cek Duplikasi (Redis Cache)
    G->>Q: Publish 'wa.message.incoming'
    G-->>M: 200 OK (Ack Cepat < 3s)
    deactivate G

    Q->>C: Consume Event
    activate C
    C->>D: Cari User by Phone
    alt User Baru
        C->>D: Create Temporary Lead
    end
    C->>D: Simpan Pesan (Encrypted)
    C->>C: Trigger Notification / AI Logic
    deactivate C
```

## 2. Outbound Message Flow (Pesan Keluar)

Alur ketika Lawyer membalas melalui Dashboard atau AI mengirim respon otomatis.

```mermaid
sequenceDiagram
    participant L as Lawyer / AI System
    participant C as Core Service
    participant Q as Message Queue
    participant G as WA Gateway
    participant M as Meta Cloud API
    participant U as User

    L->>C: Kirim Balasan ("Baik, kami proses")
    activate C
    C->>D: Simpan Pesan (Status: Pending)
    C->>Q: Publish 'wa.message.outgoing'
    deactivate C

    Q->>G: Consume Event
    activate G
    G->>M: POST /messages (Text/Template)
    M-->>G: 200 OK (Message ID)
    G->>D: Update Status (Sent)
    deactivate G

    M->>U: Deliver Message
    M->>G: Webhook (Status: Delivered/Read)
    G->>D: Update Status (Delivered/Read)
```

## 3. Penanganan Status (Status Callback)

Penting untuk melacak status pesan (Sent -> Delivered -> Read) untuk kepastian
hukum (bahwa klien sudah menerima informasi).

1. **Sent**: Diterima server Meta.
2. **Delivered**: Masuk ke HP User.
3. **Read**: Dibuka oleh User (jika Read Receipt aktif).

> **Catatan Compliance**: Jangan berasumsi pesan terbaca jika status hanya
> "Delivered". Untuk notifikasi hukum penting, pertimbangkan konfirmasi manual
> dari user.

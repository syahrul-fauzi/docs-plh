# Desktop Command Registry (IPC Contract)

**Status:** DRAFT **Versi:** 1.0.0 **Tanggal:** 2026-01-07

## 1. Definisi IPC
Inter-Process Communication (IPC) di Lawyers Hub Desktop menggunakan sistem `invoke` Tauri untuk memanggil fungsi Rust dari frontend React. Semua perintah wajib didaftarkan dan divalidasi di sisi Rust.

## 2. Daftar Perintah (Commands)

### 2.1 File System Operations
| Command | Parameter | Deskripsi | Keamanan |
| :--- | :--- | :--- | :--- |
| `open_case_folder` | `case_id: String` | Membuka folder perkara lokal | Scope-limited |
| `save_document_draft` | `case_id, content, filename` | Menyimpan draf ke disk lokal | AES-256-GCM |
| `list_local_documents` | `case_id` | Menampilkan file di folder perkara | Read-only |

### 2.2 Security & Encryption
| Command | Parameter | Deskripsi |
| :--- | :--- | :--- |
| `encrypt_local_data` | `data: Vec<u8>` | Enkripsi data sensitif di sisi Rust |
| `get_secure_vault_token` | `auth_token` | Mengambil token dari sistem vault OS |

### 2.3 AI & Memory
| Command | Parameter | Deskripsi |
| :--- | :--- | :--- |
| `query_local_vector` | `query: String, case_id` | Mencari konteks di database vektor lokal |
| `flush_case_memory` | `case_id` | Menghapus cache memori perkara dari RAM |

## 3. Standar Implementasi Rust
Setiap command harus mengikuti pola berikut:

```rust
#[tauri::command]
pub async fn save_document_draft(
    case_id: String,
    content: String,
    state: tauri::State<'_, AppState>
) -> Result<String, String> {
    // 1. Validasi Case ID
    // 2. Enkripsi Konten
    // 3. Simpan ke Disk
    // 4. Log Audit
    Ok("Success".into())
}
```

## 4. Error Handling
Semua error dari Rust harus dipetakan ke format yang dapat dibaca oleh Frontend:
```typescript
interface CommandError {
  code: string;
  message: string;
  is_fatal: boolean;
}
```

---
*Referensi teknis untuk pengembang Lawyers Hub Desktop.*

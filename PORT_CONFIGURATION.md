# Konfigurasi Port Lingkungan Pengembangan (Local Development)

Dokumen ini menjelaskan konfigurasi port standar yang digunakan untuk menjalankan Lawyers Hub di lingkungan lokal.

## 🚀 Ringkasan Port

| Layanan | Port | Endpoint Utama | Deskripsi |
| :--- | :--- | :--- | :--- |
| **Web Frontend** | `3000` | [http://localhost:3000](http://localhost:3000) | Aplikasi web Next.js (App Router) |
| **Backend API** | `3001` | [http://localhost:3001/api/v1](http://localhost:3001/api/v1) | Core service NestJS |
| **AI Gateway** | `3010` | [http://localhost:3010](http://localhost:3010) | Gateway untuk LLM & CopilotKit |
| **Mobile Bundler**| `8081` | [http://localhost:8081](http://localhost:8081) | Expo Metro Bundler |
| **Prisma Studio** | `5555` | [http://localhost:5555](http://localhost:5555) | GUI untuk manajemen database |

---

## 📊 Monitoring & Health Checks

Setiap layanan memiliki endpoint health check untuk memantau ketersediaan sistem:

| Layanan | Health Endpoint | Method | Deskripsi |
| :--- | :--- | :--- | :--- |
| **Web** | `/api/health` | `GET` | Mengembalikan status layanan web dan environment. |
| **API** | `/api/v1/monitoring/health` | `GET` | Mengembalikan status core backend. |
| **AI Gateway** | `/ai/health` | `GET` | Mengembalikan status gateway AI. |
| **Monitoring** | `/api/v1/monitoring/metrics` | `GET` | Prometheus metrics (hanya API). |

---

## 🔧 Detail Konfigurasi

### 1. Web Frontend (Port 3000)
- **Framework**: Next.js
- **Konfigurasi Penting**: 
  - File: `apps/web/next.config.js`
  - Catatan: Pastikan `output: 'standalone'` dinonaktifkan di lingkungan lokal agar `next start` berfungsi dengan benar tanpa perlu setup Docker.
- **Environment Variables**:
  - `NEXT_PUBLIC_API_URL=http://localhost:3001/api/v1`
  - `NEXT_PUBLIC_AI_GATEWAY_URL=http://localhost:3010`

### 2. Backend API (Port 3001)
- **Framework**: NestJS
- **Konfigurasi Penting**:
  - File: `apps/api/src/main.ts`
  - Port dikontrol via `process.env.PORT` (default: `3001`).
- **Endpoint**: Semua endpoint diawali dengan prefix `/api/v1`.

### 3. AI Gateway (Port 3010)
- **Framework**: NestJS
- **Konfigurasi Penting**:
  - File: `apps/ai-gateway/src/main.ts`
  - Port default disetel ke `3010`.
- **Integrasi**: Bertindak sebagai proxy untuk CopilotKit di `apps/web/src/app/api/copilotkit/[[...handle]]/route.ts`.

### 4. Mobile (Port 8081)
- **Framework**: Expo (React Native)
- **Bundler**: Metro
- **Konfigurasi Penting**:
  - File: `apps/mobile/.env`
  - Pastikan `EXPO_PUBLIC_API_URL` mengarah ke `http://localhost:3001/api/v1` (bukan staging) untuk pengembangan lokal.
  - Untuk emulator Android, gunakan IP `10.0.2.2` jika `localhost` tidak dapat dijangkau.

---

## 📝 Troubleshooting Port

1. **Port Terpakai**:
   Jika port sudah digunakan oleh aplikasi lain, Anda bisa memeriksa PID-nya:
   ```bash
   ss -tunlp | grep :3000
   ```
2. **Konflik AI Gateway**:
   Pastikan tidak ada referensi lama ke port `3100`. Port standar AI Gateway saat ini adalah `3010`.
3. **Koneksi Mobile**:
   Jika Metro Bundler tidak merespon di browser, pastikan Anda menjalankan `npm run start` dari root yang akan menjalankan `expo start`.

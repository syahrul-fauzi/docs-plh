# Panduan Deployment Staging & Telemetri

Dokumen ini menjelaskan prosedur deployment ke lingkungan Staging dan konfigurasi sistem telemetri untuk Lawyers Hub (Phase 1 Beta).

## 1. Persiapan Lingkungan Staging

### 1.1 Environment Variables
Pastikan variabel lingkungan berikut dikonfigurasi di server staging (atau Vercel/Docker):

**Backend (`apps/api`):**
```bash
NODE_ENV=staging
PORT=3000
DATABASE_URL="postgresql://user:pass@staging-db:5432/lawyers_hub_staging"
REDIS_HOST=staging-redis
JWT_SECRET="<secure-random-string>"
# Monitoring
METRICS_ENABLED=true
MONITORING_CPU_THRESHOLD=0.8
ALERT_WEBHOOK_URL="<slack-or-teams-webhook>"
```

**Frontend (`apps/web`):**
```bash
NODE_ENV=production
NEXT_PUBLIC_API_URL="https://api-staging.lawyershub.com/api/v1"
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="pk_test_..."
NEXT_PUBLIC_SENTRY_DSN="<sentry-dsn>"
```

### 1.2 Infrastruktur (Docker)
Gunakan `docker-compose.staging.yml` sebagai sumber kebenaran. Port default:

| Service | URL |
|---|---|
| Web | `http://localhost:3006` |
| API | `http://localhost:3002/api/v1` |
| AI Gateway | `http://localhost:3004` |
| Prometheus | `http://localhost:9091` |
| Grafana | `http://localhost:3007` |
| Jaeger | `http://localhost:16686` |

## 2. Sistem Telemetri & Monitoring

### 2.1 Backend Metrics
Backend secara otomatis mengumpulkan metrik sistem (CPU, Memory, Network) setiap 5 detik.

*   **Dashboard Endpoint:** `GET /api/v1/monitoring/dashboard?hours=24`
    *   Mengembalikan data JSON historis untuk visualisasi.
*   **Prometheus Endpoint:** `GET /api/v1/monitoring/metrics`
    *   Kompatibel dengan Prometheus/Grafana scraper.

**Healthchecks yang disarankan (Smoke Test):**
*   API: `GET /api/v1/monitoring/health`
*   Web: `GET /api/health`
*   AI Gateway: `GET /ai/health`

### 2.2 Frontend Telemetri (Phase 1 Routing)
Middleware Frontend merekam setiap request dengan event `PHASE_1_ROUTING`.
Log ini dapat diakses via:
1.  **Vercel Logs / Docker Logs**
2.  **Sentry Performance Monitoring** (jika dikonfigurasi)

### 2.3 Analisis Perbandingan (Staging vs Production)
Gunakan template berikut untuk laporan mingguan:

| Metrik | Staging (Load Test) | Production (Baseline) | Delta |
|--------|---------------------|-----------------------|-------|
| Avg Response Time | 120ms | 150ms | -20% (Better) |
| Error Rate (5xx) | 0.01% | 0.05% | Stabil |
| CPU Usage (Avg) | 45% | 60% | -15% |
| Tenant Routing Success | 100% | 99.8% | +0.2% |

## 3. Prosedur Rollback

Jika ditemukan isu kritis (Data Leak, Error Rate > 5%) selama fase Staging/Beta:

1.  **Stop Traffic:** Hentikan routing ke instance Staging.
2.  **Revert Database:** Jika ada migrasi skema yang merusak, restore snapshot database sebelum deployment.
    ```bash
    pg_restore -d lawyers_hub_staging backup_pre_deploy.dump
    ```
3.  **Revert Code:** Checkout commit stabil sebelumnya dan redeploy.
    ```bash
    git checkout main-stable
    npm run deploy:staging
    ```

## 4. Notifikasi Insiden
Sistem `MonitoringService` dikonfigurasi untuk mengirim alert otomatis ke `ALERT_WEBHOOK_URL` jika:
*   CPU > 80%
*   Memory > 80%
*   Latency > 500ms

Pastikan webhook ini terhubung ke channel Slack/Teams Tim DevOps.

## 5. Strategi Deployment (Best Practice)
Untuk meminimalkan downtime dan mempermudah rollback:
*   **Blue-Green:** siapkan dua environment identik, alihkan traffic setelah verifikasi healthcheck.
*   **Canary/Rolling:** rilis bertahap, pantau error rate/latency sebelum melanjutkan rollout.
*   **Feature Flags:** aktifkan fitur baru untuk subset pengguna/tenant, sehingga rollback dapat dilakukan tanpa redeploy.

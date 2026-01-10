# Environment Configuration - Lawyers Hub

Dokumen ini merinci spesifikasi infrastruktur dan konfigurasi environment untuk lingkungan Produksi Lawyers Hub.

## 1. Spesifikasi Server (Production Grade)

### Web Server (Frontend - Next.js)
- **CPU**: 2 vCPU (Dedicated)
- **RAM**: 4 GB DDR4
- **Storage**: 20 GB SSD (High IOPS)
- **OS**: Alpine Linux (via Docker)
- **Scaling**: Minimum 2 replicas, Auto-scaling up to 5 replicas based on CPU usage (>70%).

### API Server (Backend - NestJS)
- **CPU**: 4 vCPU (Compute Optimized)
- **RAM**: 8 GB DDR4
- **Storage**: 40 GB SSD
- **Scaling**: Minimum 2 replicas, Auto-scaling up to 10 replicas.

### Database Server (PostgreSQL)
- **Instance Type**: Managed Service (e.g., RDS/Cloud SQL)
- **vCPU**: 4 vCPU
- **RAM**: 16 GB
- **Storage**: 100 GB (Auto-grow enabled)
- **Backup**: Multi-AZ (High Availability), Point-in-time recovery (PITR) enabled.

### Cache & Queue (Redis)
- **Instance Type**: Managed Service
- **RAM**: 4 GB (Reserved Memory)
- **Persistence**: AOF enabled.

## 2. Load Balancer & CDN
- **Load Balancer**: L7 Load Balancer with SSL Termination (TLS 1.3).
- **CDN**: Cloudflare/CloudFront for static assets (`/_next/static`, `/public`).
- **WAF**: Web Application Firewall enabled to block SQLi, XSS, and DDoS.

## 3. Environment Variables (Required)

| Key | Description | Target |
| :--- | :--- | :--- |
| `DATABASE_URL` | PostgreSQL connection string with RLS enabled. | Backend |
| `REDIS_URL` | Redis connection string for BullMQ and Caching. | Backend |
| `JWT_SECRET` | Secret key for signing access tokens. | Backend |
| `CLERK_SECRET_KEY` | Secret key for Clerk authentication. | Backend |
| `NEXT_PUBLIC_API_URL` | Public endpoint for API access. | Frontend |
| `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` | Public key for Clerk frontend. | Frontend |
| `STRIPE_SECRET_KEY` | Key for billing and subscription processing. | Backend |
| `OPENAI_API_KEY` | Key for AI features (summarization, analysis). | AI Gateway |
| `STORAGE_BUCKET_NAME` | S3 bucket name for document storage. | Backend |

## 4. Keamanan Jaringan
- **VPC Isolation**: Database dan Redis hanya dapat diakses dari subnet API Server.
- **Firewall**: Port 80/443 terbuka untuk publik; Port 22 (SSH) hanya terbuka untuk Bastion Host/VPN.

---
*Terakhir diupdate: 2026-01-10*

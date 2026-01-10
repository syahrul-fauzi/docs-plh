# Staging Deployment Process - Lawyers Hub

This document describes the process and architecture of the staging deployment for the Lawyers Hub application.

## Staging Architecture

The staging environment is designed to mirror the production environment as closely as possible, but with isolated resources.

- **Frontend**: Next.js application (`apps/web`)
- **Backend API**: NestJS application (`apps/api`)
- **AI Gateway**: NestJS application (`apps/ai-gateway`)
- **Background Worker**: NestJS application (`apps/worker`)
- **Database**: PostgreSQL 15 (Isolated instance)
- **Cache**: Redis 7 (Isolated instance)

## Deployment Pipeline

The staging deployment is automated using GitHub Actions.

### Trigger
- Push to the `develop` branch.

### Stages
1. **Validation**:
   - Install dependencies.
   - Run linting and type checking.
   - Execute unit and integration tests.
2. **Build**:
   - Build Docker images for all services.
3. **Deploy**:
   - Start the environment using Docker Compose.
   - Run database migrations using Prisma.
4. **Verification**:
   - Perform health checks on the API and Frontend.

## Environment Variables

The staging environment uses specific variables defined in `.env.staging`. Sensitive information should be stored as GitHub Secrets and mapped in the workflow.

| Variable | Description |
|----------|-------------|
| `DATABASE_URL` | Staging database connection string |
| `REDIS_HOST` | Staging Redis host |
| `CLERK_SECRET_KEY` | Clerk secret key for staging |
| `STRIPE_SECRET_KEY` | Stripe secret key for staging |
| `OPENAI_API_KEY` | OpenAI API key for staging AI features |

## Monitoring and Logging

- **Logging**: All services output logs to stdout, which are collected by the container engine.
- **Monitoring**: Prometheus and Grafana are used for metric collection and visualization (see `docker-compose.staging.yml`).
- **Alerting**: Configured via Prometheus Alertmanager (see `prometheus_alerts.yml`).

## Data Management

### Backup
To perform a manual backup of the staging database, run:
```bash
./scripts/backup-staging.sh
```
Backups are stored in `backups/staging/` and kept for 7 days.

### Restore
To restore the staging database from a backup file, run:
```bash
./scripts/restore-staging.sh backups/staging/lawyers_hub_staging_TIMESTAMP.sql
```

## Rollback Plan

If a deployment fails:
1. Identify the previous stable commit hash.
2. Revert the `develop` branch or trigger a manual deployment with the stable hash.
3. The pipeline will automatically rebuild and redeploy the stable version.
4. In case of database migration issues, manual intervention may be required to rollback Prisma migrations.

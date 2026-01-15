# Infrastructure Phase 2: Performance & Reliability

This document outlines the architectural changes and implementations completed in Phase 2 for the Lawyers Hub staging environment.

## 1. Network Security Enhancement

### Virtual Private Cloud (VPC)
- **Segmentation**: Defined a custom VPC with isolated public and private subnets across multiple Availability Zones (AZs).
- **Public Subnets**: Host the Load Balancer and potentially the Frontend (Web).
- **Private Subnets**: Host the API, Database, and Redis instances, ensuring they are not directly accessible from the internet.

### Security Groups (Firewalls)
- **API Security Group**: Allows inbound traffic on port 3001 (API) only.
- **Database Security Group**: Allows inbound traffic on port 5432 only from the API security group.
- **Redis Security Group**: Allows inbound traffic on port 6379 only from the API security group.
- **Egress Policies**: Explicitly allow only necessary outbound traffic (least privilege).

**Artifacts**: [Terraform main.tf](file:///home/inbox/smart-ai/lawyers-hub/infrastructure/terraform/main.tf), [VPC Module](file:///home/inbox/smart-ai/lawyers-hub/infrastructure/terraform/modules/vpc/main.tf), [Security Groups Module](file:///home/inbox/smart-ai/lawyers-hub/infrastructure/terraform/modules/security_groups/main.tf).

## 2. Job Queue Persistence (BullMQ)

### Redis Configuration
- **Persistence Modes**: Enabled both RDB (snapshots) and AOF (Append-Only File) to ensure data durability and fast recovery.
  - `save 60 1`: Snapshot every 60 seconds if at least 1 key changed.
  - `appendonly yes`: Logs every write operation.
- **Recovery**: Verified that BullMQ jobs persist across container restarts.

**Artifacts**: [docker-compose.staging.yml](file:///home/inbox/smart-ai/lawyers-hub/docker-compose.staging.yml), [k8s redis.yaml](file:///home/inbox/smart-ai/lawyers-hub/infrastructure/k8s/base/redis.yaml).

## 3. Auto-scaling Infrastructure (Kubernetes)

### Cluster Readiness
- **Migration Path**: Initialized Kubernetes manifests for all core services (API, Web, Redis, DB).
- **Horizontal Pod Autoscaler (HPA)**: 
  - API service is configured to scale between 2 and 10 replicas based on CPU utilization (threshold: 70%).
- **Resource Management**: Defined explicit CPU/Memory requests and limits for all pods.

**Artifacts**: [k8s Base Manifests](file:///home/inbox/smart-ai/lawyers-hub/infrastructure/k8s/base/).

## 4. Performance Monitoring & Distributed Tracing

### Monitoring Stack
- **Prometheus**: Configured with custom scrape jobs and alerting rules (High CPU, High API Error Rate).
- **Grafana**: Provisioned with a default Prometheus datasource for real-time visualization.
- **Jaeger**: Deployed in staging for distributed tracing collection.

### Distributed Tracing
- **Correlation IDs**: Implemented `RequestIdMiddleware` to ensure every request has a unique `x-correlation-id`.
- **Propagation**: Correlation IDs are propagated through headers and logged in every service interaction.

**Artifacts**: [Monitoring Configs](file:///home/inbox/smart-ai/lawyers-hub/infrastructure/monitoring/), [RequestIdMiddleware](file:///home/inbox/smart-ai/lawyers-hub/apps/api/src/common/middleware/request-id.middleware.ts).

## 5. Verification & Disaster Recovery
### Automated Testing
- **Infrastructure Verification**: Run `bash scripts/verify-infrastructure.sh` to validate all manifests, configs, and service registrations.
- **Chaos Simulation**: Use `ts-node scripts/chaos-simulation.ts` to test service recovery and job persistence during outages.

### Disaster Recovery (Redis)
- **Backup Script**: `scripts/redis-backup.sh` handles automated `BGSAVE` and offsite-ready RDB archiving.
- **DR Test**: Run `bash scripts/redis-backup.sh test` to simulate total data loss and verify the restoration process from the latest backup.

## 6. Performance Benchmarks (Target)
| Metric | Pre-Phase 2 | Post-Phase 2 (Target) |
|--------|-------------|-----------------------|
| Concurrent Users | 100 | 500+ |
| API Latency (p95) | 450ms | < 200ms |
| Redis Recovery Time | N/A (Manual) | < 30s (Automated) |
| Auto-scaling Latency | N/A | < 120s |

## 7. Rollback Plans
- **Terraform**: `terraform destroy` or revert to previous state file.
- **Kubernetes**: `kubectl rollout undo deployment/<service-name>`.
- **Redis**: Revert `docker-compose.staging.yml` and remove persistence volumes if necessary.
- **Monitoring**: `docker compose down` for the monitoring stack.

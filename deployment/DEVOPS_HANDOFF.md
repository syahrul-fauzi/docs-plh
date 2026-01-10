# DevOps Handoff: Staging Release v1.0.0

**Date:** 2026-01-09  
**Version:** 1.0.0-staging  
**Artifact:** `release/staging-v1.0.0.tar.gz`  
**Checksum (SHA-256):** `c7dd6c3d83a9409c982d51277a0a08bc81b46f8d5862f3247e25b32a1ee8cdf5`

## 1. Target Environment Specifications

*   **OS**: Linux (Ubuntu 22.04 LTS recommended)
*   **Runtime**: Node.js v20.x LTS
*   **Process Manager**: PM2 or Systemd
*   **Network**: Inbound Traffic allowed on Port 3008

## 2. Deployment Instructions

1.  **Transfer Artifact**:
    Securely copy `staging-v1.0.0.tar.gz` to the target server `/opt/lawyers-hub/`.

2.  **Extract**:
    ```bash
    mkdir -p /opt/lawyers-hub/v1.0.0
    tar -xzf staging-v1.0.0.tar.gz -C /opt/lawyers-hub/v1.0.0
    ```

3.  **Configure Environment**:
    Create a `.env` file in `/opt/lawyers-hub/v1.0.0/.env`:
    ```env
    PORT=3008
    NODE_ENV=production
    NEXT_PUBLIC_BYPASS_CLERK=true
    # Add other DB connection strings if not using mock
    ```

4.  **Start Service**:
    ```bash
    cd /opt/lawyers-hub/v1.0.0
    npm start
    ```

## 3. Verification

Run the provided verification script or check manually:
```bash
curl http://localhost:3008/api/cases
# Expected: HTTP 200
```

## 4. Rollback Plan

If deployment fails, revert symlink to previous version:
```bash
ln -sfn /opt/lawyers-hub/v0.9.9 /opt/lawyers-hub/current
systemctl restart lawyers-hub
```

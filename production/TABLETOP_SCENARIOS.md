# Production Migration: Tabletop Exercise Scenarios

**Date:** TBD
**Participants:** Engineering Leads, DevOps, QA
**Objective:** Validate the robustness of the Migration and Rollback plans.

## Scenario 1: Database Migration Failure (Partial Apply)
*   **Trigger**: `prisma migrate deploy` fails halfway due to a timeout or lock.
*   **Symptom**: New tables exist, but columns are missing in existing tables. App crashes on startup.
*   **Discussion Points**:
    *   How do we detect the "partial" state?
    *   Does `prisma migrate resolve` work in production?
    *   **Action**: Validate the database backup restore time (RTO).

## Scenario 2: "Works in Staging, Fails in Prod" (Auth Config)
*   **Trigger**: Clerk API keys for Production are invalid or expired.
*   **Symptom**: Users see "Authentication Failed" immediately after deployment.
*   **Discussion Points**:
    *   How quickly can we swap env vars without a full redeploy?
    *   Should we rollback immediately or fix forward?
    *   **Decision Criteria**: If fix takes > 5 mins, Rollback.

## Scenario 3: High Latency in Collaborative Editor
*   **Trigger**: WebSocket connections saturate the load balancer.
*   **Symptom**: P95 latency spikes to 10s. Editor shows "Reconnecting..." constantly.
*   **Discussion Points**:
    *   Do we have autoscaling rules for WebSockets?
    *   Is this a code issue (memory leak) or infra issue?
    *   **Rollback Threshold**: If P95 > 5s for 10 mins.

## Scenario 4: Data Corruption in Drafts
*   **Trigger**: A bug in the YJS logic corrupts document state on save.
*   **Symptom**: Documents open as blank or gibberish.
*   **Discussion Points**:
    *   This is the worst-case scenario.
    *   Can we restore *only* the corrupted rows?
    *   **Action**: Verify point-in-time recovery (PITR) capability for the database.

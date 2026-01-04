# 📧 Design Document: Notification System (v1.0)

**Project:** Lawyers Hub  
**Status:** Implementation Ready  
**Last Updated:** 2026-01-03  
**Owner:** Engineering Team  

---

## 1. Overview
The Notification System is a critical component for user engagement and compliance enforcement. It ensures that users are timely informed about:
1.  **Account Status**: Subscription expiries, billing issues.
2.  **Compliance Events**: High-risk draft violations, rule breaches.
3.  **Collaboration**: Team invitations, comments (future).

## 2. Architecture

### 2.1 Components
- **EmailService**: Centralized service for sending emails via SMTP (Nodemailer).
- **BillingSchedulerService**: Cron-based service (using `@nestjs/schedule`) to run periodic checks.
- **Event Triggers**: Direct calls from Feature Services (e.g., `DraftsService`, `InvitationsService`).

### 2.2 Tech Stack
- **Framework**: NestJS
- **Scheduler**: `@nestjs/schedule` (Cron jobs)
- **Email Transport**: `nodemailer`
- **Templates**: HTML Strings (Inline for v1, Handlebars for v2)

---

## 3. Implemented Workflows

### 3.1 Subscription Expiry Notification
- **Trigger**: Daily Cron Job (09:00 AM).
- **Condition**: Subscription `currentPeriodEnd` is exactly 3 days from now.
- **Recipient**: Tenant Admins.
- **Content**: Warning about downgrade to FREE plan and link to billing dashboard.

### 3.2 High-Risk Compliance Alert
- **Trigger**: `DraftsService.generate()` completion.
- **Condition**: `riskScore >= 0.8` (80%).
- **Recipient**: The user who generated the draft.
- **Content**: Alert with specific violations and risk score.

### 3.3 Team Invitation
- **Trigger**: Admin invites a new member.
- **Recipient**: Invitee email.
- **Content**: Welcome message with unique, time-limited acceptance link.

---

## 4. Future Roadmap (Phase 18+)

### 4.1 In-App Notifications
- **Real-time**: WebSockets (Gateway) for instant alerts.
- **Persistence**: Database storage (`Notification` model) for "Bell" icon history.

### 4.2 Preferences
- Allow users to opt-out of non-critical emails.
- Daily digest options.

---
*This document governs the implementation of the Notification System.*

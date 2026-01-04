# Document Automation & Versioning - Phase 20/21

## Overview
This document covers the implementation of advanced document automation features, including Multi-Template Merge and Template Versioning.

## Features

### 1. Multi-Template Merge
Allows users to combine multiple document templates into a single draft.
- **Selection & Ordering**: Users can select multiple templates and arrange them in the desired order via the UI.
- **Automatic Format Normalization**: 
  - Normalizes line endings (`\r\n` to `\n`).
  - Removes excessive whitespace (triple newlines reduced to double).
  - Trims content for clean joining.
- **Page Break Handling**: Automatically inserts `\x0C` (Form Feed) between templates to ensure each starts on a new page in PDF exports.
- **Saving**: Results are saved as a new `Draft` with the type `Multi-Template Document`.

### 2. Template Versioning
Comprehensive system for tracking changes to document templates.
- **Automatic Tracking**: Every update to a template creates a new version in the `TemplateVersion` model.
- **Metadata**: Stores who made the change (`userId`), when (`createdAt`), and what changed (`changeLog`).
- **Restoration**: 1-click restoration to any previous version (restricted to `FIRM_ADMIN` and `LAWYER` roles).
- **Visual Diff Viewer**: Compare any two versions side-by-side with color-coded additions and removals.
- **Efficiency**: Stores content delta using Prisma (currently full content for reliability, can be optimized to deltas if size becomes an issue).

## Technical Implementation

### Models (Prisma)
- `DocumentTemplate`: Main template storage.
- `TemplateVersion`: Historical records linked to a template.

### Services
- `TemplatesService`: 
  - `mergeMultiple(tenantId, templateIds, caseId)`: Core merge logic.
  - `restoreVersion(tenantId, userId, userRole, templateId, versionId)`: Restoration with role-based access control (RBAC).
  - `compareVersions(tenantId, templateId, v1, v2)`: Generates diff using the `diff` library.
- `DraftsService`: Handles PDF generation using `pdfkit`.

### API Endpoints
- `POST /templates/merge-multiple/:caseId`: Create combined draft.
- `POST /templates/:id/restore/:versionId`: Restore a version.
- `GET /templates/:id/diff?v1=...&v2=...`: Get visual difference.

## User Guide

### How to Merge Multiple Templates
1. Navigate to a **Case Detail** page.
2. Click the **Multi-Merge** button.
3. Select the templates you want to include.
4. Use the **↑** and **↓** arrows to set the order.
5. Click **Create Combined Document**.

### How to Use Version History
1. Navigate to the **Template Gallery**.
2. Click the **History** (clock) icon on any template.
3. To compare: Select two versions and click **Compare Selected**.
4. To restore: Click the **Restore** (rotate-ccw) icon next to the desired version.

## Security & Compliance
- **RBAC**: Only authorized roles can restore templates.
- **Audit Logs**: All exports and restorations are logged in the `AuditLog` table.
- **Digital Signatures**: Exported PDFs include SHA-256 hashes of the content for integrity verification.

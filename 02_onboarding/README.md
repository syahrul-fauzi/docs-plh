---
title: Developer Onboarding Guide
version: 1.0.0
last_updated: 2026-01-07
author: World-Class Super Agent
tags: [onboarding, setup, development, guide]
agent_context: This guide helps new developers set up their local environment and understand the development workflow for the Lawyers Hub project.
---

# 🚀 Developer Onboarding Guide

Welcome to the **Lawyers Hub** engineering team! This guide will help you get your development environment up and running.

## 1. Prerequisites
Ensure you have the following installed:
- **Node.js**: >= 18.0.0
- **npm**: >= 9.0.0
- **Docker**: For running PostgreSQL, Redis, and other services locally.
- **Turbo CLI**: `npm install -g turbo` (optional, but recommended).

## 2. Local Setup

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd lawyers-hub
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Environment Variables
Copy the example environment file and fill in the required values:
```bash
cp .env.example .env
```
*Note: Ask your team lead for the development API keys for Clerk, Stripe, and OpenAI.*

### Step 4: Spin up Infrastructure
Use Docker Compose to start the database and cache:
```bash
docker-compose up -d
```

### Step 5: Run Migrations
```bash
npx turbo run db:push
```

## 3. Monorepo Overview
Understanding the structure is key to efficient development:
- **`apps/`**: Deployable units (Web, API, Worker).
- **`packages/database`**: Prisma schema, client, and the `withTenant` helper for RLS.
- **`packages/rules-engine`**: The core logic for validating AI actions against legal rules.
- **`packages/security`**: PII masking (Presidio) and data encryption utilities.
- **`packages/ui`**: Shared React components based on Tailwind and Radix UI.

## 4. Working with AI Rules
If you are developing new AI features, you must interact with the Rules Engine:
1.  **Rule Definition**: Rules are defined in `.trae/rules/`.
2.  **Local Validation**: Run `npx turbo run test --filter=@lawyers-hub/rules-engine` to ensure your changes don't break existing legal enforcements.
3.  **PII Check**: Always use `PresidioMaskingService` when passing user-generated content to LLM services.

## 5. Development Workflow

### Running the Apps
Start all applications in development mode:
```bash
npm run dev
```
- **Web App**: http://localhost:3000
- **API**: http://localhost:4000
- **AI Gateway**: http://localhost:4001

### Adding a New Feature
Follow the **Clean Architecture** principles:
1. Define the entity and repository interface in `packages/domain`.
2. Implement the repository in `apps/api/src/[module]/infrastructure`.
3. Create use cases in `apps/api/src/[module]/application/use-cases`.
4. Register everything in the NestJS module.
5. Expose via a controller.

## 4. Testing Strategy
- **Unit Tests**: `npm run test`
- **E2E Tests**: `npm run test:e2e`
- **Linting**: `npm run lint`

## 5. Coding Standards
- Use **kebab-case** for file names.
- Use **PascalCase** for React components and TypeScript interfaces.
- Follow the JSDoc standard for documenting public functions in `packages/`.

## 6. Your First Task
To get familiar with the codebase, complete this small task:
1.  **Run the App**: Ensure you can run `npm run dev` and see the login screen.
2.  **Add a Log**: Add a `console.log` in `apps/api/src/app.module.ts` and verify it appears in the terminal.
3.  **Explore the Rules**: Open `.trae/rules/project_rules.md` and read the coding standards.
4.  **Create a PR**: Create a small PR to update your name in the `CONTRIBUTORS.md` file (if it exists).

---
*Need help? Reach out to @Engineering-Lead or check the [Troubleshooting Guide](../06_engineering_execution/troubleshooting.md).*

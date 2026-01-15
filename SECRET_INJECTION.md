# Secret Injection Guide

This guide explains how to use the automated secret injection mechanism for local development and production.

## Overview

The `scripts/inject-secrets.ts` script fetches secrets from HashiCorp Vault and injects them into the application's environment variables at runtime. This ensures that sensitive keys (like `CLERK_SECRET_KEY`) are not hardcoded or stored in `.env` files.

## Prerequisites

1.  **HashiCorp Vault**: Must be running and accessible.
    ```bash
    docker-compose -f docker-compose.vault.yml up -d
    ```
2.  **Vault Token**: A valid token must be available (default: `root` for dev).

## Usage

### Running with Secret Injection

To run any command with secret injection, use `ts-node` to execute the wrapper script:

```bash
# Example: Run dev server with injected secrets
npx ts-node scripts/inject-secrets.ts npm run dev
```

### Configuration

The script is configured via environment variables (defaults provided for dev):

- `VAULT_ADDR`: URL of the Vault server (default: `http://localhost:8200`).
- `VAULT_TOKEN`: Authentication token (default: `root`).
- `SECRET_PATH`: Path to the secrets in Vault (default: `secret/data/lawyers-hub/env`).

## Integration

To integrate with `package.json`, update the scripts:

```json
"scripts": {
  "dev:secure": "ts-node ../../scripts/inject-secrets.ts npm run dev"
}
```

## Error Handling

- **Connection Refused**: Falls back to local `.env` file with a warning.
- **Secrets Not Found**: Logs a warning and proceeds with existing environment variables.
- **Other Errors**: Logs the error and exits.

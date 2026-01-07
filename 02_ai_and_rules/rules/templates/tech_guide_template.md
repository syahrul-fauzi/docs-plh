# 🛠️ Technical Guide: Rule Implementation

**Document ID:** LH-TECH-RULE-001  
**Last Updated:** 2026-01-02  
**Target Audience:** Software Engineers, QA, DevOps

---

## 1. Overview

This guide provides technical specifications for implementing, testing, and
deploying Agentic Rules within the Lawyers Hub ecosystem.

### Prerequisites

- Node.js >= 18.x
- TypeScript >= 5.x
- Access to `lawyers-hub` repository
- Understanding of
  [Rule Engine Architecture](../Design%20Document:%20Rules%20Documentation%20Framework.md)

---

## 2. Rule Structure (YAML)

All rules are defined in YAML format under `.trae/rules/`.

### Schema Definition

```typescript
interface Rule {
  rule_id: string; // Unique ID (e.g., CORP-CONT-001)
  name: string; // Descriptive name
  priority: 'CRITICAL' | 'HIGH' | 'MEDIUM' | 'LOW';
  domain: string; // e.g., "CORPORATE", "LITIGATION"
  description: string;
  trigger: {
    context: string; // e.g., "contract_analysis"
    action_type: string; // e.g., "validate_draft"
  };
  condition: Record<string, any>; // Logic to evaluate
  action: {
    type: 'BLOCK' | 'WARN' | 'INFO';
    message: string;
  };
}
```

### Example

```yaml
- rule_id: CORP-CONT-001
  name: 'Bahasa Indonesia Mandatory'
  priority: 'CRITICAL'
  domain: 'CORPORATE'
  description:
    'Contracts involving Indonesian entities must use Bahasa Indonesia (UU No.
    24/2009).'
  trigger:
    context: 'contract_drafting'
    action_type: 'generate_draft'
  condition:
    parties_nationality: "includes('ID')"
    language: "!= 'ID'"
  action:
    type: 'BLOCK'
    message:
      'Kontrak dengan pihak Indonesia wajib menggunakan Bahasa Indonesia.'
```

---

## 3. Integrasi Kode (Code Integration)

Cara memanggil aturan ini dari layanan backend:

```typescript
import { engine } from '@lawyers-hub/rule-engine';

const result = await engine.evaluate('[ID]', context);
if (result.status === 'REJECTED') {
  throw new ComplianceError(result.reason);
}
```

## 4. Interpolasi Variabel (Mail Merge)

Implementasi teknis untuk substitusi variabel dinamis yang didefinisikan di PRD:

| Variabel PRD         | Mapping Data Context              | Tipe Data |
| :------------------- | :-------------------------------- | :-------- |
| `{{CLIENT_NAME}}`    | `context.case.client.name`        | String    |
| `{{CONTRACT_VALUE}}` | `context.document.metadata.value` | Number    |

Contoh implementasi resolver:

```typescript
const variables = {
  CLIENT_NAME: await clientService.getName(context.clientId),
  CONTRACT_VALUE: documentParser.extractValue(context.fileBuffer),
};

// Mengganti placeholder dalam pesan error/warning
const message = rule.message.replace(
  /\{\{(\w+)\}\}/g,
  (_, key) => variables[key] || 'Unknown',
);
```

## 5. Pengujian & Debugging

- **Linting**: Jalankan `npm run lint:rules` untuk validasi sintaks.
- **Dry Run**: Gunakan `rule-cli test [ID] --data sample.json` untuk simulasi.
- **Logs**: Periksa audit trail di `logs/compliance/audit.log`.

---

## 5. Deployment & Monitoring

### CI/CD Checks

- **Linting**: Ensure YAML syntax is valid.
- **Tests**: All rule tests must pass before merge.

### Observability

- **Audit Logs**: Check `AuditLog` table in Prisma for rule execution history.
- **Metrics**: Monitor `rule_violations_total` in Grafana (if configured).

---

## 6. Troubleshooting

| Error                         | Cause                   | Solution                                             |
| :---------------------------- | :---------------------- | :--------------------------------------------------- |
| `Rule ID collision`           | Duplicate ID in YAML    | Search and rename one of the rules.                  |
| `Condition evaluation failed` | Missing data in payload | Ensure `ComplianceAgent` passes all required fields. |
| `YAML parser error`           | Invalid indentation     | Use a YAML validator to fix syntax.                  |

---

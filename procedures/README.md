# Procedures

This section contains step-by-step operational procedures that implement the requirements defined in policies.

## Available Procedures (12)

### Access Management

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [User Access Request Procedure](./user-access-request-procedure.md) | [Access Control Policy](../policies/access-control-policy.md) | Available |
| [Access Review Procedure](./access-review-procedure.md) | [Access Control Policy](../policies/access-control-policy.md) | Available |
| [User Offboarding Procedure](./user-offboarding-procedure.md) | [Access Control Policy](../policies/access-control-policy.md) | Available |

### Incident Management

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Incident Response Procedure](./incident-response-procedure.md) | [Incident Response Policy](../policies/incident-response-policy.md) | Available |

### Change & Operations

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Change Management Procedure](./change-management-procedure.md) | [Change Management Policy](../policies/change-management-policy.md) | Available |
| [Backup and Recovery Procedure](./backup-procedure.md) | [Backup Policy](../policies/backup-policy.md) | Available |
| [Patch Management Procedure](./patch-management-procedure.md) | [Vulnerability Management Policy](../policies/vulnerability-management-policy.md) | **NEW** |

### Third Party & Vendor

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Vendor Security Assessment Procedure](./vendor-security-assessment-procedure.md) | [Supplier Security Policy](../policies/supplier-security-policy.md) | **NEW** |

### Business Continuity

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Disaster Recovery Procedure](./disaster-recovery-procedure.md) | [Business Continuity Policy](../policies/business-continuity-policy.md) | **NEW** |

### Data Protection

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Data Subject Request Procedure](./data-subject-request-procedure.md) | [Data Protection Policy](../policies/data-protection-policy.md) | **NEW** |

### ISMS Operations

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Internal Audit Procedure](./internal-audit-procedure.md) | [Information Security Policy](../policies/information-security-policy.md) | Available |
| [Security Awareness Procedure](./security-awareness-procedure.md) | [Information Security Policy](../policies/information-security-policy.md) | **NEW** |

### ISO 27001 Specific Procedures

Additional procedures in `/frameworks/iso-27001/procedures/`:

| Procedure | ISO Clause | Status |
|-----------|------------|--------|
| [Document Control Procedure](../frameworks/iso-27001/procedures/document-control-procedure.md) | 7.5 | Available |
| [Internal Audit Program](../frameworks/iso-27001/procedures/internal-audit-program.md) | 9.2 | Available |
| [Management Review Procedure](../frameworks/iso-27001/procedures/management-review-procedure.md) | 9.3 | Available |
| [Corrective Action Procedure](../frameworks/iso-27001/procedures/corrective-action-procedure.md) | 10.1, 10.2 | Available |
| [Risk Treatment Procedure](../frameworks/iso-27001/procedures/risk-treatment-procedure.md) | 6.1.3 | **NEW** |

---

## Planned Procedures (To Do)

### Access Management

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Password Reset Procedure | Password Policy | High |
| Privileged Access Procedure | Access Control Policy | High |
| Third-Party Access Procedure | Supplier Security Policy | Medium |

### Incident Management

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Incident Reporting Procedure | Incident Response Policy | Medium |
| Forensics Procedure | Incident Response Policy | Low |
| Evidence Collection Procedure | Incident Response Policy | Low |

### Data Management

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Data Disposal Procedure | Data Classification Policy | Medium |
| Data Handling Procedure | Data Classification Policy | Medium |

### Change & Operations

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Vulnerability Scanning Procedure | Vulnerability Management Policy | Medium |
| Configuration Management Procedure | Change Management Policy | Medium |

### Physical Security

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Visitor Management Procedure | Physical Security Policy | Medium |
| Equipment Disposal Procedure | Physical Security Policy | Medium |

### Business Continuity

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Business Continuity Testing Procedure | Business Continuity Policy | Medium |

### Cryptography

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Key Management Procedure | Cryptography Policy | High |
| Certificate Management Procedure | Cryptography Policy | Medium |

---

## Procedure Template

Use this structure for all procedures:

```markdown
# [Procedure Name]

## Document Control
| Version | Date | Owner | Status |

## 1. Purpose
Why this procedure exists

## 2. Scope
What it covers

## 3. Prerequisites
What's needed before starting

## 4. Procedure Steps
Numbered steps with clear actions

## 5. Exceptions
How to handle special cases

## 6. Related Documents
Links to policies and other procedures
```

---

## Difference: Policies vs. Procedures

| Aspect | Policy | Procedure |
|--------|--------|-----------|
| Purpose | States what must be done | Explains how to do it |
| Level | High-level principles | Detailed steps |
| Audience | All personnel | Specific roles |
| Change Frequency | Less frequent | More frequent |
| Approval | Executive/Board | Management |
| Example | "Access must be removed immediately upon termination" | "Step 1: HR sends termination notice... Step 2: IT disables account..." |

---

## Contributing

Procedures are the most needed contribution area. See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines on submitting new procedures.

---

[Back to Home](../README.md) | [View Policies](../policies/README.md)

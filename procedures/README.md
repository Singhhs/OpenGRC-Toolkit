# Procedures

This section contains step-by-step operational procedures that implement the requirements defined in policies.

## Available Procedures (7)

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

### ISMS Operations

| Procedure | Related Policy | Status |
|-----------|----------------|--------|
| [Internal Audit Procedure](./internal-audit-procedure.md) | [Information Security Policy](../policies/information-security-policy.md) | Available |

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
| Data Backup Procedure | Backup Policy | High |
| Data Recovery Procedure | Backup Policy | High |
| Data Disposal Procedure | Data Classification Policy | Medium |
| Data Handling Procedure | Data Classification Policy | Medium |

### Change & Operations

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Change Management Procedure | Change Management Policy | High |
| Patch Management Procedure | Vulnerability Management Policy | High |
| Vulnerability Scanning Procedure | Vulnerability Management Policy | Medium |
| Configuration Management Procedure | Change Management Policy | Medium |

### Third Party & Vendor

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Vendor Security Assessment Procedure | Supplier Security Policy | High |
| Vendor Onboarding Procedure | Supplier Security Policy | Medium |

### Physical Security

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Visitor Management Procedure | Physical Security Policy | Medium |
| Equipment Disposal Procedure | Physical Security Policy | Medium |

### ISMS Operations

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Internal Audit Procedure | Information Security Policy | High |
| Management Review Procedure | Information Security Policy | High |
| Corrective Action Procedure | Information Security Policy | High |
| Document Control Procedure | Information Security Policy | Medium |
| Risk Assessment Procedure | Information Security Policy | High |
| Risk Treatment Procedure | Information Security Policy | High |
| Security Awareness Procedure | Information Security Policy | Medium |

### Business Continuity

| Procedure | Related Policy | Priority |
|-----------|----------------|----------|
| Disaster Recovery Procedure | Business Continuity Policy | High |
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

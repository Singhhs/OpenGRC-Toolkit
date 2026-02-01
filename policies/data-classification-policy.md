# Data Classification Policy

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Next Review** | [DATE] |
| **Owner** | [ROLE - e.g., CISO / Data Protection Officer] |
| **Approved By** | [ROLE - e.g., CEO] |
| **Classification** | Internal |

---

## 1. Purpose

This policy establishes a framework for classifying information based on its sensitivity and value to [ORGANIZATION NAME], and defines the handling requirements for each classification level.

## 2. Scope

This policy applies to:
- All information created, received, or maintained by [ORGANIZATION NAME]
- All formats: electronic, paper, verbal
- All personnel handling organizational information

## 3. Classification Levels

### 3.1 Overview

| Level | Label | Description |
|-------|-------|-------------|
| **Public** | PUBLIC | Information approved for public release |
| **Internal** | INTERNAL | General business information for internal use |
| **Confidential** | CONFIDENTIAL | Sensitive business information requiring protection |
| **Restricted** | RESTRICTED | Highly sensitive information with strict access controls |

### 3.2 Classification Definitions

#### 3.2.1 Public

Information approved for public access with no confidentiality requirements.

**Examples:**
- Published marketing materials
- Public website content
- Press releases
- Published annual reports

**Impact if disclosed:** None

---

#### 3.2.2 Internal

General business information not intended for public release but would cause minimal harm if disclosed.

**Examples:**
- Internal policies and procedures
- Organization charts
- Internal announcements
- Non-sensitive meeting minutes

**Impact if disclosed:** Minor embarrassment or inconvenience

---

#### 3.2.3 Confidential

Sensitive information that could cause significant harm to [ORGANIZATION NAME] or its stakeholders if disclosed.

**Examples:**
- Financial data and forecasts
- Business strategies and plans
- Customer lists and contracts
- Employee personal information (HR records)
- Vendor agreements
- Audit reports
- Security assessments

**Impact if disclosed:**
- Financial loss
- Competitive disadvantage
- Reputational damage
- Regulatory penalties

---

#### 3.2.4 Restricted

Highly sensitive information requiring the strictest protection. Unauthorized disclosure could cause severe harm.

**Examples:**
- Trade secrets
- M&A activities
- Legal matters and litigation
- Authentication credentials
- Encryption keys
- Personal data subject to specific regulations (health, financial)
- Security vulnerabilities
- Incident details during active response

**Impact if disclosed:**
- Severe financial loss
- Legal liability
- Major reputational damage
- Regulatory sanctions
- Safety or security risks

## 4. Handling Requirements

### 4.1 Summary Matrix

| Requirement | Public | Internal | Confidential | Restricted |
|-------------|--------|----------|--------------|------------|
| **Labeling Required** | Optional | Yes | Yes | Yes |
| **Access Control** | None | Authenticated users | Need-to-know | Explicit approval |
| **Encryption at Rest** | No | No | Recommended | Required |
| **Encryption in Transit** | No | Recommended | Required | Required |
| **Email** | Unrestricted | Internal OK | Internal only* | Encrypted only |
| **Printing** | Unrestricted | OK | Minimize | Avoid |
| **External Sharing** | OK | With approval | With NDA | With explicit approval |
| **Storage Location** | Any | Approved systems | Approved systems | Designated secure systems |
| **Disposal** | Standard | Standard | Secure deletion | Secure destruction + verification |

*External email requires encryption

### 4.2 Detailed Requirements

#### 4.2.1 Labeling

- **Confidential** and **Restricted** documents must be labeled
- Electronic documents: Header, footer, or watermark
- Paper documents: Header on each page
- Emails: Subject line prefix [CONFIDENTIAL] or [RESTRICTED]
- Storage: Folder/container labels

#### 4.2.2 Access Control

| Level | Access Requirement |
|-------|-------------------|
| Public | No restrictions |
| Internal | Authentication required |
| Confidential | Authentication + role-based access |
| Restricted | Authentication + explicit authorization + audit logging |

#### 4.2.3 Storage

| Level | Allowed Storage |
|-------|-----------------|
| Public | Any location |
| Internal | Approved corporate systems, cloud services |
| Confidential | Approved secure systems, encrypted cloud |
| Restricted | Designated secure systems only, encrypted |

**Not allowed for Confidential/Restricted:**
- Personal cloud storage (Dropbox, personal Google Drive)
- Personal devices without MDM
- Removable media without encryption
- Email attachments to personal accounts

#### 4.2.4 Transmission

| Level | Requirements |
|-------|-------------|
| Public | No restrictions |
| Internal | Use corporate email or approved channels |
| Confidential | Encryption required for external transmission |
| Restricted | Encryption required, approved secure channels only |

#### 4.2.5 Printing and Physical Copies

| Level | Requirements |
|-------|-------------|
| Public | No restrictions |
| Internal | Retrieve promptly from printer |
| Confidential | Use secure print, minimize copies, lock when not in use |
| Restricted | Avoid if possible, secure print, numbered copies, secure storage |

#### 4.2.6 Disposal

| Level | Method |
|-------|--------|
| Public | Standard disposal |
| Internal | Standard disposal |
| Confidential | Secure delete (electronic), cross-cut shred (paper) |
| Restricted | Secure delete with verification, cross-cut shred with witness |

## 5. Classification Process

### 5.1 Who Classifies

| Role | Responsibility |
|------|----------------|
| Information Creator | Initial classification |
| Information Owner | Review and approve classification |
| Data Steward | Ensure consistent classification |
| All Users | Maintain classification when handling |

### 5.2 Classification Decision Guide

```
START
  │
  ├─ Is it approved for public release? ──Yes──→ PUBLIC
  │
  No
  │
  ├─ Would disclosure cause significant harm? ──No──→ INTERNAL
  │
  Yes
  │
  ├─ Is it regulated personal data, trade secret, ──Yes──→ RESTRICTED
  │   security credentials, or highly sensitive?
  │
  No
  │
  └──→ CONFIDENTIAL
```

### 5.3 Reclassification

- Classification may change over time
- Reclassification requires owner approval
- Downgrading Restricted requires [CISO] approval
- Document classification changes

## 6. Roles and Responsibilities

### 6.1 Data/Information Owner
- Assign appropriate classification
- Define access requirements
- Review classification periodically
- Approve access requests

### 6.2 Data Steward
- Implement classification controls
- Monitor compliance
- Support data owners

### 6.3 All Personnel
- Apply correct classification
- Handle data according to requirements
- Report misclassified information
- Protect information in their care

### 6.4 IT/Security
- Implement technical controls
- Monitor and audit compliance
- Provide secure storage solutions
- Support classification tools

## 7. Compliance

### 7.1 Monitoring
- Regular audits of classification practices
- Data loss prevention monitoring
- Access reviews

### 7.2 Violations
Violations may result in:
- Retraining
- Disciplinary action
- Access revocation
- Legal action for serious breaches

## 8. Exceptions

Exceptions require:
- Written justification
- Risk assessment
- Compensating controls
- Approval from [Data Owner] and [CISO]
- Documentation and expiry date

## 9. Related Documents

- [Information Security Policy](./information-security-policy.md)
- [Acceptable Use Policy](./acceptable-use-policy.md)
- [Data Protection Policy](./data-protection-policy.md)
- [Data Handling Procedure](../procedures/data-handling-procedure.md)

## 10. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

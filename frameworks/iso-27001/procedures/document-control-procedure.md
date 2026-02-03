# Document Control Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Owner** | [ROLE - e.g., ISMS Manager, Quality Manager] |
| **Approver** | [ROLE - e.g., CISO, Management Representative] |
| **Review Frequency** | Annual |
| **Classification** | Internal |

---

## 1. Purpose

This procedure defines the process for creating, reviewing, approving, distributing, and managing ISMS documentation at [ORGANIZATION NAME] in accordance with ISO 27001:2022 Clause 7.5 (Documented Information).

## 2. Scope

This procedure applies to all documented information required by:
- The ISO 27001:2022 standard
- The organization's ISMS
- Regulatory and contractual requirements
- Operational security needs

### Document Types Covered

| Type | Description | Examples |
|------|-------------|----------|
| **Policies** | High-level statements of intent and direction | Information Security Policy, Access Control Policy |
| **Procedures** | Step-by-step processes for specific activities | Incident Response Procedure, Change Management Procedure |
| **Standards** | Specific technical or operational requirements | Password standards, Encryption standards |
| **Guidelines** | Recommended practices (non-mandatory) | Secure coding guidelines |
| **Templates** | Standardized forms and formats | Risk register, Incident report form |
| **Records** | Evidence of activities performed | Audit reports, Training records, Risk assessments |

---

## 3. Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| **ISMS Manager** | Maintain document register, coordinate reviews, manage document repository |
| **Document Owner** | Create/update documents, ensure accuracy, initiate reviews |
| **Approver** | Review and formally approve documents before publication |
| **Users** | Use current versions, report issues, follow documented processes |
| **Internal Audit** | Verify document control compliance |

---

## 4. Document Control Requirements

### 4.1 Document Identification

All controlled documents must include:

| Element | Requirement |
|---------|-------------|
| **Title** | Clear, descriptive name |
| **Document ID** | Unique identifier (optional but recommended) |
| **Version** | Current version number |
| **Effective Date** | When document becomes active |
| **Owner** | Role responsible for the document |
| **Classification** | Confidentiality level |
| **Review Date** | When next review is due |

### 4.2 Version Numbering

| Version | When to Use |
|---------|-------------|
| 0.1, 0.2, etc. | Draft versions (not yet approved) |
| 1.0 | First approved release |
| 1.1, 1.2, etc. | Minor updates (clarifications, corrections) |
| 2.0, 3.0, etc. | Major updates (significant changes) |

### 4.3 Document Naming Convention

```
[Type]-[Topic]-[Suffix].md

Examples:
- policy-information-security.md
- procedure-incident-response.md
- standard-password-requirements.md
- template-risk-register.md
```

---

## 5. Document Lifecycle

### 5.1 Process Overview

```
┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐
│  Create  │───▶│  Review  │───▶│ Approve  │───▶│ Publish  │
└──────────┘    └──────────┘    └──────────┘    └──────────┘
                                                      │
      ┌───────────────────────────────────────────────┘
      │
      ▼
┌──────────┐    ┌──────────┐    ┌──────────┐
│   Use    │───▶│ Periodic │───▶│  Update  │───▶ [Back to Review]
│          │    │  Review  │    │   or     │
└──────────┘    └──────────┘    │  Retire  │
                                └──────────┘
```

### 5.2 Document Creation

```
□ Step 1: Identify need for new document
  □ Gap identified in ISMS documentation
  □ New process or control requires documentation
  □ Regulatory or standard requirement
  □ Stakeholder request

□ Step 2: Assign document owner
  □ Subject matter expert identified
  □ Owner accepts responsibility
  □ Timeline agreed

□ Step 3: Draft document
  □ Use appropriate template
  □ Include all required elements
  □ Follow naming conventions
  □ Apply correct classification
  □ Mark as DRAFT

□ Step 4: Internal review
  □ Technical accuracy review
  □ Compliance review (if applicable)
  □ Stakeholder review
  □ Incorporate feedback
```

### 5.3 Document Review

```
□ Step 5: Submit for review
  □ Document complete and formatted
  □ Submitted to ISMS Manager
  □ Reviewers identified

□ Step 6: Review process
  □ Reviewers assess:
    - Accuracy and completeness
    - Alignment with policies/standards
    - Compliance requirements
    - Practical implementability
  □ Feedback provided to owner
  □ Owner addresses feedback
  □ Re-review if significant changes
```

### 5.4 Document Approval

```
□ Step 7: Approval
  □ Final version submitted for approval
  □ Appropriate approver identified:

  | Document Type | Approver |
  |---------------|----------|
  | Policies | [Executive Management / CISO] |
  | Procedures | [CISO / Department Head] |
  | Standards | [CISO / Technical Lead] |
  | Guidelines | [Document Owner / Manager] |

  □ Approver reviews and signs off
  □ Approval recorded
  □ Version number assigned (remove DRAFT)
```

### 5.5 Document Publication

```
□ Step 8: Publish document
  □ Add to document repository
  □ Update document register
  □ Remove/archive previous version
  □ Notify relevant stakeholders
  □ Update links/references as needed
```

### 5.6 Document Communication

| Document Type | Communication Method | Audience |
|---------------|---------------------|----------|
| New Policy | Email + meeting | All affected staff |
| Updated Policy | Email notification | All affected staff |
| New Procedure | Email + training | Users of procedure |
| Updated Procedure | Email notification | Users of procedure |
| Standards/Guidelines | Email notification | Technical teams |

### 5.7 Periodic Review

```
□ Step 9: Scheduled review

  Review Triggers:
  □ Scheduled review date reached
  □ Significant organizational change
  □ Regulatory/standard change
  □ Incident highlighting gap
  □ Audit finding
  □ Stakeholder feedback

  Review Process:
  □ Document owner notified of due review
  □ Owner assesses document currency:
    - Still accurate?
    - Still relevant?
    - Changes needed?
    - References current?
  □ If no changes: Update review date, re-approve
  □ If changes needed: Return to Step 3
  □ If obsolete: Proceed to retirement
```

### 5.8 Document Retirement

```
□ Step 10: Retire obsolete document
  □ Confirm document no longer required
  □ Approval for retirement
  □ Remove from active repository
  □ Move to archive (retain per retention schedule)
  □ Update document register
  □ Update/remove references in other documents
  □ Notify users of retirement
```

---

## 6. Document Repository

### 6.1 Repository Structure

```
/ISMS Documents
  /Policies
    - Information Security Policy
    - Access Control Policy
    - [etc.]
  /Procedures
    - Incident Response Procedure
    - [etc.]
  /Standards
  /Guidelines
  /Templates
  /Records
    /Risk Assessments
    /Audit Reports
    /Training Records
    /Incident Records
  /Archive
    /Superseded Documents
    /Retired Documents
```

### 6.2 Access Control

| Document Type | Access Level |
|---------------|--------------|
| Policies | All employees (read) |
| Procedures | Relevant staff (read) |
| Standards | Technical staff (read) |
| Templates | As needed (read/use) |
| Records | Restricted (need to know) |
| Archive | ISMS team + audit |

### 6.3 Repository Requirements

- [ ] Version control enabled
- [ ] Access controls configured
- [ ] Backup included in organizational backup
- [ ] Search functionality available
- [ ] Audit trail of changes
- [ ] Single source of truth (one master location)

---

## 7. Document Register

Maintain a register of all controlled documents:

| Field | Description |
|-------|-------------|
| Document ID | Unique identifier |
| Document Title | Full document name |
| Document Type | Policy/Procedure/Standard/etc. |
| Version | Current version number |
| Owner | Responsible role |
| Approver | Who approved |
| Effective Date | When current version became active |
| Review Date | When next review due |
| Status | Active/Draft/Retired |
| Location | Where document is stored |

### Sample Register Entry

| ID | Title | Type | Version | Owner | Effective | Review Due | Status |
|----|-------|------|---------|-------|-----------|------------|--------|
| POL-001 | Information Security Policy | Policy | 2.0 | CISO | 2024-01-15 | 2025-01-15 | Active |
| PRO-005 | Incident Response Procedure | Procedure | 1.2 | Security Manager | 2024-03-01 | 2025-03-01 | Active |

---

## 8. Control of External Documents

### 8.1 External Documents

External documents that affect the ISMS must be identified and controlled:

- ISO 27001 standard
- Applicable laws and regulations
- Contractual requirements
- Vendor documentation
- Industry standards (NIST, CIS, etc.)

### 8.2 External Document Management

```
□ Identify required external documents
□ Obtain authorized copies
□ Maintain current versions
□ Store in accessible location
□ Track updates/new versions
□ Communicate relevant changes to staff
```

---

## 9. Control of Records

### 9.1 Record Types

| Record Type | Examples | Retention |
|-------------|----------|-----------|
| Risk assessments | Risk registers, treatment plans | 5 years minimum |
| Audit records | Internal audit reports, findings | 5 years minimum |
| Training records | Attendance, completion certificates | Duration of employment + 2 years |
| Incident records | Incident reports, investigations | 5 years minimum |
| Access records | Access reviews, approvals | 3 years minimum |
| Change records | Change requests, approvals | 3 years minimum |
| Management reviews | Meeting minutes, decisions | 5 years minimum |

### 9.2 Record Requirements

Records must be:
- **Legible** - Readable and understandable
- **Identifiable** - Clear what they relate to
- **Retrievable** - Can be found when needed
- **Protected** - Secured appropriately
- **Retained** - Kept for required period
- **Disposed** - Securely destroyed when retention expires

---

## 10. Document Templates

### 10.1 Policy Template Structure

```markdown
# [Policy Name]

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Owner** | [ROLE] |
| **Approver** | [ROLE] |
| **Classification** | [LEVEL] |

## 1. Purpose
## 2. Scope
## 3. Policy Statements
## 4. Roles and Responsibilities
## 5. Compliance
## 6. Related Documents
## 7. Document History
```

### 10.2 Procedure Template Structure

```markdown
# [Procedure Name]

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Owner** | [ROLE] |

## 1. Purpose
## 2. Scope
## 3. Responsibilities
## 4. Procedure Steps
## 5. Related Documents
## 6. Document History
```

---

## 11. Monitoring and Metrics

### 11.1 Key Metrics

| Metric | Target | Frequency |
|--------|--------|-----------|
| Documents reviewed on schedule | 100% | Quarterly |
| Overdue document reviews | 0 | Monthly |
| Average time to approve new documents | < 2 weeks | Quarterly |
| Documents with identified owner | 100% | Quarterly |

### 11.2 Document Control Review

Annually review:
- Document register completeness
- Review schedule compliance
- Repository organization
- Access control effectiveness
- User compliance with procedures

---

## 12. Related Documents

- [Information Security Policy](../../../policies/information-security-policy.md)
- [ISMS Scope](../isms-scope.md)
- [Internal Audit Procedure](../../../procedures/internal-audit-procedure.md)
- [Management Review Procedure](./management-review-procedure.md)

---

## 13. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |
| 2.0 | [DATE] | [AUTHOR] | Comprehensive update - added lifecycle, register, templates |

---

[Back to ISO 27001 Procedures](./README.md) | [Back to ISO 27001](../README.md)

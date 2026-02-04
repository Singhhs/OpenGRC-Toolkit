# SOC 2 Evidence Collection Guide

A guide for collecting and organizing evidence for SOC 2 audits.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE] |
| **Classification** | Internal |

---

## 1. Introduction

### 1.1 Purpose

This guide helps organizations prepare evidence for SOC 2 audits by:
- Identifying evidence requirements by control area
- Defining evidence quality standards
- Providing evidence collection templates
- Establishing organization and retention practices

### 1.2 Evidence Types

| Type | Description | Examples |
|------|-------------|----------|
| **Inquiry** | Verbal/written responses to auditor questions | Interview notes |
| **Observation** | Auditor directly observes process | Walkthroughs |
| **Inspection** | Review of documents and records | Policies, logs, reports |
| **Re-performance** | Auditor performs the control | Testing access controls |

### 1.3 Evidence Quality

Evidence should be:

| Attribute | Description |
|-----------|-------------|
| **Relevant** | Directly addresses the control objective |
| **Reliable** | From authoritative source, tamper-resistant |
| **Sufficient** | Enough to support the conclusion |
| **Timely** | Within the audit period (Type II) |

---

## 2. Evidence by Common Criteria

### CC1 - Control Environment

#### CC1.1-CC1.5 - Governance and Ethics

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Code of conduct | Current policy document | PDF |
| Code acknowledgment | Sample acknowledgment records | Screenshot/report |
| Organizational chart | Current org chart | PDF/Image |
| Board/committee charter | Charter document | PDF |
| Board meeting minutes | Meeting minutes (redacted if needed) | PDF |
| Background checks | Sample check results or attestation | Report |
| Job descriptions | Sample job descriptions | PDF |
| Performance reviews | Sample reviews (redacted) | PDF |

---

### CC2 - Communication and Information

#### CC2.1-CC2.3 - Communication

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Security policies | All security policy documents | PDF |
| Policy communication | Distribution records, intranet screenshots | Screenshot |
| Security awareness training | Training materials | PDF/Slides |
| Training completion | Completion report with dates | Report |
| Incident reporting mechanism | Procedure, hotline/email | PDF/Screenshot |
| External security page | Website security/trust page | Screenshot |
| Customer notifications | Sample customer communication | Email/PDF |

---

### CC3 - Risk Assessment

#### CC3.1-CC3.4 - Risk Management

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Risk assessment methodology | Process/procedure document | PDF |
| Risk assessment | Completed risk assessment | PDF/Spreadsheet |
| Risk register | Current risk register | Spreadsheet |
| Risk treatment plans | Treatment documentation | PDF |
| Fraud risk assessment | Fraud risk documentation | PDF |
| Change impact assessments | Sample assessment records | PDF |

---

### CC4 - Monitoring Activities

#### CC4.1-CC4.2 - Monitoring

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Internal audit program | Audit plan/schedule | PDF |
| Internal audit reports | Sample audit reports | PDF |
| Vulnerability scan reports | Sample scan results | Report |
| Penetration test report | Annual pentest report | PDF |
| Issue tracking system | Screenshot of tracking system | Screenshot |
| Remediation records | Sample remediation evidence | Screenshot |
| Management review minutes | Review meeting records | PDF |

---

### CC5 - Control Activities

#### CC5.1-CC5.3 - Controls

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Control documentation | Control matrix or catalog | Spreadsheet |
| Policy review records | Review approval records | PDF/Screenshot |
| Segregation of duties matrix | RACI or duty matrix | Spreadsheet |
| Procedure documentation | Sample procedures | PDF |

---

### CC6 - Logical and Physical Access

#### CC6.1 - Access Security

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Asset inventory | Hardware/software inventory | Spreadsheet |
| Network diagram | Current network architecture | Diagram |
| Firewall configuration | Firewall rules (sanitized) | Screenshot/Export |
| Encryption configuration | TLS/SSL configuration evidence | Screenshot |
| Key management procedures | Key management documentation | PDF |

#### CC6.2-CC6.3 - Access Management

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Access request form/workflow | Sample access requests | Screenshot |
| Access approval evidence | Approved request samples | Screenshot |
| User access list | System user listings | Report |
| Access review records | Quarterly review documentation | Spreadsheet/PDF |
| Termination evidence | Sample termination/revocation | Screenshot |
| Termination checklist | Completed checklists | PDF |

#### CC6.4 - Physical Access

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Physical access policy | Policy document | PDF |
| Badge/key inventory | Access device inventory | Spreadsheet |
| Physical access logs | Sample access logs | Report |
| Visitor logs | Sample visitor records | PDF/Screenshot |
| Data center access list | Authorized personnel list | Report |

#### CC6.5-CC6.8 - Security Controls

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Endpoint protection deployment | Deployment report | Report |
| Anti-malware definitions | Update status report | Screenshot |
| IDS/IPS configuration | Configuration evidence | Screenshot |
| DLP configuration | DLP policy configuration | Screenshot |
| Software restriction policies | GPO or configuration | Screenshot |

---

### CC7 - System Operations

#### CC7.1-CC7.2 - Monitoring

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| SIEM configuration | SIEM dashboard/configuration | Screenshot |
| Alert configuration | Sample alerts | Screenshot |
| Log retention settings | Retention configuration | Screenshot |
| Log samples | Sample security logs | Export |
| Monitoring procedures | Monitoring runbook | PDF |

#### CC7.3-CC7.5 - Incident Response

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Incident response plan | IRP document | PDF |
| Incident response team roster | Team contact list | PDF |
| Incident classification matrix | Classification criteria | PDF |
| Sample incident tickets | Redacted incident records | Screenshot |
| Post-incident reviews | Sample PIR/lessons learned | PDF |
| BCP/DR plan | Continuity plans | PDF |
| DR test results | Test execution records | PDF |
| Backup configuration | Backup job configuration | Screenshot |
| Backup restoration test | Restoration test records | PDF |

---

### CC8 - Change Management

#### CC8.1 - Change Control

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Change management policy | Policy document | PDF |
| Change request samples | Sample change tickets | Screenshot |
| Change approval evidence | Approval records | Screenshot |
| Testing evidence | Test results documentation | Screenshot/PDF |
| Deployment records | Deployment logs/tickets | Screenshot |
| Emergency change samples | Emergency change records | Screenshot |
| Code review evidence | PR/code review records | Screenshot |
| Version control | Repository screenshots | Screenshot |

---

### CC9 - Risk Mitigation

#### CC9.1-CC9.2 - Vendor Management

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Vendor management policy | Policy document | PDF |
| Vendor inventory | Vendor list with classifications | Spreadsheet |
| Vendor assessment questionnaires | Sample assessments | PDF |
| Vendor SOC reports | SOC 2 reports from vendors | PDF |
| Vendor contracts | Sample contract (redacted) | PDF |
| Vendor review records | Annual review documentation | PDF |

---

## 3. Availability Evidence

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| SLA documentation | SLA/SLO definitions | PDF |
| Uptime reports | Monitoring/uptime data | Report |
| Capacity planning | Capacity analysis | PDF/Spreadsheet |
| Performance monitoring | Dashboards, alerts | Screenshot |
| Redundancy documentation | Architecture showing redundancy | Diagram |
| Failover test results | Failover test records | PDF |
| Environmental monitoring | Monitoring configuration | Screenshot |
| UPS/generator testing | Test/maintenance records | PDF |

---

## 4. Processing Integrity Evidence

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Processing procedures | Process documentation | PDF |
| Input validation rules | Validation configuration | Screenshot |
| Error handling procedures | Error handling documentation | PDF |
| Reconciliation records | Sample reconciliations | Spreadsheet |
| Audit trails | Sample audit logs | Export |
| Data quality reports | Quality metrics | Report |

---

## 5. Confidentiality Evidence

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Data classification policy | Policy document | PDF |
| Classification inventory | Data classification matrix | Spreadsheet |
| NDA templates | NDA samples | PDF |
| Confidential data access controls | Access restrictions | Screenshot |
| Data disposal records | Disposal certificates | PDF |

---

## 6. Privacy Evidence

| Control | Evidence Required | Format |
|---------|-------------------|--------|
| Privacy policy | Published privacy policy | PDF/Screenshot |
| Privacy notice | Notice provided to users | Screenshot |
| Consent mechanisms | Consent collection evidence | Screenshot |
| Data subject request procedure | Procedure documentation | PDF |
| DSAR fulfillment records | Sample request handling | Screenshot |
| Data retention schedule | Retention matrix | Spreadsheet |
| Breach notification procedures | Notification procedure | PDF |

---

## 7. Evidence Organization

### 7.1 Folder Structure

```
/SOC2_Evidence
├── /CC1_Control_Environment
│   ├── /CC1.1_Integrity_Ethics
│   │   ├── code_of_conduct.pdf
│   │   └── acknowledgments/
│   ├── /CC1.2_Board_Oversight
│   └── ...
├── /CC2_Communication
├── /CC3_Risk_Assessment
├── /CC4_Monitoring
├── /CC5_Control_Activities
├── /CC6_Logical_Physical_Access
├── /CC7_System_Operations
├── /CC8_Change_Management
├── /CC9_Risk_Mitigation
├── /Availability (if in scope)
├── /Processing_Integrity (if in scope)
├── /Confidentiality (if in scope)
├── /Privacy (if in scope)
└── /System_Description
```

### 7.2 Naming Convention

```
[Criteria]_[Control]_[Description]_[Date].[ext]

Examples:
CC6.2_Access_Request_Sample_2024-01.pdf
CC7.4_Incident_Ticket_INC-1234_2024-02.png
CC8.1_Change_Approval_CHG-5678_2024-03.pdf
```

### 7.3 Evidence Log

Track all evidence in a master log:

| Criteria | Control | Evidence Description | File Name | Date Collected | Source | Collected By |
|----------|---------|---------------------|-----------|----------------|--------|--------------|
| CC6.2 | Access provisioning | Access request sample | CC6.2_AccessReq_2024-01.pdf | 2024-01-15 | ServiceNow | J. Smith |

---

## 8. Type II Sampling

### 8.1 Sample Sizes

For Type II audits, auditors will sample evidence across the audit period:

| Population Size | Minimum Sample |
|-----------------|----------------|
| 1-10 | All items |
| 11-50 | 10-15 |
| 51-100 | 15-25 |
| 101-250 | 25-30 |
| 251+ | 30-40 |

### 8.2 Population Documentation

Document populations for sampling:

| Control | Population | Count | Audit Period | Source System |
|---------|------------|-------|--------------|---------------|
| Access requests | New user requests | 150 | Jan-Dec | ServiceNow |
| Changes | Production changes | 200 | Jan-Dec | Jira |
| Incidents | Security incidents | 25 | Jan-Dec | PagerDuty |
| Terminations | Employee terminations | 30 | Jan-Dec | Workday |

---

## 9. Common Evidence Issues

### 9.1 Issues to Avoid

| Issue | Problem | Solution |
|-------|---------|----------|
| Missing dates | Can't verify timing | Ensure dates visible in screenshots |
| Partial screenshots | Control not fully visible | Capture complete evidence |
| Inconsistent periods | Evidence from different timeframes | Align to audit period |
| Redacted too heavily | Auditor can't verify | Discuss with auditor first |
| Stale evidence | Evidence from before audit period | Collect fresh evidence |
| Missing approvals | Can't verify authorization | Ensure approval visible |

### 9.2 Quality Checklist

Before submitting evidence:

```
□ Date/timestamp visible
□ Complete and unedited (except approved redactions)
□ Within audit period (Type II)
□ From authoritative source
□ Clearly demonstrates control
□ File named consistently
□ Logged in evidence tracker
```

---

## 10. Evidence Request Process

### 10.1 Typical Request Flow

```
Auditor Request → Evidence Owner Identified → Evidence Collected
        ↓                    ↓                       ↓
Review Request        Gather Evidence         Quality Check
        ↓                    ↓                       ↓
Clarify if Needed    Redact if Needed        Submit to Auditor
```

### 10.2 Request Tracking

| Request ID | Criteria | Request | Owner | Due Date | Status | Notes |
|------------|----------|---------|-------|----------|--------|-------|
| REQ-001 | CC6.2 | 10 access request samples | IT | 2024-03-01 | Complete | |
| REQ-002 | CC8.1 | 15 change ticket samples | DevOps | 2024-03-05 | In Progress | |

---

## 11. Related Documents

- [SOC 2 Guide](./soc2-guide.md)
- [Trust Service Criteria Reference](./trust-services-criteria.md)
- [SOC 2 Readiness Checklist](./soc2-readiness-checklist.md)
- [SOC 2 Gap Assessment](./soc2-gap-assessment.md)

---

## 12. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to SOC 2](./README.md) | [Back to Frameworks](../README.md)

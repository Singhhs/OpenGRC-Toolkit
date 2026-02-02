# Third-Party / Supply Chain Breach Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides step-by-step guidance for responding to security breaches at third-party vendors, suppliers, or partners that may impact [ORGANIZATION NAME].

### Scenarios Covered
- Vendor data breach affecting our data
- Compromised software/service we use
- Supply chain attack (SolarWinds-style)
- Cloud service provider breach
- Managed service provider compromise
- Partner system compromise
- Vendor credential compromise

---

## 2. Detection Indicators

### 2.1 External Notification

| Source | Type |
|--------|------|
| Vendor notification | Direct breach notification from vendor |
| News/media reports | Public disclosure of vendor breach |
| Regulatory notification | Notification from authorities |
| Security researcher | Public vulnerability disclosure |
| Threat intelligence | IoCs related to vendor |
| Customer report | Third party reports issue |

### 2.2 Internal Detection

| Indicator | Description |
|-----------|-------------|
| Suspicious vendor activity | Unusual access from vendor connections |
| Software anomalies | Unexpected behavior in vendor software |
| Network indicators | Traffic to known malicious infrastructure |
| Malware detection | Detection linked to vendor software |
| Authentication anomalies | Suspicious vendor account activity |

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Our sensitive data breached, active attack via vendor, critical vendor compromised | Immediate, all hands |
| **P2 High** | Potential data exposure, high-risk vendor affected, software we use compromised | Priority response |
| **P3 Medium** | Limited data exposure, non-critical vendor, patch available | Standard response |
| **P4 Low** | Vendor breach but no data shared, minimal integration | Monitor and assess |

### Vendor Risk Factors

| Factor | Impact |
|--------|--------|
| Data shared with vendor | Higher if sensitive/personal data |
| System access | Higher if direct system access |
| Integration depth | Higher if deeply integrated |
| Business criticality | Higher if critical service |
| Credential sharing | Higher if credentials exposed |

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Incident Commander | Overall coordination | [NAME/PHONE] |
| Security Lead | Technical assessment | [NAME/PHONE] |
| Vendor Manager | Vendor communication | [NAME/PHONE] |
| Legal Counsel | Legal/regulatory matters | [NAME/PHONE] |
| Privacy Officer | Data protection implications | [NAME/PHONE] |
| Communications | Internal/external comms | [NAME/PHONE] |
| Procurement | Contract matters | [NAME/PHONE] |

---

## 5. Immediate Actions (First 1-2 Hours)

### 5.1 Gather Information

```
□ Step 1: Collect initial information about the breach

  From Notification/Report:
  □ What vendor is affected?
  □ What type of breach occurred?
  □ When did it occur / when discovered?
  □ What systems/data affected?
  □ Is our data/systems specifically impacted?
  □ What is vendor doing about it?

□ Step 2: Identify our relationship with vendor
  □ What data do we share with them?
  □ What access do they have to our systems?
  □ What systems/software do we use from them?
  □ How critical is this vendor?
  □ Who is our vendor contact?
  □ Review vendor security assessment
```

### 5.2 Initial Assessment

```
□ Step 3: Assess potential impact to our organization

  Data Exposure Questions:
  □ Do we share data with this vendor?
  □ What types of data? (PII, financial, confidential)
  □ How much data?
  □ Is our data confirmed breached or potentially exposed?

  System Exposure Questions:
  □ Does vendor have access to our systems?
  □ What level of access?
  □ Do we use their software/services?
  □ Could their systems be used to attack ours?

□ Step 4: Make containment decision
  - Is immediate action needed?
  - Can we wait for more information?
  - What's the risk of inaction?
```

---

## 6. Containment

### 6.1 Vendor Access Containment

```
□ Step 5: Review and restrict vendor access

  If Vendor Has System Access:
  □ Disable vendor VPN accounts
  □ Revoke vendor user accounts
  □ Block vendor IP ranges (if known)
  □ Disable API connections
  □ Revoke OAuth tokens
  □ Suspend automated integrations
  □ Review vendor admin accounts

  Document:
  □ What access was disabled
  □ When disabled
  □ Business impact of disabling
```

### 6.2 Software/Service Containment

```
□ Step 6: Address compromised software/service

  If Using Compromised Vendor Software:
  □ Check if we have affected version
  □ Check for IoCs on our systems
  □ Isolate systems running affected software
  □ Block outbound connections from software
  □ Apply emergency patches if available
  □ Consider disabling software temporarily

  If Using Compromised Cloud Service:
  □ Review recent activity in service
  □ Rotate credentials/API keys
  □ Review data access logs
  □ Check for data exfiltration
  □ Consider temporary disconnection
```

### 6.3 Credential Rotation

```
□ Step 7: Rotate shared credentials

  Identify and Rotate:
  □ Credentials shared with vendor
  □ API keys used with vendor
  □ Certificates for vendor connections
  □ Passwords for shared accounts
  □ Integration credentials
  □ Database connection strings

  Track:
  □ What was rotated
  □ Any systems affected by rotation
  □ When rotation completed
```

---

## 7. Investigation

### 7.1 Vendor Communication

```
□ Step 8: Engage with vendor

  Information to Request:
  □ Official breach notification (written)
  □ Detailed incident timeline
  □ Specific data/systems affected
  □ Confirmation if our data involved
  □ Root cause (when known)
  □ Remediation actions taken
  □ Future prevention measures
  □ Point of contact for updates
  □ Regulatory notifications they've made

  Document All Communications:
  □ Date/time of communication
  □ Who participated
  □ Information provided
  □ Commitments made
```

### 7.2 Internal Investigation

```
□ Step 9: Check for indicators of compromise

  Log Analysis:
  □ Review vendor access logs
  □ Check for anomalous vendor activity
  □ Review authentication logs
  □ Check data access patterns
  □ Look for IoCs (if provided)

  System Checks:
  □ Scan systems for malware/backdoors
  □ Check for unauthorized changes
  □ Review integrity of vendor software
  □ Check for unexpected network connections

□ Step 10: Assess data impact
  □ What specific data may be exposed?
  □ How many records/individuals?
  □ Data classification?
  □ Regulatory implications?
```

### 7.3 Supply Chain Attack Assessment

```
□ Step 11: For supply chain attacks (compromised software)

  Additional Checks:
  □ When did we install affected version?
  □ What systems have affected software?
  □ What did software have access to?
  □ Signs of exploitation?
  □ Lateral movement from affected systems?
  □ Data exfiltration indicators?

  Consider Full Compromise:
  □ Assume affected systems are compromised
  □ Treat as internal breach
  □ Follow malware/breach playbooks
```

---

## 8. Remediation

### 8.1 Addressing Compromised Software

```
□ Step 12: Remediate affected software

  Options (in order of preference):
  1. Apply vendor security patch
  2. Roll back to unaffected version
  3. Remove and reinstall clean version
  4. Remove software entirely

  Verification:
  □ Scan cleaned systems
  □ Monitor for reinfection
  □ Verify patch effectiveness
```

### 8.2 Restoring Vendor Relationship

```
□ Step 13: Plan vendor access restoration

  Before Restoring Access:
  □ Written confirmation breach is contained
  □ Root cause identified and addressed
  □ Enhanced security measures implemented
  □ Review and minimize access needed
  □ Enhanced monitoring in place
  □ Updated contract/security terms (if needed)
  □ Management approval to restore
```

---

## 9. Data Breach Considerations

### 9.1 If Our Data Was Breached

```
□ Step 14: Activate data breach response

  Refer to: [Data Breach Playbook](./data-breach-playbook.md)

  Key Actions:
  □ Assess data breach scope
  □ Determine notification requirements
  □ Engage legal counsel
  □ Engage privacy officer
  □ Plan affected individual notification
  □ Prepare regulatory notifications
  □ Consider credit monitoring offerings
```

### 9.2 Regulatory Notifications

| Regulation | Requirement | Timeline |
|------------|-------------|----------|
| GDPR | Report to DPA if risk to individuals | 72 hours |
| CCPA | Notify affected California residents | Without unreasonable delay |
| HIPAA | Notify HHS, individuals, media (if large) | 60 days |
| State laws | Varies by state | Varies |
| Contractual | Per customer contracts | Per contract |

---

## 10. Communication

### 10.1 Internal Communication

| Audience | When | Content |
|----------|------|---------|
| Response Team | Immediately | Incident details, assignments |
| IT Teams | As needed | Technical impact, actions required |
| Business Owners | If vendor disruption | Impact to services |
| Executive Team | P1/P2 immediately | Situation summary, decisions needed |
| Legal/Compliance | Immediately if data breach | Regulatory implications |
| All Staff | If action required | Guidance, awareness |

### 10.2 External Communication

| Audience | When | Owner |
|----------|------|-------|
| Vendor | Ongoing | Vendor Manager |
| Customers | If their data affected | Communications + Legal |
| Regulators | If required | Legal + Privacy |
| Partners | If they're affected | Business + Communications |
| Media | If public, as needed | Communications |

### 10.3 Communication Templates

**Internal Announcement:**
```
Subject: Security Incident - Third Party Vendor [NAME]

Team,

We have been notified that [VENDOR NAME], a vendor we work with,
has experienced a security incident.

What We Know:
- [Brief description of vendor incident]
- We are assessing potential impact to our organization
- [Whether our data/systems are believed to be affected]

What We're Doing:
- Investigating potential exposure
- [Containment actions taken]
- Working with the vendor for information

What You Should Do:
- [Any actions required]
- Report any suspicious activity to IT Security
- Do not discuss externally

We will provide updates as we learn more.

IT Security Team
```

---

## 11. Post-Incident

### 11.1 Vendor Review

```
□ Step 15: Conduct vendor security review

  Assessment:
  □ How did breach occur?
  □ Were security controls adequate?
  □ How did vendor respond?
  □ Did they meet contractual obligations?
  □ Do we have confidence in future security?

  Actions:
  □ Update vendor risk rating
  □ Require additional security measures
  □ Enhance monitoring of vendor
  □ Consider contract amendments
  □ Consider alternative vendors
  □ Update vendor security questionnaire
```

### 11.2 Internal Improvements

```
□ Step 16: Improve third-party risk management

  Review and Improve:
  □ Vendor assessment process
  □ Minimum security requirements
  □ Monitoring of vendor access
  □ Data sharing controls
  □ Contract security requirements
  □ Incident notification requirements
  □ Right to audit clauses
```

### 11.3 Documentation

```
□ Step 17: Complete documentation

  Incident Record:
  □ Complete timeline
  □ Vendor communications
  □ Actions taken
  □ Impact assessment
  □ Regulatory notifications
  □ Customer notifications
  □ Lessons learned
```

---

## 12. Vendor Inventory Reference

### 12.1 Critical Vendors Requiring Immediate Response

| Vendor | Services | Data Shared | Access Level | Contact |
|--------|----------|-------------|--------------|---------|
| [Vendor 1] | [Services] | [Data types] | [Level] | [Contact] |
| [Vendor 2] | [Services] | [Data types] | [Level] | [Contact] |
| [Add critical vendors] | | | | |

### 12.2 Vendor Access Quick Reference

| Access Type | How to Disable | Who Can Disable |
|-------------|----------------|-----------------|
| VPN | [Process] | [Team/Person] |
| API | [Process] | [Team/Person] |
| User Accounts | [Process] | [Team/Person] |
| Network | [Process] | [Team/Person] |

---

## 13. Escalation Matrix

| Condition | Escalate To | Contact |
|-----------|-------------|---------|
| Critical vendor breach | CISO + CIO | [PHONE] |
| Our data confirmed breached | Legal + Privacy | [PHONE] |
| Regulatory notification needed | Legal + Compliance | [PHONE] |
| Media inquiry | Communications | [PHONE] |
| Customer notification needed | Executive + Legal | [PHONE] |

---

## 14. Related Documents

- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Supplier Security Policy](../../policies/supplier-security-policy.md)
- [Data Breach Playbook](./data-breach-playbook.md)
- [Data Protection Policy](../../policies/data-protection-policy.md)
- [Vendor Security Assessment Procedure](../../procedures/vendor-security-assessment-procedure.md)

---

## 15. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

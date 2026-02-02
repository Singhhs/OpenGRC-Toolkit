# Vendor Security Assessment Checklist

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Date** | [DATE] |
| **Assessor** | [NAME] |
| **Vendor Name** | [VENDOR] |
| **Assessment Type** | ☐ Initial ☐ Renewal ☐ Periodic |

---

## Purpose

Use this checklist to assess the security posture of vendors and third parties before engagement or during periodic reviews. Adjust scope based on vendor risk tier.

---

## Section 1: Vendor Information

| Field | Information |
|-------|-------------|
| Vendor Name | |
| Primary Contact | |
| Services Provided | |
| Data Types Accessed | |
| Systems Accessed | |
| Contract Value | |
| Contract Duration | |
| Risk Tier | ☐ Critical ☐ High ☐ Medium ☐ Low |

---

## Section 2: Security Governance

### 2.1 Security Program

| # | Question | Response | Evidence | Notes |
|---|----------|----------|----------|-------|
| 2.1.1 | Does the vendor have a documented information security policy? | ☐ Yes ☐ No ☐ Partial | | |
| 2.1.2 | Is there a designated security officer or team? | ☐ Yes ☐ No | | |
| 2.1.3 | Are security roles and responsibilities defined? | ☐ Yes ☐ No ☐ Partial | | |
| 2.1.4 | Is there executive/board oversight of security? | ☐ Yes ☐ No | | |
| 2.1.5 | Does the vendor conduct regular security risk assessments? | ☐ Yes ☐ No ☐ Partial | | |

### 2.2 Certifications and Audits

| # | Certification/Audit | Status | Expiry Date | Scope Covers Service |
|---|---------------------|--------|-------------|---------------------|
| 2.2.1 | ISO 27001 | ☐ Yes ☐ No ☐ In Progress | | ☐ Yes ☐ No ☐ Partial |
| 2.2.2 | SOC 2 Type II | ☐ Yes ☐ No ☐ In Progress | | ☐ Yes ☐ No ☐ Partial |
| 2.2.3 | SOC 1 Type II | ☐ Yes ☐ No ☐ In Progress | | ☐ Yes ☐ No ☐ Partial |
| 2.2.4 | PCI DSS | ☐ Yes ☐ No ☐ N/A | | ☐ Yes ☐ No ☐ Partial |
| 2.2.5 | HIPAA | ☐ Yes ☐ No ☐ N/A | | ☐ Yes ☐ No ☐ Partial |
| 2.2.6 | Other: _______ | ☐ Yes ☐ No | | |

### 2.3 Third-Party Risk

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 2.3.1 | Does the vendor use subcontractors for the service? | ☐ Yes ☐ No | |
| 2.3.2 | Are subcontractors subject to same security requirements? | ☐ Yes ☐ No ☐ N/A | |
| 2.3.3 | Can vendor provide list of material subcontractors? | ☐ Yes ☐ No | |
| 2.3.4 | Will vendor notify of subcontractor changes? | ☐ Yes ☐ No | |

---

## Section 3: Access Control

### 3.1 Authentication

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 3.1.1 | Is multi-factor authentication (MFA) required for access to systems/data? | ☐ Yes ☐ No ☐ Partial | |
| 3.1.2 | Are there password complexity requirements? | ☐ Yes ☐ No | |
| 3.1.3 | Is there account lockout after failed attempts? | ☐ Yes ☐ No | |
| 3.1.4 | Are default credentials changed? | ☐ Yes ☐ No | |
| 3.1.5 | Is single sign-on (SSO) supported? | ☐ Yes ☐ No | |

### 3.2 Authorization

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 3.2.1 | Is access based on least privilege principle? | ☐ Yes ☐ No ☐ Partial | |
| 3.2.2 | Is role-based access control (RBAC) implemented? | ☐ Yes ☐ No | |
| 3.2.3 | Are access rights reviewed periodically? | ☐ Yes ☐ No | Frequency: |
| 3.2.4 | Is privileged access restricted and monitored? | ☐ Yes ☐ No ☐ Partial | |
| 3.2.5 | Is access removed promptly on termination? | ☐ Yes ☐ No | Timeframe: |

---

## Section 4: Data Protection

### 4.1 Data Handling

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 4.1.1 | Is data classified according to sensitivity? | ☐ Yes ☐ No ☐ Partial | |
| 4.1.2 | Are there data handling procedures? | ☐ Yes ☐ No | |
| 4.1.3 | Is data segregated from other customers? | ☐ Yes ☐ No | Method: |
| 4.1.4 | Is data location(s) known and documented? | ☐ Yes ☐ No | Locations: |
| 4.1.5 | Are there data retention and deletion policies? | ☐ Yes ☐ No | |

### 4.2 Encryption

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 4.2.1 | Is data encrypted in transit? | ☐ Yes ☐ No ☐ Partial | Protocol: |
| 4.2.2 | Is data encrypted at rest? | ☐ Yes ☐ No ☐ Partial | Method: |
| 4.2.3 | Are encryption keys properly managed? | ☐ Yes ☐ No | |
| 4.2.4 | Is TLS 1.2 or higher required? | ☐ Yes ☐ No | Version: |
| 4.2.5 | Is end-to-end encryption available? | ☐ Yes ☐ No ☐ N/A | |

### 4.3 Data Privacy

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 4.3.1 | Does vendor have a privacy policy? | ☐ Yes ☐ No | |
| 4.3.2 | Is GDPR compliance demonstrated (if applicable)? | ☐ Yes ☐ No ☐ N/A | |
| 4.3.3 | Will vendor sign a Data Processing Agreement? | ☐ Yes ☐ No | |
| 4.3.4 | Can vendor support data subject requests? | ☐ Yes ☐ No | |
| 4.3.5 | Are international data transfers documented? | ☐ Yes ☐ No ☐ N/A | Mechanism: |

---

## Section 5: Network and Infrastructure Security

### 5.1 Network Security

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 5.1.1 | Are firewalls deployed and properly configured? | ☐ Yes ☐ No | |
| 5.1.2 | Is network segmentation implemented? | ☐ Yes ☐ No ☐ Partial | |
| 5.1.3 | Is intrusion detection/prevention (IDS/IPS) deployed? | ☐ Yes ☐ No | |
| 5.1.4 | Is DDoS protection in place? | ☐ Yes ☐ No | |
| 5.1.5 | Are wireless networks secured? | ☐ Yes ☐ No ☐ N/A | |

### 5.2 Endpoint Security

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 5.2.1 | Is anti-malware/EDR deployed on endpoints? | ☐ Yes ☐ No | Product: |
| 5.2.2 | Are endpoints patched regularly? | ☐ Yes ☐ No | Frequency: |
| 5.2.3 | Are mobile devices managed? | ☐ Yes ☐ No ☐ N/A | |
| 5.2.4 | Is endpoint encryption required? | ☐ Yes ☐ No | |
| 5.2.5 | Are removable media controlled? | ☐ Yes ☐ No | |

---

## Section 6: Security Operations

### 6.1 Vulnerability Management

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 6.1.1 | Are regular vulnerability scans performed? | ☐ Yes ☐ No | Frequency: |
| 6.1.2 | Are penetration tests conducted? | ☐ Yes ☐ No | Frequency: |
| 6.1.3 | Is there a patch management process? | ☐ Yes ☐ No | |
| 6.1.4 | Are critical patches applied within defined SLAs? | ☐ Yes ☐ No | SLA: |
| 6.1.5 | Can penetration test results be shared? | ☐ Yes ☐ No | |

### 6.2 Logging and Monitoring

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 6.2.1 | Are security events logged? | ☐ Yes ☐ No ☐ Partial | |
| 6.2.2 | Are logs monitored for security incidents? | ☐ Yes ☐ No | |
| 6.2.3 | Is there 24/7 security monitoring? | ☐ Yes ☐ No | |
| 6.2.4 | Are logs retained for adequate period? | ☐ Yes ☐ No | Retention: |
| 6.2.5 | Are logs available for customer review? | ☐ Yes ☐ No ☐ Partial | |

### 6.3 Change Management

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 6.3.1 | Is there a formal change management process? | ☐ Yes ☐ No | |
| 6.3.2 | Are changes tested before deployment? | ☐ Yes ☐ No | |
| 6.3.3 | Are customers notified of material changes? | ☐ Yes ☐ No | |
| 6.3.4 | Are emergency changes controlled? | ☐ Yes ☐ No | |

---

## Section 7: Incident Response

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 7.1 | Is there a documented incident response plan? | ☐ Yes ☐ No | |
| 7.2 | Is there a dedicated incident response team? | ☐ Yes ☐ No | |
| 7.3 | Are incident response procedures tested? | ☐ Yes ☐ No | Frequency: |
| 7.4 | What is the breach notification timeframe? | | Hours: |
| 7.5 | Will vendor notify customer of breaches affecting their data? | ☐ Yes ☐ No | |
| 7.6 | Can vendor provide forensic investigation support? | ☐ Yes ☐ No | |

---

## Section 8: Business Continuity

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 8.1 | Is there a business continuity plan? | ☐ Yes ☐ No | |
| 8.2 | Is there a disaster recovery plan? | ☐ Yes ☐ No | |
| 8.3 | What is the committed RTO? | | Hours: |
| 8.4 | What is the committed RPO? | | Hours: |
| 8.5 | Are backups performed regularly? | ☐ Yes ☐ No | Frequency: |
| 8.6 | Are backups tested for recoverability? | ☐ Yes ☐ No | Frequency: |
| 8.7 | Is there geographic redundancy? | ☐ Yes ☐ No | |
| 8.8 | Are BC/DR plans tested? | ☐ Yes ☐ No | Frequency: |

---

## Section 9: Physical Security

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 9.1 | Are data centers physically secured? | ☐ Yes ☐ No ☐ N/A | |
| 9.2 | Is there access control to facilities? | ☐ Yes ☐ No | |
| 9.3 | Is there video surveillance? | ☐ Yes ☐ No | |
| 9.4 | Are there environmental controls (fire, flood, power)? | ☐ Yes ☐ No | |
| 9.5 | Is there redundant power supply? | ☐ Yes ☐ No | |
| 9.6 | Are visitors logged and escorted? | ☐ Yes ☐ No | |

---

## Section 10: Human Resources Security

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 10.1 | Are background checks performed on employees? | ☐ Yes ☐ No ☐ Partial | |
| 10.2 | Is security awareness training provided? | ☐ Yes ☐ No | Frequency: |
| 10.3 | Are employees required to sign confidentiality agreements? | ☐ Yes ☐ No | |
| 10.4 | Is there a termination procedure including access revocation? | ☐ Yes ☐ No | |
| 10.5 | Are disciplinary procedures in place for security violations? | ☐ Yes ☐ No | |

---

## Section 11: Application Security (if applicable)

| # | Question | Response | Notes |
|---|----------|----------|-------|
| 11.1 | Is secure development lifecycle (SDLC) followed? | ☐ Yes ☐ No ☐ N/A | |
| 11.2 | Are code reviews performed? | ☐ Yes ☐ No | |
| 11.3 | Is application security testing performed (SAST/DAST)? | ☐ Yes ☐ No | |
| 11.4 | Are OWASP Top 10 vulnerabilities addressed? | ☐ Yes ☐ No | |
| 11.5 | Is there input validation on all user inputs? | ☐ Yes ☐ No | |
| 11.6 | Are dependencies scanned for vulnerabilities? | ☐ Yes ☐ No | |

---

## Section 12: Assessment Summary

### 12.1 Scoring

| Domain | Weight | Score (1-5) | Weighted Score |
|--------|--------|-------------|----------------|
| Security Governance | 15% | | |
| Access Control | 15% | | |
| Data Protection | 20% | | |
| Network/Infrastructure | 10% | | |
| Security Operations | 15% | | |
| Incident Response | 10% | | |
| Business Continuity | 10% | | |
| Physical/HR Security | 5% | | |
| **Total** | **100%** | | |

**Score Key:** 1=Not Implemented, 2=Partially Implemented, 3=Implemented, 4=Well Implemented, 5=Excellent

### 12.2 Risk Rating

| Score Range | Risk Level |
|-------------|------------|
| 4.0 - 5.0 | Low Risk |
| 3.0 - 3.9 | Medium Risk |
| 2.0 - 2.9 | High Risk |
| 1.0 - 1.9 | Critical Risk |

**Overall Risk Rating:** ☐ Low ☐ Medium ☐ High ☐ Critical

### 12.3 Findings Summary

| # | Finding | Severity | Remediation Required |
|---|---------|----------|---------------------|
| 1 | | ☐ Critical ☐ High ☐ Medium ☐ Low | ☐ Yes ☐ No |
| 2 | | ☐ Critical ☐ High ☐ Medium ☐ Low | ☐ Yes ☐ No |
| 3 | | ☐ Critical ☐ High ☐ Medium ☐ Low | ☐ Yes ☐ No |

### 12.4 Recommendation

☐ **Approve** - Vendor meets security requirements
☐ **Approve with Conditions** - Vendor must address findings within [timeframe]
☐ **Do Not Approve** - Significant security gaps exist
☐ **Further Review Required** - Additional assessment needed

---

## Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Assessor | | | |
| Security Manager | | | |
| Business Owner | | | |

---

[Back to Checklists](./README.md) | [Back to Home](../README.md)

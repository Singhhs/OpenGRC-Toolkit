# Security Incident Report

## Document Information

| Field | Value |
|-------|-------|
| **Incident ID** | INC-[YYYY]-[XXX] |
| **Incident Title** | [Brief descriptive title] |
| **Report Date** | [DATE] |
| **Report Author** | [NAME] |
| **Classification** | [CONFIDENTIAL / RESTRICTED] |

---

## 1. Executive Summary

[2-3 paragraph summary covering: what happened, impact, response, current status, and key lessons learned. Write for a non-technical executive audience.]

| Key Facts | |
|-----------|---|
| **Incident Type** | [e.g., Ransomware, Data Breach, Phishing] |
| **Severity** | [Critical / High / Medium / Low] |
| **Duration** | [Start date/time] to [End date/time] |
| **Impact** | [Brief impact statement] |
| **Root Cause** | [One sentence] |
| **Status** | [Closed / Monitoring / Ongoing] |

---

## 2. Incident Timeline

| Date/Time | Event |
|-----------|-------|
| [YYYY-MM-DD HH:MM] | [Initial compromise/first indicator] |
| [YYYY-MM-DD HH:MM] | [Detection] |
| [YYYY-MM-DD HH:MM] | [CSIRT activated] |
| [YYYY-MM-DD HH:MM] | [Containment action] |
| [YYYY-MM-DD HH:MM] | [Key milestone] |
| [YYYY-MM-DD HH:MM] | [Recovery complete] |
| [YYYY-MM-DD HH:MM] | [Incident closed] |

---

## 3. Incident Description

### 3.1 What Happened

[Detailed narrative of the incident from initial compromise through resolution. Include technical details appropriate for the audience.]

### 3.2 How It Was Detected

[How the incident was discovered - monitoring alert, user report, third-party notification, etc.]

### 3.3 Initial Response

[Actions taken immediately upon detection.]

---

## 4. Technical Details

### 4.1 Attack Vector

[How the attacker gained access - phishing, vulnerability, stolen credentials, etc.]

### 4.2 Systems Affected

| System | Type | Data | Impact |
|--------|------|------|--------|
| [System name] | [Server/Workstation/Cloud] | [Data type] | [Impact] |

### 4.3 Indicators of Compromise (IOCs)

| Type | Value | Notes |
|------|-------|-------|
| IP Address | [X.X.X.X] | [C2 server] |
| Domain | [domain.com] | [Phishing] |
| File Hash | [SHA256] | [Malware] |
| Email Address | [email] | [Sender] |

### 4.4 Attacker TTPs

[If known, describe tactics, techniques, and procedures observed. Reference MITRE ATT&CK if applicable.]

---

## 5. Impact Assessment

### 5.1 Data Impact

| Data Type | Records/Volume | Classification | Regulatory |
|-----------|----------------|----------------|------------|
| [Type] | [Number/Size] | [Level] | [GDPR/HIPAA/etc.] |

### 5.2 Business Impact

- **Operational:** [Impact on operations]
- **Financial:** [Estimated costs - response, recovery, potential fines]
- **Reputational:** [Customer/public perception impact]
- **Regulatory:** [Compliance implications]

### 5.3 Affected Parties

- Internal: [Departments, users affected]
- External: [Customers, partners, vendors affected]

---

## 6. Response Actions

### 6.1 Containment

| Action | Date/Time | Performed By |
|--------|-----------|--------------|
| [Action taken] | [When] | [Who] |

### 6.2 Eradication

| Action | Date/Time | Performed By |
|--------|-----------|--------------|
| [Action taken] | [When] | [Who] |

### 6.3 Recovery

| System | Recovery Method | Completed |
|--------|-----------------|-----------|
| [System] | [Rebuild/Restore] | [Date] |

---

## 7. Communication

### 7.1 Internal Communication

| Audience | Date | Method | Summary |
|----------|------|--------|---------|
| [Executive team] | [Date] | [Meeting/Email] | [What communicated] |

### 7.2 External Communication

| Audience | Date | Method | Summary |
|----------|------|--------|---------|
| [Customers] | [Date] | [Email/Letter] | [What communicated] |
| [Regulator] | [Date] | [Formal notification] | [Reference number] |

---

## 8. Root Cause Analysis

### 8.1 Root Cause

[What was the fundamental cause that allowed this incident to occur?]

### 8.2 Contributing Factors

1. [Factor 1 - e.g., missing patch]
2. [Factor 2 - e.g., weak authentication]
3. [Factor 3 - e.g., lack of monitoring]

### 8.3 Why It Wasn't Prevented

[What controls failed or were missing?]

### 8.4 Why It Wasn't Detected Earlier

[What detection gaps existed?]

---

## 9. Lessons Learned

### 9.1 What Worked Well

1. [Positive aspect of response]
2. [Positive aspect of response]

### 9.2 What Could Be Improved

1. [Area for improvement]
2. [Area for improvement]

### 9.3 Recommendations

| # | Recommendation | Priority | Owner | Due Date |
|---|----------------|----------|-------|----------|
| 1 | [Specific recommendation] | [High/Med/Low] | [Name] | [Date] |
| 2 | [Specific recommendation] | [High/Med/Low] | [Name] | [Date] |
| 3 | [Specific recommendation] | [High/Med/Low] | [Name] | [Date] |

---

## 10. Appendices

### Appendix A: Evidence Inventory

| Evidence ID | Type | Description | Location | Collected By |
|-------------|------|-------------|----------|--------------|
| [EVD-001] | [Log/Image/etc.] | [Description] | [Location] | [Name] |

### Appendix B: Response Team

| Role | Name | Department |
|------|------|------------|
| Incident Manager | [Name] | [Dept] |
| Technical Lead | [Name] | [Dept] |
| [Other roles] | [Name] | [Dept] |

### Appendix C: Related Tickets/Cases

| System | ID | Status |
|--------|------|--------|
| [Ticketing system] | [ID] | [Status] |
| [Legal case] | [ID] | [Status] |

---

## Approvals

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Incident Manager | | | |
| [CISO] | | | |
| [Legal] | | | |

---

**Distribution:** [List who receives this report]

**Retention:** [How long to retain]

---

[Back to Templates](./README.md) | [Back to Crisis Management](../README.md)

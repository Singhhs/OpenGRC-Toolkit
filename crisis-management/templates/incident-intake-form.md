# Incident Intake Form

Use this form to capture initial incident information when a security event is reported.

---

## Incident Intake Form

### Section 1: Reporter Information

| Field | Information |
|-------|-------------|
| **Date/Time Reported** | |
| **Reported By** | |
| **Reporter Contact** | Phone: / Email: |
| **Reporter Department** | |
| **Intake Handled By** | |
| **Ticket Number** | INC- |

---

### Section 2: Incident Description

**How was the incident discovered?**
- [ ] User report
- [ ] Alert from security tool
- [ ] IT staff observation
- [ ] External notification
- [ ] Automated monitoring
- [ ] Other: ____________

**Brief description of the incident:**

_________________________________________________________________

_________________________________________________________________

_________________________________________________________________

**When did the incident occur?**
- Date: ____________
- Time: ____________
- Timezone: ____________
- [ ] Ongoing
- [ ] Unknown

**When was it discovered?**
- Date: ____________
- Time: ____________

---

### Section 3: Incident Classification

**Type of incident:** (check all that apply)
- [ ] Malware/Virus
- [ ] Ransomware
- [ ] Phishing/Social Engineering
- [ ] Unauthorized Access
- [ ] Data Breach/Exposure
- [ ] Denial of Service
- [ ] Account Compromise
- [ ] Lost/Stolen Device
- [ ] Insider Threat
- [ ] Physical Security
- [ ] Policy Violation
- [ ] Other: ____________

**Initial severity assessment:**
- [ ] **P1 Critical** - Active attack, data exfiltration, business-threatening
- [ ] **P2 High** - Significant impact, requires priority response
- [ ] **P3 Medium** - Moderate impact, limited scope
- [ ] **P4 Low** - Minimal impact, routine handling
- [ ] Unknown - Needs assessment

---

### Section 4: Affected Assets

**Systems affected:** (list hostnames, IPs, or descriptions)

| System Name | IP Address | Type | Location |
|-------------|------------|------|----------|
| | | | |
| | | | |
| | | | |

**Users affected:**

| User Name | Username | Department | Role |
|-----------|----------|------------|------|
| | | | |
| | | | |

**Number of systems potentially affected:** ____________

**Number of users potentially affected:** ____________

**Critical systems involved?**
- [ ] Yes - List: ____________
- [ ] No
- [ ] Unknown

---

### Section 5: Data Impact

**Is data involved?**
- [ ] Yes
- [ ] No
- [ ] Unknown

**If yes, what type of data?**
- [ ] Personal Identifiable Information (PII)
- [ ] Financial data
- [ ] Health information (PHI)
- [ ] Intellectual property
- [ ] Customer data
- [ ] Employee data
- [ ] Business confidential
- [ ] Public information
- [ ] Unknown
- [ ] Other: ____________

**Data impact type:**
- [ ] Data accessed/viewed
- [ ] Data exfiltrated/stolen
- [ ] Data modified/corrupted
- [ ] Data encrypted (ransomware)
- [ ] Data deleted/destroyed
- [ ] Unknown

---

### Section 6: Immediate Actions Taken

**What actions have already been taken?**
- [ ] System isolated/disconnected
- [ ] User account disabled
- [ ] Password reset
- [ ] Antivirus scan initiated
- [ ] Logs preserved
- [ ] Screenshots captured
- [ ] Manager notified
- [ ] None yet
- [ ] Other: ____________

**Who else has been notified?**

| Name | Role | Time Notified |
|------|------|---------------|
| | | |
| | | |

---

### Section 7: Additional Information

**Indicators of Compromise (if known):**
- Malicious IPs: ____________
- Malicious domains: ____________
- File hashes: ____________
- Suspicious filenames: ____________
- Error messages: ____________

**Related ticket numbers:** ____________

**Is this potentially related to another incident?**
- [ ] Yes - Related incident: ____________
- [ ] No
- [ ] Unknown

**Additional context or observations:**

_________________________________________________________________

_________________________________________________________________

_________________________________________________________________

---

### Section 8: Attachments/Evidence

**Evidence collected:**
- [ ] Screenshots
- [ ] Log files
- [ ] Email samples
- [ ] Malware samples
- [ ] Network captures
- [ ] Other: ____________

**Attachment locations:**

| Description | Location/Filename |
|-------------|-------------------|
| | |
| | |

---

### Section 9: Escalation Decision

**Escalation required?**
- [ ] Yes - Escalate to: ____________
- [ ] No - Handle as routine ticket
- [ ] Needs triage by security team

**Escalation reason:**

_________________________________________________________________

---

### Section 10: Intake Completion

**Intake completed by:** ____________

**Date/Time:** ____________

**Initial response team assigned:** ____________

**Initial response deadline:** ____________

---

## Quick Reference: When to Escalate Immediately

Escalate immediately (P1/P2) if:
- [ ] Active data exfiltration
- [ ] Ransomware encryption in progress
- [ ] Multiple systems affected
- [ ] Critical systems/data involved
- [ ] Executive accounts affected
- [ ] Customer data at risk
- [ ] External notification received
- [ ] Evidence of advanced persistent threat

---

## Intake Process Checklist

- [ ] All sections completed to extent information is available
- [ ] Evidence preserved (do not modify/delete)
- [ ] Initial severity assigned
- [ ] Escalation decision made
- [ ] Ticket created in tracking system
- [ ] Assigned to appropriate team
- [ ] Reporter acknowledged
- [ ] Initial response SLA noted

---

## Contact Quick Reference

| Escalation | Contact | Phone |
|------------|---------|-------|
| Security Team | [EMAIL] | [PHONE] |
| On-Call Security | [EMAIL] | [PHONE] |
| CISO | [EMAIL] | [PHONE] |
| IT Operations | [EMAIL] | [PHONE] |
| Help Desk | [EMAIL] | [PHONE] |

---

[Back to Templates](./README.md) | [Back to Crisis Management](../README.md)

# Data Breach Playbook

**Severity:** Typically High (P2) or Critical (P1)
**Last Updated:** [DATE]
**Owner:** [ROLE]

---

## 1. Overview

This playbook covers response to confirmed or suspected unauthorized access, acquisition, or disclosure of personal or sensitive data.

## 2. Detection Indicators

### Signs of Data Breach

- [ ] Unusual data access patterns
- [ ] Large data transfers or downloads
- [ ] Access from unusual locations/times
- [ ] Security alerts for data exfiltration
- [ ] Unauthorized access attempts
- [ ] Third-party notification
- [ ] Discovery of data on dark web/external sites
- [ ] Customer/user reports of identity theft
- [ ] Suspicious outbound network traffic

### Initial Assessment Questions

1. What type of data may be affected?
2. How many records/individuals impacted?
3. Is breach confirmed or suspected?
4. Is data exposure ongoing?
5. What systems were involved?
6. Was data encrypted?
7. What was the attack vector?

## 3. Severity Assessment

| Factor | Critical (P1) | High (P2) | Medium (P3) |
|--------|--------------|-----------|-------------|
| Data Type | Regulated PII, financial, health | Sensitive personal data | Internal data |
| Volume | >10,000 records | 1,000-10,000 records | <1,000 records |
| Active | Ongoing exfiltration | Stopped but uncertain scope | Contained |
| Regulatory | Mandatory notification | Likely notification | Possible notification |

## 4. Immediate Actions (First Hour)

### DO

- [ ] **Contain the breach** - Stop ongoing data loss
- [ ] **Preserve evidence** - Do not delete logs or data
- [ ] **Assess scope** - What data, how much, who affected
- [ ] **Alert key personnel**:
  - [ ] CSIRT Lead
  - [ ] CISO
  - [ ] Legal Counsel
  - [ ] Privacy Officer/DPO
  - [ ] Executive Management
- [ ] **Begin incident log** - Document all actions with timestamps
- [ ] **Activate legal privilege** if appropriate

### DO NOT

- [ ] Do NOT communicate externally without legal approval
- [ ] Do NOT delete or modify potential evidence
- [ ] Do NOT notify affected individuals yet (legal coordination first)
- [ ] Do NOT make public statements
- [ ] Do NOT speculate on scope or cause

## 5. Containment

### Stop Data Loss

1. [ ] Block compromised accounts
2. [ ] Isolate affected systems
3. [ ] Block exfiltration channels (IPs, domains)
4. [ ] Revoke API keys or tokens
5. [ ] Change relevant credentials
6. [ ] Implement additional monitoring

### Secure Evidence

1. [ ] Preserve all relevant logs
2. [ ] Create forensic images
3. [ ] Document network traffic
4. [ ] Capture memory dumps
5. [ ] Secure physical evidence
6. [ ] Maintain chain of custody

## 6. Investigation

### Determine Scope

| Question | Finding |
|----------|---------|
| What data types were exposed? | |
| How many records? | |
| How many individuals? | |
| What geographies? | |
| Time period of exposure? | |
| Was data encrypted? | |
| Was encryption compromised? | |
| What was attack vector? | |
| Is data publicly accessible? | |

### Data Classification Review

| Data Type | Affected | Volume | Regulatory Impact |
|-----------|----------|--------|-------------------|
| Names | Yes/No | | |
| Email addresses | Yes/No | | |
| Addresses | Yes/No | | |
| Phone numbers | Yes/No | | |
| National IDs (SSN, etc.) | Yes/No | | |
| Financial data | Yes/No | | |
| Health data | Yes/No | | |
| Authentication data | Yes/No | | |
| [Other] | Yes/No | | |

### Root Cause Analysis

- [ ] How did attackers gain access?
- [ ] What vulnerabilities were exploited?
- [ ] Were there warning signs missed?
- [ ] How long was access maintained?
- [ ] What controls failed?

## 7. Legal and Regulatory Assessment

### Notification Requirements

**Work with Legal to determine:**

| Jurisdiction/Regulation | Applies | Timeline | Authority |
|------------------------|---------|----------|-----------|
| GDPR (EU) | Yes/No | 72 hours | Data Protection Authority |
| [State breach laws] | Yes/No | [Timeline] | [Authority] |
| HIPAA | Yes/No | 60 days | HHS |
| PCI DSS | Yes/No | Varies | Card brands |
| [Other regulations] | Yes/No | [Timeline] | [Authority] |

### Notification Content Requirements

Notifications typically require:
- Description of breach
- Data types involved
- Approximate number affected
- Likely consequences
- Measures taken
- Contact information
- Recommendations for individuals

## 8. Communication Plan

### Internal Communication

| Audience | When | Who Communicates | Content |
|----------|------|------------------|---------|
| CSIRT | Immediately | Incident Manager | Full details |
| Executive team | Within hours | CISO | Impact, response |
| Board | Within 24-48h | CEO/CISO | Impact, response, liability |
| Employees | After external | Communications | Prepared messaging |

### External Communication

**All external communications require Legal approval**

| Audience | Trigger | Timeline | Content |
|----------|---------|----------|---------|
| Regulators | Regulatory requirement | Per regulation | Formal notification |
| Affected individuals | Confirmed impact | Per regulation | Notification letter |
| Media | Public exposure | As needed | Prepared statement |
| Partners | Impact on them | As appropriate | Coordinated message |

### Communication Principles

- Accurate, factual information only
- Do not speculate or assign blame
- Coordinate all messaging
- Document all communications
- Legal review before external communications

## 9. Individual Notification

### When Required

Notify individuals when breach is likely to result in high risk to their rights and freedoms (GDPR) or as required by applicable laws.

### Notification Content

| Element | Details |
|---------|---------|
| What happened | Clear description of incident |
| What data was affected | Specific data types |
| What we're doing | Remediation actions |
| What you can do | Protective measures |
| Where to get help | Contact information |
| Credit monitoring | If offering |

### Notification Channels

- Direct mail (preferred for regulated breaches)
- Email (if mail address not available)
- Substitute notice (large-scale, no contact info)

### Support Resources

- Dedicated helpline
- FAQ document
- Credit monitoring enrollment
- Identity protection services

## 10. Remediation

### Immediate Fixes

- [ ] Patch exploited vulnerabilities
- [ ] Reset compromised credentials
- [ ] Block attack vectors
- [ ] Enhance monitoring

### Long-term Improvements

- [ ] Address root cause
- [ ] Implement additional controls
- [ ] Update policies/procedures
- [ ] Enhance detection capabilities
- [ ] Staff training

## 11. Recovery

### System Recovery

- [ ] Verify systems are clean
- [ ] Restore from known good backups
- [ ] Implement additional controls
- [ ] Return to normal operations
- [ ] Enhanced monitoring period

### Business Recovery

- [ ] Address customer concerns
- [ ] Manage reputational impact
- [ ] Address regulatory requirements
- [ ] Support affected individuals

## 12. Post-Incident

### Documentation

- [ ] Complete incident report
- [ ] Timeline of events
- [ ] Root cause analysis
- [ ] Impact assessment
- [ ] Costs incurred
- [ ] Regulatory filings

### Lessons Learned

Conduct within 2 weeks:
- What happened and why?
- What worked well?
- What could be improved?
- What controls need strengthening?
- What training is needed?

### Improvements

| Finding | Action | Owner | Due Date |
|---------|--------|-------|----------|
| | | | |

## 13. Quick Reference

```
DATA BREACH - FIRST HOUR

1. CONTAIN - Stop ongoing data loss
2. PRESERVE - Don't delete evidence
3. ASSESS - What data, how much, who
4. NOTIFY - CSIRT, Legal, CISO, Privacy
5. DOCUMENT - Log everything
6. DON'T COMMUNICATE externally yet

Emergency: [PHONE NUMBER]
Legal: [PHONE NUMBER]
Privacy Officer: [PHONE NUMBER]
```

## 14. Regulatory Quick Reference

| Regulation | Timeline | Key Requirements |
|------------|----------|------------------|
| GDPR | 72 hours to DPA | Notify unless unlikely to risk |
| CCPA | "Expedient" | Written notice |
| HIPAA | 60 days | Notify individuals + HHS |
| PCI DSS | Immediate | Notify card brands |

<!-- CUSTOMIZE: Add your applicable regulations -->

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

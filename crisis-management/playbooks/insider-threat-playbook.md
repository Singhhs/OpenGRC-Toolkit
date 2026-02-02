# Insider Threat Playbook

**Severity:** Typically High (P2) or Critical (P1)
**Last Updated:** [DATE]
**Owner:** [ROLE]

---

## 1. Overview

This playbook covers response to suspected or confirmed malicious insider activity, including data theft, sabotage, fraud, and policy violations by employees, contractors, or other trusted insiders.

## 2. Insider Threat Categories

| Type | Description | Examples |
|------|-------------|----------|
| **Malicious** | Intentional harmful actions | Data theft, sabotage, fraud |
| **Negligent** | Careless but not intentional | Policy violations, accidental exposure |
| **Compromised** | Credentials/access exploited by external actor | Account takeover, coercion |

## 3. Detection Indicators

### Behavioral Indicators

- [ ] Working unusual hours without justification
- [ ] Accessing data outside job scope
- [ ] Expressing dissatisfaction or grievances
- [ ] Financial difficulties
- [ ] Resignation notice (especially to competitor)
- [ ] Bypassing security controls
- [ ] Unusual interest in sensitive information

### Technical Indicators

- [ ] Large data downloads or transfers
- [ ] Accessing systems after hours
- [ ] Using unauthorized storage (USB, cloud)
- [ ] Email to personal accounts with attachments
- [ ] Attempts to access restricted areas
- [ ] Disabled security software
- [ ] Excessive printing of sensitive documents
- [ ] Multiple failed access attempts

### Data Activity Indicators

- [ ] Bulk downloads from sensitive repositories
- [ ] Copying customer/client lists
- [ ] Accessing intellectual property
- [ ] Downloading code repositories
- [ ] Exporting databases
- [ ] Printing unusual volumes

## 4. Severity Assessment

| Factor | Critical | High | Medium |
|--------|----------|------|--------|
| **Data Involved** | Trade secrets, regulated data | Confidential business data | Internal data |
| **Intent** | Confirmed malicious | Suspected malicious | Unknown/negligent |
| **Ongoing** | Active exfiltration | Recent activity | Historical |
| **Position** | Privileged/executive | Standard access | Limited access |

---

## 5. Initial Response

### CRITICAL: Confidentiality

> **All insider threat investigations MUST be conducted with strict confidentiality. Premature disclosure can:**
> - Alert the insider
> - Compromise evidence
> - Expose the organization to legal liability
> - Damage reputation of innocent employees

### Immediate Actions

1. [ ] **Do NOT confront** the individual
2. [ ] **Limit knowledge** to need-to-know
3. [ ] **Secure evidence** without alerting subject
4. [ ] **Notify core team only:**
   - CISO/Security Manager
   - Legal Counsel
   - HR Director
   - [Executive Sponsor]
5. [ ] **Preserve logs** before they rotate
6. [ ] **Document everything**

### Initial Assessment Questions

1. What activity triggered the concern?
2. What data may be involved?
3. Is the threat ongoing?
4. What is the person's role/access level?
5. Is there an employment situation (resignation, termination)?
6. Are there any accomplices?
7. Is law enforcement involvement warranted?

---

## 6. Investigation Team

### Core Team

| Role | Responsibility |
|------|----------------|
| Investigation Lead | Coordinate investigation, decision-making |
| IT Security | Technical investigation, log analysis |
| HR | Employment matters, policy, interviews |
| Legal | Legal guidance, evidence preservation |
| Executive Sponsor | Authority, resource allocation |

### Extended Team (as needed)

| Role | When Needed |
|------|-------------|
| Forensics Specialist | Digital forensics required |
| Outside Counsel | Litigation likely |
| Law Enforcement | Criminal activity |
| Physical Security | Physical access concerns |
| PR/Communications | Public exposure risk |

---

## 7. Evidence Preservation

### CRITICAL: Legal Hold

Before any investigation activity:

1. [ ] Consult legal counsel
2. [ ] Issue litigation hold if appropriate
3. [ ] Preserve all relevant data
4. [ ] Document chain of custody

### Digital Evidence

| Evidence Type | Preservation Method |
|---------------|---------------------|
| Email | Legal hold, export mailbox |
| File access logs | Export, preserve |
| Authentication logs | Export, preserve |
| Network traffic | Capture if possible |
| Endpoint data | Forensic image |
| Cloud activity | Export audit logs |
| Badge access | Export logs |
| CCTV footage | Preserve relevant footage |

### Documentation Requirements

For all evidence:
- Date and time collected
- Who collected
- How stored
- Chain of custody
- Hash values for digital evidence

---

## 8. Investigation Procedures

### Phase 1: Preliminary Assessment

**Timeline:** 24-48 hours

1. [ ] Review initial indicators
2. [ ] Analyze available logs
3. [ ] Determine scope of concern
4. [ ] Assess immediate risk
5. [ ] Decide on enhanced monitoring

### Phase 2: Detailed Investigation

**Timeline:** As needed (days to weeks)

#### Technical Investigation

1. [ ] Analyze access logs:
   - What systems accessed
   - When accessed
   - What data viewed/copied
2. [ ] Review email activity:
   - External sends with attachments
   - Forwarding rules
   - Personal account sends
3. [ ] Check file activity:
   - Downloads
   - Copies to removable media
   - Cloud uploads
4. [ ] Network analysis:
   - Unusual connections
   - Data transfers
   - Unauthorized services
5. [ ] Endpoint analysis:
   - USB connections
   - Software installed
   - Browser history
   - Local storage

#### HR Investigation

1. [ ] Review employment records
2. [ ] Check for grievances/disputes
3. [ ] Note resignation/termination status
4. [ ] Document access and clearances
5. [ ] Identify potential motives

### Phase 3: Interviews (if appropriate)

**IMPORTANT:** Coordinate with HR and Legal before any interviews

| Interview Type | Conducted By | Purpose |
|----------------|--------------|---------|
| Witnesses | HR + Security | Corroborate information |
| Managers | HR | Context and observations |
| Subject | HR + Legal | Only with legal guidance |

---

## 9. Response Actions

### If Active Threat Confirmed

#### Containment (Covert if possible)

1. [ ] Increase monitoring/logging
2. [ ] Restrict access incrementally (if won't alert)
3. [ ] Block data exfiltration channels
4. [ ] Preserve ongoing evidence
5. [ ] Prepare for rapid lockout

#### When Ready to Act

1. [ ] Coordinate timing with HR/Legal
2. [ ] Disable all access simultaneously:
   - [ ] Network/VPN
   - [ ] Email
   - [ ] Applications
   - [ ] Badge access
   - [ ] Remote access
3. [ ] Secure devices
4. [ ] Redirect phone/email as appropriate
5. [ ] Conduct interview (HR led)
6. [ ] Execute separation if warranted

### Access Revocation Checklist

| System | Disabled | Verified | By |
|--------|----------|----------|-----|
| Active Directory | [ ] | [ ] | |
| Email | [ ] | [ ] | |
| VPN | [ ] | [ ] | |
| Cloud services | [ ] | [ ] | |
| Building access | [ ] | [ ] | |
| Business applications | [ ] | [ ] | |
| Admin accounts | [ ] | [ ] | |
| Shared accounts | [ ] | [ ] | |

---

## 10. Handling Departing Employees

### High-Risk Indicators

- Resignation to competitor
- Involuntary termination
- Access to sensitive data
- Previous policy violations
- Expressed grievances

### Monitoring Period

For high-risk departures:

1. [ ] Enhanced monitoring during notice period
2. [ ] Review data access patterns
3. [ ] Check for bulk downloads
4. [ ] Monitor email for exfiltration
5. [ ] Exit interview focus on data
6. [ ] Device return and inspection

---

## 11. Legal Considerations

### Consult Legal Before

- Conducting surveillance
- Accessing personal areas/accounts
- Interviewing the subject
- Terminating employment
- Contacting law enforcement
- Communicating externally

### Employee Rights

Be aware of:
- Privacy laws in jurisdiction
- Employment contracts
- Union agreements
- Whistleblower protections
- Wrongful termination risks

### Law Enforcement

Involve law enforcement when:
- Criminal activity evident
- Significant financial loss
- Threat to safety
- Regulatory requirement
- Legal counsel recommends

---

## 12. Communication

### Internal Communication

| Audience | What to Share | When |
|----------|---------------|------|
| Investigation team | Full details | Throughout |
| HR | Employment matters | As needed |
| Executive | Summary, decisions | Key milestones |
| Affected teams | Minimal, need-to-know | After resolution |
| General staff | Nothing specific | If necessary |

### What NOT to Communicate

- Investigation details
- Subject's identity (unless public)
- Speculation
- Legal conclusions

---

## 13. Remediation

### Immediate

- [ ] Recover company property
- [ ] Secure data and systems
- [ ] Close access vulnerabilities
- [ ] Assess data exposure

### If Data Compromised

- [ ] Determine data scope
- [ ] Assess breach notification requirements
- [ ] Follow [Data Breach Playbook](./data-breach-playbook.md) if needed
- [ ] Notify affected parties as required

### Longer Term

- [ ] Review access controls
- [ ] Enhance monitoring
- [ ] Update policies if needed
- [ ] Training/awareness improvements

---

## 14. Post-Incident

### Documentation

- [ ] Complete investigation report
- [ ] Timeline of events
- [ ] Evidence inventory
- [ ] Actions taken
- [ ] Lessons learned
- [ ] Store securely (legal hold)

### Review

- [ ] How was threat detected?
- [ ] Could we have detected earlier?
- [ ] Were controls adequate?
- [ ] What improvements needed?

### Program Improvements

| Area | Improvement | Owner | Timeline |
|------|-------------|-------|----------|
| Detection | | | |
| Monitoring | | | |
| Access Control | | | |
| Training | | | |

---

## 15. Prevention

### Preventive Controls

- Principle of least privilege
- Regular access reviews
- Data loss prevention tools
- Behavioral analytics
- Exit procedures
- Security awareness training
- Background checks
- Separation of duties

### Detection Controls

- User activity monitoring
- Data exfiltration detection
- Anomaly detection
- Log monitoring and alerting
- Physical access monitoring

---

## 16. Quick Reference

```
INSIDER THREAT - KEY PRINCIPLES

1. CONFIDENTIALITY is critical
2. DO NOT confront the individual
3. PRESERVE evidence first
4. INVOLVE Legal and HR early
5. COORDINATE all actions
6. DOCUMENT everything

Core Team:
- Security: [CONTACT]
- Legal: [CONTACT]
- HR: [CONTACT]
- Executive: [CONTACT]

Remember: Innocent until proven guilty
```

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

# Incident Response Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., Security Operations Manager] |
| **Classification** | Internal |

---

## 1. Purpose

This procedure provides step-by-step guidance for responding to information security incidents at [ORGANIZATION NAME].

## 2. Scope

Applies to all confirmed or suspected security incidents including:
- Malware infections
- Unauthorized access
- Data breaches
- Phishing attacks
- Denial of service
- Lost/stolen devices

## 3. Prerequisites

Before incident response begins, ensure:
- [ ] Access to incident response toolkit
- [ ] Contact list for CSIRT members
- [ ] Access to logging and monitoring systems
- [ ] Communication channels established
- [ ] Evidence collection tools available

## 4. Procedure

### Phase 1: Detection & Reporting

#### Step 1.1: Receive Incident Report
**Responsibility:** Security Operations / Help Desk

| Source | Action |
|--------|--------|
| User report | Log ticket, gather initial details |
| Alert from monitoring | Validate alert, reduce false positives |
| Third party notification | Verify source, obtain details |
| Automated detection | Review and correlate with other data |

#### Step 1.2: Initial Information Gathering

Collect the following information:
- [ ] Date and time of discovery
- [ ] Who reported it
- [ ] What was observed
- [ ] Systems/data potentially affected
- [ ] Initial scope estimate
- [ ] Is the incident ongoing?

Use the [Incident Intake Form](../templates/incident-intake-form.md).

#### Step 1.3: Initial Classification

| Question | If Yes → |
|----------|----------|
| Active data exfiltration? | P1 Critical |
| Ransomware/destructive malware? | P1 Critical |
| Critical system compromise? | P1 Critical |
| Sensitive data breach? | P2 High |
| Multiple systems affected? | P2 High |
| Single account compromise? | P3 Medium |
| Contained, minor impact? | P4 Low |

---

### Phase 2: Triage & Escalation

#### Step 2.1: Assign Incident Manager

| Severity | Incident Manager | Escalation Time |
|----------|-----------------|-----------------|
| P1 Critical | [CISO or Security Director] | Immediate |
| P2 High | [Security Operations Lead] | Within 1 hour |
| P3 Medium | [Security Analyst] | Within 4 hours |
| P4 Low | [Security Analyst] | Within 24 hours |

#### Step 2.2: Notify CSIRT

**For P1/P2 incidents, immediately notify:**
- [ ] CSIRT Team Lead
- [ ] IT Operations Manager
- [ ] [CISO]
- [ ] Legal (if potential data breach)
- [ ] Communications (if potential public impact)

**Notification template:**
```
SECURITY INCIDENT - [SEVERITY LEVEL]

Type: [Incident type]
Status: [Active/Contained]
Detected: [Date/Time]
Systems: [Affected systems]
Impact: [Known/potential impact]
Current action: [What's being done]
Bridge call: [If established]

Contact: [Incident Manager name and number]
```

#### Step 2.3: Establish Communication

| Severity | Communication Channel |
|----------|----------------------|
| P1 Critical | War room + bridge call |
| P2 High | Dedicated chat channel + scheduled calls |
| P3/P4 | Ticket-based updates |

---

### Phase 3: Containment

#### Step 3.1: Assess Containment Options

**Consider impact vs. effectiveness:**

| Option | When to Use | Considerations |
|--------|-------------|----------------|
| Network isolation | Active threat, spreading | Business disruption |
| Account disable | Compromised credentials | User impact |
| System shutdown | Destructive malware | Data loss, availability |
| Block at firewall | External threat | May alert attacker |
| Endpoint isolation | Single device compromised | User productivity |

#### Step 3.2: Implement Containment

**Short-term (stop the bleeding):**
1. [ ] Isolate affected systems from network
2. [ ] Disable compromised accounts
3. [ ] Block malicious IPs/domains
4. [ ] Preserve system state for forensics

**Document all actions with timestamp:**
```
[DATETIME] - [PERSON] - [ACTION TAKEN] - [RESULT]
```

#### Step 3.3: Evidence Preservation

Before making changes:
1. [ ] Create memory dump (if possible)
2. [ ] Create disk image
3. [ ] Capture network logs
4. [ ] Screenshot any evidence
5. [ ] Export relevant logs

**Chain of custody:**
- Who collected
- When collected
- How stored
- Who has accessed

---

### Phase 4: Eradication

#### Step 4.1: Identify Root Cause

Investigate:
- [ ] How did the attacker get in?
- [ ] What vulnerability was exploited?
- [ ] What accounts/systems were compromised?
- [ ] Was data accessed or exfiltrated?
- [ ] Are there persistence mechanisms?

#### Step 4.2: Remove Threat

| Threat Type | Eradication Steps |
|-------------|------------------|
| Malware | Remove malware, scan all systems, verify clean |
| Compromised account | Reset password, review activity, check other accounts |
| Vulnerability exploit | Patch vulnerability, review similar systems |
| Backdoor/persistence | Remove backdoor, verify no others exist |
| Phishing | Block sender, remove emails, reset any compromised credentials |

#### Step 4.3: Verify Eradication

- [ ] Run full antimalware scan
- [ ] Review system logs for anomalies
- [ ] Check for persistence mechanisms
- [ ] Verify no active connections to C2
- [ ] Confirm affected accounts secured

---

### Phase 5: Recovery

#### Step 5.1: Restoration Planning

| System Priority | Recovery Time Objective |
|-----------------|------------------------|
| Critical | < 4 hours |
| High | < 24 hours |
| Medium | < 72 hours |
| Low | As scheduled |

#### Step 5.2: System Restoration

**Option A: Rebuild from known good**
1. [ ] Rebuild system from gold image
2. [ ] Apply all patches
3. [ ] Restore data from clean backup
4. [ ] Verify integrity

**Option B: Clean and restore**
1. [ ] Remove all malicious artifacts
2. [ ] Apply missing patches
3. [ ] Harden configuration
4. [ ] Verify integrity

#### Step 5.3: Validate Recovery

Before returning to production:
- [ ] Security scan clean
- [ ] All patches applied
- [ ] Configurations hardened
- [ ] Logs being collected
- [ ] Monitoring active
- [ ] Test functionality

#### Step 5.4: Return to Operations

1. [ ] Reconnect to network
2. [ ] Enable user access
3. [ ] Monitor closely for 24-72 hours
4. [ ] Document restoration complete

---

### Phase 6: Post-Incident

#### Step 6.1: Incident Documentation

Complete the [Incident Report](../templates/incident-report-template.md) including:
- [ ] Executive summary
- [ ] Timeline of events
- [ ] Root cause analysis
- [ ] Impact assessment
- [ ] Actions taken
- [ ] Evidence inventory
- [ ] Costs incurred

#### Step 6.2: Lessons Learned Meeting

**Hold within 2 weeks of closure**

Agenda:
1. Incident walkthrough
2. What worked well
3. What could be improved
4. Action items

**Questions to address:**
- Was detection timely?
- Was response effective?
- Were procedures followed?
- What gaps were identified?
- What will we do differently?

#### Step 6.3: Improvement Actions

| Finding | Action | Owner | Due Date |
|---------|--------|-------|----------|
| [Gap identified] | [Corrective action] | [Person] | [Date] |

#### Step 6.4: Close Incident

- [ ] All documentation complete
- [ ] Lessons learned conducted
- [ ] Actions assigned and tracked
- [ ] Management briefed
- [ ] Incident ticket closed

---

## 5. Quick Reference: Severity Response

| Severity | Response Time | Incident Manager | Communication | Escalation |
|----------|---------------|------------------|---------------|------------|
| **P1 Critical** | Immediate | CISO | War room | Executive immediately |
| **P2 High** | < 4 hours | SecOps Lead | Chat channel | Executive within 4 hrs |
| **P3 Medium** | < 24 hours | Analyst | Ticket | Manager daily |
| **P4 Low** | < 72 hours | Analyst | Ticket | As needed |

## 6. Contacts

| Role | Name | Phone | Email |
|------|------|-------|-------|
| Security Operations | [NAME] | [PHONE] | [EMAIL] |
| CISO | [NAME] | [PHONE] | [EMAIL] |
| IT Operations | [NAME] | [PHONE] | [EMAIL] |
| Legal | [NAME] | [PHONE] | [EMAIL] |
| Communications | [NAME] | [PHONE] | [EMAIL] |
| HR | [NAME] | [PHONE] | [EMAIL] |

## 7. Related Documents

- [Incident Response Policy](../policies/incident-response-policy.md)
- [Incident Playbooks](../crisis-management/playbooks/README.md)
- [Communication Templates](../crisis-management/templates/README.md)
- [Forensics Procedure](./forensics-procedure.md)

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

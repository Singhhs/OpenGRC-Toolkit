# Physical Security Breach Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., Facilities/Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides guidance for responding to physical security incidents at [ORGANIZATION NAME] facilities, including unauthorized access, theft, vandalism, and security system failures.

### Scenarios Covered
- Unauthorized facility access
- Break-in / forced entry
- Theft of equipment or documents
- Vandalism or property damage
- Tailgating incidents
- Lost/stolen access badges
- Security system failures
- Suspicious persons or activity

---

## 2. Detection Indicators

### 2.1 Access Control Indicators

| Indicator | Description |
|-----------|-------------|
| Forced entry signs | Damaged doors, locks, windows |
| Unauthorized badge use | Badge used outside normal hours/locations |
| Failed access attempts | Multiple failed badge reads |
| Tailgating alerts | Piggybacking detection |
| Propped doors | Fire doors or secure doors propped open |
| Missing badges | Reported lost or stolen credentials |

### 2.2 Visual/Physical Indicators

| Indicator | Description |
|-----------|-------------|
| Unknown persons | Unescorted individuals in secure areas |
| Missing equipment | Computers, devices, or assets missing |
| Signs of tampering | Disturbed equipment, opened cases |
| Vandalism | Graffiti, damage to property |
| Suspicious items | Unknown packages, devices |
| Alarm activation | Intrusion, motion, or glass break alarms |

### 2.3 Security System Indicators

| Indicator | Description |
|-----------|-------------|
| Camera tampering | Cameras moved, covered, or disabled |
| System offline | Access control or CCTV system failures |
| Unusual log entries | Unexpected system access or changes |

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Active intruder, data center breach, theft of sensitive equipment, personal safety threat | Immediate - Call police |
| **P2 High** | After-hours breach detected, server room access, multiple thefts | Priority response |
| **P3 Medium** | Tailgating incident, single theft, suspicious person removed | Standard response |
| **P4 Low** | Lost badge, propped door, minor policy violation | Normal process |

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Security Manager | Overall coordination | [NAME/PHONE] |
| Facilities | Building systems, locksmith | [NAME/PHONE] |
| IT Security | Data/system implications | [NAME/PHONE] |
| HR | Employee matters | [NAME/PHONE] |
| Legal | Law enforcement liaison | [NAME/PHONE] |
| Building Security | Guards, patrols | [NAME/PHONE] |
| Police/Emergency | 911 or local number | [NUMBER] |

---

## 5. Immediate Response

### 5.1 Active Threat / Intruder

```
⚠️ SAFETY FIRST - If there is immediate danger to people:

□ Step 1: Ensure personal safety
  □ Do not confront intruders
  □ Move to safe location
  □ Call 911 if in danger
  □ Follow active threat procedures

□ Step 2: Alert others
  □ Activate panic alarm if available
  □ Notify building security
  □ Warn nearby colleagues

□ Step 3: Call emergency services
  □ Call 911 (or local emergency)
  □ Provide location, description, situation
  □ Stay on line until instructed

□ Step 4: Secure if safe to do so
  □ Lock doors
  □ Evacuate if appropriate
  □ Do not block exits
```

### 5.2 Unauthorized Access Detected (No Active Threat)

```
□ Step 5: Assess the situation
  □ Is anyone currently present?
  □ What area was accessed?
  □ Signs of forced entry?
  □ What is potentially affected?

□ Step 6: Notify security team
  □ Call Security Manager
  □ Alert building security/guards
  □ Document time of discovery

□ Step 7: Do not disturb the scene
  □ Avoid touching anything
  □ Do not clean up
  □ Preserve evidence for investigation
  □ Keep others away from area
```

### 5.3 Theft Discovered

```
□ Step 8: Document what's missing
  □ List of missing items
  □ Asset tags/serial numbers
  □ Last known location
  □ When last seen

□ Step 9: Preserve the scene
  □ Do not touch or move items
  □ Restrict access to area
  □ Note anything unusual

□ Step 10: Notify appropriate parties
  □ Security Manager
  □ IT Security (if IT equipment)
  □ Asset owner/department
  □ Police (if valuable or sensitive)
```

---

## 6. Containment

### 6.1 Access Control Actions

```
□ Step 11: Secure the facility

  Immediate Actions:
  □ Lock down affected area
  □ Post guard if needed
  □ Disable compromised badges
  □ Change access codes if needed
  □ Review and restrict after-hours access

  If Badge Compromised:
  □ Deactivate lost/stolen badge immediately
  □ Issue replacement with new credentials
  □ Review badge access history
  □ Check for unauthorized use
```

### 6.2 IT Equipment Considerations

```
□ Step 12: Address IT security implications

  If Computers/Servers Accessed:
  □ Notify IT Security immediately
  □ Assume data may be compromised
  □ Check for unauthorized access
  □ Review system logs
  □ Consider password resets

  If Storage Media Stolen:
  □ Identify data on device
  □ Determine if encrypted
  □ Assess data breach implications
  □ Follow Data Breach Playbook if applicable

  If Network Equipment Accessed:
  □ Check for tampering
  □ Review configurations
  □ Look for rogue devices
  □ Scan for unauthorized connections
```

### 6.3 Document/Paper Theft

```
□ Step 13: Address document theft

  Assessment:
  □ What documents are missing?
  □ Classification of documents?
  □ Personal data involved?
  □ Business sensitive information?

  Actions:
  □ Inventory affected files
  □ Notify document owners
  □ Assess breach implications
  □ Consider notifications required
```

---

## 7. Investigation

### 7.1 Evidence Collection

```
□ Step 14: Gather evidence

  Physical Evidence:
  □ Photograph the scene
  □ Document damage
  □ Note entry/exit points
  □ Preserve fingerprint areas
  □ Secure any items left behind

  Electronic Evidence:
  □ Pull CCTV footage
  □ Export access control logs
  □ Review alarm system logs
  □ Check nearby camera footage
  □ Preserve before overwrite

  Witness Information:
  □ Identify witnesses
  □ Collect statements
  □ Note who discovered incident
  □ Document timeline
```

### 7.2 Timeline Reconstruction

```
□ Step 15: Build timeline

  Determine:
  □ When did breach occur?
  □ How long was intruder present?
  □ What areas were accessed?
  □ What was taken/accessed?
  □ How did they enter/exit?

  Sources:
  □ Access control logs
  □ CCTV timestamps
  □ Witness accounts
  □ Alarm logs
  □ Last known good state
```

### 7.3 Root Cause Analysis

```
□ Step 16: Identify how it happened

  Entry Method:
  □ Forced entry?
  □ Tailgating?
  □ Stolen credentials?
  □ Social engineering?
  □ Insider?
  □ Security system failure?

  Contributing Factors:
  □ Security control gaps?
  □ Policy violations?
  □ Equipment failures?
  □ Staffing issues?
```

---

## 8. Recovery

### 8.1 Facility Restoration

```
□ Step 17: Restore physical security

  Repair and Secure:
  □ Repair damaged entry points
  □ Replace compromised locks
  □ Fix damaged security equipment
  □ Restore alarm systems
  □ Replace damaged cameras

  Enhanced Security:
  □ Increase patrols temporarily
  □ Add temporary cameras if needed
  □ Review and enhance access controls
  □ Brief security staff
```

### 8.2 Asset Recovery/Replacement

```
□ Step 18: Address stolen assets

  IT Equipment:
  □ Report to IT for tracking
  □ Enable remote wipe if possible
  □ Report to police with serial numbers
  □ File insurance claim
  □ Procure replacements

  Documents:
  □ Determine if copies exist
  □ Assess impact of loss
  □ Recreate if possible
  □ Notify affected parties
```

---

## 9. Law Enforcement

### 9.1 When to Involve Police

| Situation | Action |
|-----------|--------|
| Active threat to safety | Call 911 immediately |
| Break-in / forced entry | File police report |
| Theft over $[AMOUNT] | File police report |
| Vandalism | File police report |
| Sensitive data stolen | File police report + notify Legal |
| Repeated incidents | File police report |

### 9.2 Police Report Information

```
□ Step 19: Prepare for police report

  Have Ready:
  □ Incident description
  □ Date, time, location
  □ List of stolen items with values
  □ Serial numbers / asset tags
  □ Witness contact information
  □ CCTV footage availability
  □ Suspect description (if any)
  □ Business contact for follow-up
```

---

## 10. Communication

### 10.1 Internal Communication

| Audience | When | Content |
|----------|------|---------|
| Executive Team | P1/P2 immediately | Incident summary, impact |
| Department Heads | If their area affected | What happened, actions taken |
| All Staff | If awareness needed | Security reminder, guidance |
| Building Occupants | If safety concern | Advisory, instructions |

### 10.2 Communication Templates

**Staff Notification (If Needed):**
```
Subject: Security Incident - [Building/Location]

Team,

[We are investigating a security incident / There was a break-in]
at [LOCATION] on [DATE].

What Happened:
- [Brief description]

What We're Doing:
- [Security measures being taken]
- [Investigation status]

What You Should Do:
- Report any suspicious activity
- Ensure you badge in/out properly
- Do not prop open secure doors
- Report lost badges immediately

If you have any information about this incident, please contact
Security at [CONTACT].

[Security/Facilities Team]
```

---

## 11. Post-Incident

### 11.1 Documentation

```
□ Step 20: Complete incident documentation

  Incident Report Contents:
  □ Incident type and description
  □ Date, time, location
  □ How discovered
  □ Timeline of events
  □ Items stolen/damaged (with values)
  □ Areas accessed
  □ Response actions taken
  □ Police report number
  □ Insurance claim number
  □ Root cause
  □ Recommendations
```

### 11.2 Security Improvements

```
□ Step 21: Implement improvements

  Immediate Improvements:
  □ Fix identified vulnerabilities
  □ Address control gaps
  □ Update procedures
  □ Brief security staff

  Long-term Improvements:
  □ Security assessment
  □ Technology upgrades
  □ Policy updates
  □ Training enhancements
  □ Budget for improvements
```

### 11.3 Insurance

```
□ Step 22: Handle insurance matters

  Documentation for Claim:
  □ Police report
  □ Incident report
  □ List of losses with values
  □ Photos of damage
  □ Repair estimates
  □ Receipts for emergency repairs
```

---

## 12. Prevention Reference

### 12.1 Physical Security Controls

| Control | Purpose |
|---------|---------|
| Access control system | Restrict and log entry |
| CCTV | Deter and record |
| Security guards | Monitor and respond |
| Alarms | Detect and alert |
| Lighting | Deter and enable detection |
| Locks | Prevent unauthorized entry |
| Visitor management | Control and track visitors |

### 12.2 Best Practices

| Practice | Description |
|----------|-------------|
| Badge always visible | Wear badge where visible |
| Challenge unknown persons | Politely verify identity |
| No tailgating | Each person badges in |
| Secure workstations | Lock and secure devices |
| Report lost badges | Immediately report |
| Secure documents | Lock up sensitive documents |
| Report suspicious activity | If you see something, say something |

---

## 13. Emergency Contacts

| Contact | Number | When to Call |
|---------|--------|--------------|
| Emergency Services | 911 | Immediate danger |
| Building Security | [NUMBER] | 24/7 security issues |
| Security Manager | [NUMBER] | Incident coordination |
| Facilities | [NUMBER] | Building issues |
| Police Non-Emergency | [NUMBER] | Reports, follow-up |
| IT Security | [NUMBER] | IT equipment involved |

---

## 14. Related Documents

- [Physical Security Policy](../../policies/physical-security-policy.md)
- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Lost Device Playbook](./lost-device-playbook.md)
- [Data Breach Playbook](./data-breach-playbook.md)
- [Asset Management Policy](../../policies/asset-management-policy.md)

---

## 15. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

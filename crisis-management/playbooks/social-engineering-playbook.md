# Social Engineering Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides guidance for responding to social engineering attacks against [ORGANIZATION NAME], including voice phishing (vishing), pretexting, and in-person social engineering attempts.

### Scenarios Covered
- **Vishing**: Voice phishing calls
- **Pretexting**: False identity/story to gain information
- **Impersonation**: Posing as employee, vendor, or authority
- **Baiting**: Malicious USB or physical media
- **Tailgating**: Unauthorized physical access
- **Quid pro quo**: Offering something for information
- **BEC (Business Email Compromise)**: Executive impersonation fraud

For email phishing, see [Phishing Playbook](./phishing-playbook.md).

---

## 2. Detection Indicators

### 2.1 Vishing / Phone-Based

| Indicator | Description |
|-----------|-------------|
| Urgency/pressure | Caller creates false urgency |
| Authority claims | Claims to be IT, executive, law enforcement |
| Unusual requests | Requests for passwords, payments, personal info |
| Call back refusal | Won't provide callback number or verification |
| Poor caller ID | Spoofed or blocked number |
| Information already known | Uses public info to build trust |
| Threats | Threatens consequences for non-compliance |

### 2.2 Pretexting / Impersonation

| Indicator | Description |
|-----------|-------------|
| Unknown person | Claims to be employee/vendor but unknown |
| Verification resistance | Can't verify identity through normal channels |
| Unusual request | Asking for access, information, or actions outside normal process |
| Story inconsistencies | Details don't add up |
| Inappropriate questions | Asking about systems, security, personnel |

### 2.3 Physical Social Engineering

| Indicator | Description |
|-----------|-------------|
| Tailgating | Following employees through secure doors |
| Lost badge claims | Asking to be let in, claims lost badge |
| Delivery/contractor | Unexpected deliveries or service personnel |
| Baiting | USB drives, CDs found in common areas |
| Inappropriate access | Person in unauthorized areas |

### 2.4 BEC / Executive Fraud

| Indicator | Description |
|-----------|-------------|
| Urgency | Request must be done immediately |
| Secrecy | "Keep this confidential" |
| Unusual request | Wire transfer, gift cards, credentials |
| Slight email differences | Similar but not exact email address |
| Executive traveling | Claims executive is unavailable |
| Change in payment details | Vendor requesting new account |

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Financial fraud completed, credentials stolen, data breached | Immediate, all hands |
| **P2 High** | Fraud attempt in progress, sensitive info disclosed, physical breach | Priority response |
| **P3 Medium** | Unsuccessful attempt, no information disclosed | Standard response |
| **P4 Low** | Suspicious contact reported, no engagement | Document and monitor |

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Security Lead | Investigation coordination | [NAME/PHONE] |
| IT Security | Technical investigation | [NAME/PHONE] |
| Physical Security | Facility-related incidents | [NAME/PHONE] |
| HR | Employee matters | [NAME/PHONE] |
| Finance | Financial fraud matters | [NAME/PHONE] |
| Legal | Law enforcement, legal matters | [NAME/PHONE] |

---

## 5. Immediate Response by Scenario

### 5.1 Vishing / Suspicious Call (Active)

**If currently on a suspicious call:**

```
□ Step 1: Recognize the signs
  - Urgency, pressure, threats
  - Requests for credentials, payment, or sensitive info
  - Caller can't verify identity

□ Step 2: Don't provide information
  - Do NOT give passwords, codes, or personal info
  - Do NOT confirm employee information
  - Do NOT make payments or transfers

□ Step 3: Verify independently
  - Ask for callback number
  - Say you'll call back through official channels
  - Look up company number independently
  - Verify request through known contacts

□ Step 4: End the call
  - "I'll need to verify this request through official channels"
  - It's OK to hang up on suspicious callers

□ Step 5: Report immediately
  - Note caller ID, time, what was said
  - Report to IT Security immediately
  - Don't feel embarrassed - reporting helps
```

### 5.2 Vishing / Suspicious Call (Completed)

```
□ Step 6: Assess what was disclosed

  If Credentials Disclosed:
  → Follow [Account Compromise Playbook](./account-compromise-playbook.md)
  □ Change password immediately
  □ Report to IT Security
  □ Check for unauthorized access

  If Financial Information Disclosed:
  □ Notify Finance immediately
  □ Contact bank if account details shared
  □ Monitor for unauthorized transactions

  If Personal Information Disclosed:
  □ Document what was shared
  □ Consider identity protection measures
  □ Report to Security

□ Step 7: Document the incident
  - Caller's claimed identity
  - Phone number (if available)
  - Time and duration
  - What was requested
  - What was disclosed
  - Exact language used
```

### 5.3 BEC / Executive Fraud Attempt

```
□ Step 8: Stop and verify

  Before Any Action:
  □ STOP - Don't act on urgency
  □ VERIFY - Confirm through known channels
  □ Call the executive directly (not reply to email)
  □ Ask someone else to verify

□ Step 9: If fraud was successful
  → This is P1 Critical - Escalate immediately

  Financial Fraud:
  □ Contact bank IMMEDIATELY
  □ Request wire recall (time is critical)
  □ Notify Finance leadership
  □ Notify Legal
  □ Preserve all communications

□ Step 10: Investigate the email
  □ Check email headers
  □ Compare to legitimate executive emails
  □ Check for email account compromise
  □ Look for inbox rules/forwarding
```

### 5.4 Physical Social Engineering

```
□ Step 11: Tailgating / Unauthorized access

  If You Observe:
  □ Politely ask person to badge in
  □ Offer to call their host
  □ Do not let unknown persons follow you
  □ Report to Security if suspicious

  If Unauthorized Person Inside:
  □ Don't confront if you feel unsafe
  □ Note description and location
  □ Call Security immediately
  □ Monitor from safe distance

□ Step 12: Baiting (suspicious USB/media)
  □ DO NOT plug it in
  □ Note where it was found
  □ Report to IT Security
  □ IT Security will safely analyze
```

### 5.5 Impersonation / Pretexting

```
□ Step 13: Verify identity

  For Unknown "Employees":
  □ Ask for employee ID
  □ Look up in directory
  □ Call their manager
  □ Escort to Security if unverified

  For Unknown "Vendors/Contractors":
  □ Check with facilities/procurement
  □ Verify work order exists
  □ Escort until verified
  □ Issue visitor badge

  For "IT Support" Calls:
  □ Ask for ticket number
  □ Call IT Help Desk to verify
  □ IT will never ask for password
```

---

## 6. Investigation

### 6.1 Gather Information

```
□ Step 14: Document the attempt

  For Phone-Based:
  □ Caller ID / phone number
  □ Time and date
  □ Duration of call
  □ Caller's claimed identity
  □ What was requested
  □ What was disclosed
  □ Caller's manner/script

  For In-Person:
  □ Physical description
  □ Location observed
  □ Time observed
  □ What they said/requested
  □ Witnesses
  □ Security camera footage

  For Email-Based:
  □ Full email headers
  □ Sending address analysis
  □ Email content
  □ Any links or attachments
```

### 6.2 Assess Impact

```
□ Step 15: Determine what was compromised

  Information Disclosed:
  □ Credentials
  □ Personal information
  □ Financial information
  □ Business confidential
  □ Customer data
  □ System information

  Access Granted:
  □ Physical access
  □ System access
  □ Data access

  Actions Taken:
  □ Payments made
  □ Information sent
  □ Changes made
```

### 6.3 Identify Scope

```
□ Step 16: Check for broader campaign
  □ Were others targeted?
  □ Similar attempts reported?
  □ Part of a coordinated attack?
  □ Organization-wide alert needed?
```

---

## 7. Containment and Remediation

### 7.1 Address Immediate Damage

```
□ Step 17: Remediate based on impact

  Credentials Compromised:
  → [Account Compromise Playbook](./account-compromise-playbook.md)

  Financial Fraud:
  □ Contact bank immediately
  □ Attempt wire recall
  □ File fraud report
  □ Notify law enforcement

  Physical Breach:
  □ Review security footage
  □ Assess what was accessed
  □ Check for planted devices
  □ Review badge access logs
```

### 7.2 Prevent Further Attempts

```
□ Step 18: Block and warn
  □ Block caller number (if known)
  □ Block sending email domain
  □ Alert staff of specific tactic
  □ Update email filters
  □ Brief reception/security
```

---

## 8. Communication

### 8.1 Awareness Alert

```
If active campaign detected, alert organization:

Subject: Security Alert - Social Engineering Attempts

Team,

We have identified social engineering attempts targeting our
organization. Please be aware of the following:

Type of Attack: [Vishing/BEC/etc.]
What to Watch For:
- [Specific indicators]
- [Example script/approach used]

What to Do:
- Do not provide [credentials/information/etc.]
- Verify all unusual requests through known channels
- Report suspicious contacts to IT Security at [CONTACT]

Remember: It's OK to be suspicious. Always verify.

IT Security Team
```

### 8.2 Stakeholder Communication

| Audience | When | Content |
|----------|------|---------|
| Affected Employee | Immediately | Support, no blame, next steps |
| Employee's Manager | If disclosure occurred | Incident awareness |
| Finance | If financial fraud | Immediate notification |
| Executive Team | If P1/P2 | Impact summary |
| All Staff | If widespread campaign | Awareness alert |

---

## 9. Post-Incident

### 9.1 Documentation

```
□ Step 19: Complete incident report
  - Full incident timeline
  - Attack methodology
  - What worked (for attacker)
  - What worked (for defense)
  - Impact assessment
  - Recommendations
```

### 9.2 Lessons Learned

```
□ Step 20: Improve defenses

  Training Updates:
  □ Add to security awareness content
  □ Create simulations based on real attack
  □ Brief high-risk groups (finance, reception)

  Process Improvements:
  □ Strengthen verification procedures
  □ Update payment authorization process
  □ Improve visitor management

  Technical Controls:
  □ Enhance email filtering
  □ Improve caller ID/VOIP protections
  □ Add verification tools
```

---

## 10. Prevention Reference

### 10.1 Verification Procedures

| Request Type | Verification Method |
|--------------|---------------------|
| Password reset | Must go through Help Desk |
| Wire transfer | Two-person approval, verbal confirmation |
| Vendor payment change | Verify via known contact |
| Executive request | Call executive directly |
| System access | Ticket required |
| Physical access | Badge + escort policy |

### 10.2 Red Flags to Watch

| Category | Red Flags |
|----------|-----------|
| Urgency | "Must be done immediately," "Don't tell anyone" |
| Authority | "CEO asked for this," "I'm from IT" |
| Fear | "Your account will be closed," "Legal consequences" |
| Trust | Uses your name, knows details |
| Helpfulness | "I'm trying to help you" |

### 10.3 Safe Responses

| Situation | Response |
|-----------|----------|
| Unexpected call requesting info | "I'll call you back at the main number" |
| Email requesting payment | "I'll verify through our normal process" |
| Someone without badge | "Let me call security to help you" |
| USB drive found | "I'll turn this in to IT" |
| Unusual request from boss | "I'll verify with you directly" |

---

## 11. Related Documents

- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Phishing Playbook](./phishing-playbook.md)
- [Account Compromise Playbook](./account-compromise-playbook.md)
- [Data Breach Playbook](./data-breach-playbook.md)
- [Physical Security Policy](../../policies/physical-security-policy.md)

---

## 12. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

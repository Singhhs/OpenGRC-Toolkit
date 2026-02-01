# Phishing Incident Playbook

**Severity:** Typically Medium (P3) to High (P2)
**Last Updated:** [DATE]
**Owner:** [ROLE]

---

## 1. Overview

This playbook covers response to phishing attacks, including email phishing, spear phishing, and business email compromise (BEC).

## 2. Incident Types

| Type | Description | Typical Severity |
|------|-------------|------------------|
| **Mass Phishing** | Generic phishing sent to many employees | Medium |
| **Spear Phishing** | Targeted attack on specific individuals | High |
| **Whaling** | Targeting executives | High/Critical |
| **BEC** | Business Email Compromise | High/Critical |
| **Credential Harvesting** | Fake login pages | Medium-High |
| **Malware Delivery** | Phishing with malicious attachments | High |

## 3. Detection Indicators

### Phishing Indicators

- [ ] Suspicious sender address (misspelling, external domain)
- [ ] Urgent or threatening language
- [ ] Request for credentials or sensitive info
- [ ] Suspicious links or attachments
- [ ] Poor grammar/spelling
- [ ] Mismatched URLs (hover vs. display)
- [ ] Unexpected attachment types
- [ ] Request to bypass normal procedures

### Compromise Indicators

- [ ] User reports clicking link or opening attachment
- [ ] User reports entering credentials
- [ ] Suspicious login activity
- [ ] Unusual email sending patterns
- [ ] Rules/forwards added to mailbox
- [ ] Security alerts triggered

## 4. Severity Assessment

| Scenario | Severity | Response |
|----------|----------|----------|
| Phishing reported, no clicks | Low | Block and educate |
| User clicked, no credentials entered | Medium | Scan endpoint, monitor |
| Credentials entered | High | Full account compromise response |
| Malware executed | High | Malware response |
| BEC with financial impact | Critical | Full incident response |
| Multiple users compromised | High/Critical | Campaign response |

## 5. Response Procedures

### Scenario A: Phishing Reported (No Interaction)

**Timeline:** Complete within 2 hours

1. [ ] Obtain original phishing email (as attachment)
2. [ ] Analyze email:
   - [ ] Sender address
   - [ ] Reply-to address
   - [ ] Links in email
   - [ ] Attachments
   - [ ] Headers
3. [ ] Check if others received same email
4. [ ] Block sender at email gateway
5. [ ] Block malicious URLs at web filter
6. [ ] Remove email from all inboxes
7. [ ] Send awareness reminder if widespread
8. [ ] Thank reporter

---

### Scenario B: User Clicked Link (No Credentials)

**Timeline:** Complete within 4 hours

1. [ ] All steps from Scenario A
2. [ ] Identify what user clicked on
3. [ ] Scan user's endpoint for malware
4. [ ] Review browser history
5. [ ] Check for downloads
6. [ ] Monitor for suspicious activity
7. [ ] If malware found → [Malware Playbook](./malware-playbook.md)

---

### Scenario C: Credentials Compromised

**Timeline:** Immediate response

#### Immediate Actions (First 30 Minutes)

1. [ ] **Reset password** immediately
2. [ ] **Revoke all sessions** (force re-authentication)
3. [ ] **Review and remove** any:
   - [ ] Email forwarding rules
   - [ ] Inbox rules
   - [ ] Delegates
   - [ ] Connected applications
4. [ ] **Enable MFA** if not already enabled
5. [ ] **Review recent activity**:
   - [ ] Email sent
   - [ ] Files accessed
   - [ ] Data downloaded

#### Investigation

6. [ ] Check login history:
   - [ ] Unusual locations
   - [ ] Unusual times
   - [ ] Multiple concurrent sessions
7. [ ] Review email sent from account
8. [ ] Check for data exfiltration
9. [ ] Identify other accounts with same password
10. [ ] Check if user is privileged user

#### Communication

11. [ ] Notify user of compromise
12. [ ] Provide guidance on password changes
13. [ ] Advise monitoring for fraud
14. [ ] Document incident

---

### Scenario D: Business Email Compromise (BEC)

**Timeline:** Immediate response - potential financial loss

#### Immediate Actions

1. [ ] **Stop any pending transactions** related to BEC
2. [ ] Alert finance team immediately
3. [ ] Contact bank if funds transferred
4. [ ] Preserve all communications
5. [ ] Identify scope of compromise

#### If Funds Were Transferred

6. [ ] Contact sending bank immediately
7. [ ] Request recall/reversal
8. [ ] Contact receiving bank
9. [ ] File report with law enforcement
10. [ ] Contact FBI IC3 (US)
11. [ ] Contact cyber insurance carrier

#### Investigation

12. [ ] Determine how attacker gained access
13. [ ] Review all email communications
14. [ ] Identify other potential victims
15. [ ] Document complete timeline
16. [ ] Preserve evidence for law enforcement

---

### Scenario E: Phishing Campaign (Multiple Users)

**Timeline:** Priority response

1. [ ] Activate CSIRT
2. [ ] Identify all recipients
3. [ ] Block at email gateway and web filter
4. [ ] Remove from all inboxes
5. [ ] Identify who interacted:
   - [ ] Clicked link
   - [ ] Entered credentials
   - [ ] Opened attachment
6. [ ] Respond to each based on scenario above
7. [ ] Send organization-wide alert
8. [ ] Increase monitoring
9. [ ] Consider password reset for exposed users

---

## 6. Technical Response Actions

### Email Analysis

| Check | How | What to Look For |
|-------|-----|------------------|
| Sender | View headers | Spoofed domain, external |
| Reply-to | View headers | Different from sender |
| Links | Hover/inspect | Mismatch, suspicious domain |
| Attachments | Do not open | Unexpected file types |
| Headers | Full headers | SPF/DKIM/DMARC fails |

### Email Blocking

```
Block sender domain: [Instructions for your email system]
Block URLs: [Instructions for your web filter]
Remove from inboxes: [Instructions for your email system]
```

### Account Remediation

```
Reset password: [Instructions]
Revoke sessions: [Instructions]
Check mail rules: [Instructions]
Review audit logs: [Instructions]
```

## 7. Communication

### Internal Notification

**To Users (if widespread):**
```
Subject: SECURITY ALERT: Phishing emails in circulation

We have identified phishing emails targeting our organization.

DO NOT:
- Click links in suspicious emails
- Open unexpected attachments
- Provide credentials or sensitive info

If you received a suspicious email:
- Do not interact with it
- Report to [security@company.com / phishing button]

If you clicked a link or entered credentials:
- Contact IT Security immediately: [PHONE]

[IT Security Team]
```

## 8. Evidence Collection

Preserve:
- [ ] Original phishing email (as .eml or .msg)
- [ ] Email headers
- [ ] Screenshots
- [ ] User statement
- [ ] Login logs
- [ ] Email audit logs
- [ ] Endpoint scan results

## 9. Post-Incident

### For All Phishing Incidents

1. [ ] Update email filters
2. [ ] Add indicators to blocklist
3. [ ] Share IOCs with threat intelligence
4. [ ] Consider awareness training refresh
5. [ ] Document lessons learned

### For Credential Compromise

1. [ ] Verify no ongoing access
2. [ ] Ensure MFA enabled
3. [ ] Review for additional indicators
4. [ ] Consider monitoring affected accounts
5. [ ] Follow up with user on awareness

### For BEC/Financial

1. [ ] Complete incident report
2. [ ] Work with legal on recovery
3. [ ] Review and strengthen approval processes
4. [ ] Implement additional verification controls
5. [ ] Report to insurance if applicable

## 10. Prevention Recommendations

After incident, consider:

- [ ] Enable MFA for all users
- [ ] Implement email authentication (SPF, DKIM, DMARC)
- [ ] Deploy advanced email security
- [ ] Conduct phishing simulations
- [ ] Implement verification procedures for financial changes
- [ ] Regular security awareness training

## 11. Quick Reference Card

```
PHISHING RESPONSE QUICK GUIDE

REPORTED (No Click):
1. Get original email
2. Block sender/URLs
3. Remove from inboxes
4. Thank reporter

CLICKED LINK:
+ Scan endpoint for malware

CREDENTIALS ENTERED:
1. Reset password NOW
2. Revoke sessions
3. Remove mail rules/forwards
4. Review activity
5. Enable MFA

BEC/FINANCIAL:
1. Stop transactions
2. Alert finance
3. Contact bank immediately
4. Report to law enforcement

Report to: [SECURITY CONTACT]
```

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

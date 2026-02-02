# Account Compromise Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides step-by-step guidance for responding to compromised user accounts at [ORGANIZATION NAME], including credential theft, unauthorized access, and account takeover incidents.

### Scenarios Covered
- Compromised user credentials (phishing, breach)
- Unauthorized account access
- Account takeover
- Privilege escalation
- Service account compromise
- Privileged account compromise (admin, root)

---

## 2. Detection Indicators

### 2.1 Authentication Anomalies

| Indicator | Description |
|-----------|-------------|
| Impossible travel | Logins from geographically distant locations |
| Unusual login times | Access outside normal working hours |
| Failed login attempts | Multiple failures followed by success |
| New device/browser | Login from unrecognized device |
| Unusual location | Login from unexpected country/region |
| Multiple concurrent sessions | Same account active in multiple locations |
| MFA bypass attempts | Repeated MFA failures or resets |
| Password change | Unexpected password reset |

### 2.2 Behavioral Indicators

| Indicator | Description |
|-----------|-------------|
| Unusual data access | Accessing files not normally accessed |
| Large data downloads | Bulk file downloads |
| Email forwarding rules | New forwarding to external addresses |
| Mailbox delegation | Unexpected mailbox access grants |
| Permission changes | Unusual privilege modifications |
| Account modifications | Changes to security settings |
| Unusual application access | Access to unfamiliar applications |

### 2.3 External Indicators

| Indicator | Description |
|-----------|-------------|
| Credential in breach database | User credentials found in data breach |
| Dark web exposure | Credentials posted on dark web |
| User report | User reports they didn't perform action |
| Partner notification | Third party reports suspicious activity |
| Phishing confirmation | User confirmed clicking phishing link |

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Privileged account, active abuse, data exfiltration | Immediate, all hands |
| **P2 High** | Multiple accounts, sensitive data access, executive account | Priority response |
| **P3 Medium** | Single account, limited access, contained | Standard response |
| **P4 Low** | Credentials exposed but no confirmed abuse | Preventive action |

### Account Type Severity Multiplier

| Account Type | Severity Factor |
|--------------|-----------------|
| Domain Admin / Root | +2 levels |
| IT Administrator | +1 level |
| Executive | +1 level |
| Finance/HR | +1 level |
| Service Account | +1 level |
| Standard User | Baseline |

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Incident Commander | Overall coordination | [NAME/PHONE] |
| Security Analyst | Investigation, analysis | [NAME/PHONE] |
| Identity Team | Account actions, access review | [NAME/PHONE] |
| IT Support | User communication, system access | [NAME/PHONE] |
| HR Contact | Employee matters | [NAME/PHONE] |
| Legal Contact | If data breach implications | [NAME/PHONE] |

---

## 5. Immediate Actions (First 15 Minutes)

### 5.1 Confirm Compromise

```
□ Step 1: Gather initial information
  - Account name/email
  - How compromise was detected
  - Timeline of suspicious activity
  - Account type and privileges
  - Systems/data accessible

□ Step 2: Verify compromise indicators
  - Review authentication logs
  - Check for impossible travel
  - Review recent account activity
  - Check for suspicious actions:
    • Email forwarding rules
    • Password changes
    • MFA changes
    • Permission changes

□ Step 3: Assess scope
  - Single account or multiple?
  - Which systems accessed?
  - What data potentially exposed?
  - Any lateral movement?
```

### 5.2 Immediate Containment

```
□ Step 4: Disable/contain the account

  CRITICAL - Do immediately:

  For Active Abuse:
  □ Disable the account immediately
  □ Terminate all active sessions
  □ Block sign-ins
  □ Revoke refresh tokens

  For Suspected Compromise (no active abuse):
  □ Force password reset
  □ Reset MFA
  □ Terminate sessions
  □ Enable enhanced monitoring

□ Step 5: Preserve evidence
  - Export authentication logs
  - Export account activity logs
  - Document current state
  - Screenshot suspicious activity
```

---

## 6. Containment

### 6.1 Account Containment Actions

```
□ Step 6: Comprehensive account lockdown

  Identity Provider (Azure AD, Okta, etc.):
  □ Disable sign-in
  □ Revoke all sessions
  □ Revoke refresh tokens
  □ Remove from all groups (temporary)
  □ Disable MFA devices

  Email (Microsoft 365, Google Workspace):
  □ Remove email forwarding rules
  □ Remove mailbox delegates
  □ Remove inbox rules
  □ Block ActiveSync/mobile access
  □ Review sent items

  Applications:
  □ Revoke OAuth app consents
  □ Remove API tokens
  □ Review connected applications
  □ Reset application passwords
```

### 6.2 Prevent Lateral Movement

```
□ Step 7: Check for expanded access

  Review Recent Activity:
  □ Systems accessed
  □ Files accessed/downloaded
  □ Emails sent
  □ Permission changes made
  □ New accounts created
  □ Password resets initiated

□ Step 8: Secure related accounts
  - Reset passwords for accounts accessed by compromised user
  - Check for shared credentials
  - Review service accounts user had access to
  - Check for privilege escalation
```

### 6.3 Privileged Account Special Actions

```
□ Step 9: For privileged accounts (admin, root, service)

  Immediate Actions:
  □ Disable account
  □ Rotate all associated credentials
  □ Review all administrative actions
  □ Check for persistence (backdoors, new accounts)
  □ Review configuration changes
  □ Check scheduled tasks/cron jobs
  □ Audit group memberships

  Systems Administration:
  □ Rotate service account passwords
  □ Regenerate API keys
  □ Review infrastructure access
  □ Check for unauthorized changes
```

---

## 7. Investigation

### 7.1 Determine Compromise Method

```
□ Step 10: Identify how credentials were compromised

  Common Methods:
  □ Phishing email - Review email logs for phishing
  □ Credential breach - Check haveibeenpwned, breach databases
  □ Malware/keylogger - Scan user's endpoint
  □ Password reuse - User used same password elsewhere
  □ Brute force - Review failed login patterns
  □ Social engineering - Interview user
  □ Insider threat - Review for intentional sharing
  □ Man-in-the-middle - Review network indicators

□ Step 11: Document attack timeline
  - When did compromise occur?
  - First unauthorized access
  - Activities performed
  - Data accessed/exfiltrated
  - Last unauthorized access
```

### 7.2 Assess Impact

```
□ Step 12: Determine data exposure

  Data Assessment:
  □ Emails accessed/sent
  □ Files accessed/downloaded
  □ Applications accessed
  □ Data shared externally
  □ Confidential information exposed
  □ Personal data (PII) involved

□ Step 13: Determine system impact
  □ Configuration changes
  □ New accounts created
  □ Persistence mechanisms
  □ Malware installed
  □ Lateral movement
```

---

## 8. Eradication

### 8.1 Remove Attacker Access

```
□ Step 14: Complete access removal

  Account Cleanup:
  □ All sessions terminated
  □ All tokens revoked
  □ All connected apps removed
  □ All forwarding rules removed
  □ All delegates removed
  □ MFA devices reset

  System Cleanup:
  □ Remove any backdoors identified
  □ Remove unauthorized accounts
  □ Remove persistence mechanisms
  □ Reverse configuration changes
  □ Remove malware if present
```

### 8.2 Secure the Account

```
□ Step 15: Prepare account for restoration

  Security Enhancements:
  □ Strong unique password set
  □ MFA re-enrolled (different method if phone compromised)
  □ Recovery options updated
  □ Security questions reset (if used)
  □ Review and minimize permissions
```

---

## 9. Recovery

### 9.1 Account Restoration

```
□ Step 16: Restore account access

  Pre-Restoration Checklist:
  □ Investigation complete
  □ All attacker access removed
  □ Root cause addressed
  □ New credentials set
  □ MFA configured
  □ User educated on incident

□ Step 17: Re-enable account
  □ Enable sign-in
  □ Restore group memberships (review first)
  □ Restore application access (review first)
  □ Test access with user
  □ Provide new credentials securely
```

### 9.2 User Communication

```
□ Step 18: Brief the user

  Cover With User:
  - What happened (appropriate detail)
  - How to sign in with new credentials
  - MFA setup instructions
  - What to watch for
  - How to report suspicious activity
  - Password security best practices
```

### 9.3 Monitoring

```
□ Step 19: Enhanced monitoring
  □ Enable detailed logging for account
  □ Set up alerts for suspicious activity
  □ Monitor for 30 days minimum
  □ Review activity weekly
```

---

## 10. Communication

### 10.1 Internal Communication

| Audience | When | Content |
|----------|------|---------|
| Affected User | Immediately | Account secured, instructions |
| User's Manager | P1/P2 | Incident summary, user status |
| IT Teams | As needed | IoCs, monitoring guidance |
| Executive Team | P1/P2 | Impact summary, response status |
| HR | If policy violation | Incident details |

### 10.2 User Communication Templates

**Initial Notification:**
```
Subject: Important: Security Action Required for Your Account

[Name],

Our security team has detected suspicious activity on your account.
As a precaution, we have temporarily secured your account.

What you need to do:
1. Do not attempt to log in until contacted
2. Contact IT Security at [PHONE/EMAIL]
3. Be prepared to verify your identity
4. Have your phone ready for MFA setup

This is being handled as a priority. We will contact you shortly
with next steps.

IT Security Team
```

**Account Restoration:**
```
Subject: Your Account Has Been Secured - Action Required

[Name],

Your account has been secured following a security incident.
Please follow these steps to regain access:

1. Go to [LOGIN URL]
2. Use this temporary password: [Provided separately]
3. You will be required to set a new password
4. Follow the prompts to set up MFA

Important Security Reminders:
- Use a unique password not used elsewhere
- Never share your password or MFA codes
- Report any suspicious emails or requests

If you have questions, contact [SUPPORT].

IT Security Team
```

---

## 11. Special Scenarios

### 11.1 Executive Account Compromise

```
Additional Steps:
□ Immediate escalation to CISO and Legal
□ Check for BEC (Business Email Compromise)
□ Review recent emails for fraud attempts
□ Alert finance of potential wire fraud
□ Review calendar for sensitive meetings
□ Consider PR/communications implications
```

### 11.2 Service Account Compromise

```
Additional Steps:
□ Identify all systems using the account
□ Rotate credentials on all systems
□ Review all automated processes
□ Check for unauthorized API calls
□ Review application logs
□ Consider key/certificate rotation
```

### 11.3 Multiple Account Compromise

```
Additional Steps:
□ Treat as potential broader breach
□ Identify common factor (same phishing, same password)
□ Wider credential reset may be needed
□ Check for compromised identity infrastructure
□ Escalate to P1
```

---

## 12. Post-Incident

### 12.1 Documentation

```
□ Step 20: Complete documentation
  - Incident timeline
  - Accounts affected
  - Compromise method
  - Data exposure
  - Actions taken
  - Lessons learned
```

### 12.2 Post-Incident Review (Within 1 Week)

```
□ Step 21: Review and improve
  - How were credentials compromised?
  - Was detection timely?
  - Was response effective?
  - What prevented earlier detection?
  - What controls to improve?

□ Step 22: Implement improvements
  - Enhance detection rules
  - Improve authentication controls
  - Update user training
  - Strengthen password policies
  - Consider additional MFA
```

---

## 13. Prevention Reference

### 13.1 Authentication Controls

| Control | Purpose |
|---------|---------|
| MFA everywhere | Prevent password-only access |
| Conditional access | Risk-based authentication |
| Password policies | Strong, unique passwords |
| Password monitoring | Detect breached passwords |
| Session management | Limit session duration |

### 13.2 Detection Controls

| Control | Purpose |
|---------|---------|
| Impossible travel alerts | Detect geographic anomalies |
| Failed login monitoring | Detect brute force |
| Behavioral analytics | Detect unusual patterns |
| New device alerts | Detect new access sources |
| Privilege monitoring | Detect escalation |

---

## 14. Tools and Resources

| Tool | Purpose | Location |
|------|---------|----------|
| [Identity Provider Admin] | Account management | [URL] |
| [SIEM] | Log analysis | [URL] |
| [Email Security] | Email investigation | [URL] |
| HaveIBeenPwned | Breach checking | haveibeenpwned.com |
| [EDR] | Endpoint investigation | [URL] |

---

## 15. Related Documents

- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Access Control Policy](../../policies/access-control-policy.md)
- [Phishing Playbook](./phishing-playbook.md)
- [Data Breach Playbook](./data-breach-playbook.md)

---

## 16. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

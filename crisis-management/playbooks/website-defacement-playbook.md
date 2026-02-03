# Website Defacement Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides guidance for responding to website defacement incidents at [ORGANIZATION NAME], where attackers modify the visual appearance or content of public-facing websites.

### Scenarios Covered
- Homepage or page content replacement
- Unauthorized content injection
- Political or hacktivist messages
- Malicious redirect insertion
- SEO spam injection
- Cryptominer script injection
- Drive-by download insertion

### Why Defacement Matters

While often dismissed as "just cosmetic," website defacement indicates:
- Attackers have gained write access to web infrastructure
- Deeper compromise may exist (databases, backend systems)
- Reputational damage occurs immediately
- Customer trust is impacted
- The same access could be used for more harmful attacks

---

## 2. Detection Indicators

### 2.1 Visual Indicators

| Indicator | Description |
|-----------|-------------|
| Changed homepage | Obvious replacement of homepage content |
| Political/hacktivist messages | Messages from threat groups |
| Unusual images or text | Content not created by organization |
| Foreign language content | Unexpected language on pages |
| Missing content | Legitimate content removed |
| Broken functionality | Site features not working |

### 2.2 Technical Indicators

| Indicator | Description |
|-----------|-------------|
| File modification alerts | IDS/monitoring detecting file changes |
| Unexpected file timestamps | Recently modified files |
| New or modified scripts | JavaScript, PHP, or other code changes |
| Modified .htaccess | Redirect rules changed |
| Database content changes | CMS content modified |
| Unauthorized admin access | Unknown logins to CMS/admin panels |
| Web shell presence | Backdoor scripts uploaded |

### 2.3 External Reports

| Source | Description |
|--------|-------------|
| Customer reports | Users reporting strange content |
| Social media | Public posts about defacement |
| Search engine alerts | Google Search Console warnings |
| Security researchers | External notification of compromise |
| Defacement archives | Site appearing on zone-h or similar |

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Customer-facing site, malware distributed, ongoing attack, data breach suspected | Immediate, all hands |
| **P2 High** | Primary website defaced, high visibility, business impact | Priority response |
| **P3 Medium** | Secondary site defaced, limited visibility, no malware | Standard response |
| **P4 Low** | Internal site, minimal visibility, quickly detected | Normal process |

### Escalation Triggers

Escalate to P1 if:
- Malware or malicious scripts are being served
- Customer data may be compromised
- Attack is ongoing/spreading
- Media attention is likely or occurring
- Regulatory notification may be required

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Incident Commander | Overall coordination | [NAME/PHONE] |
| Web/Application Team | Site restoration, investigation | [NAME/PHONE] |
| Security Team | Forensics, root cause analysis | [NAME/PHONE] |
| Communications | External messaging, social media | [NAME/PHONE] |
| Legal | If data breach suspected | [NAME/PHONE] |
| Hosting/Infrastructure | Server access, logs | [NAME/PHONE] |

---

## 5. Immediate Actions (First 30 Minutes)

### 5.1 Confirm and Document

```
□ Step 1: Verify the defacement
  □ Access the site from multiple locations/devices
  □ Check if all pages affected or specific pages
  □ Determine if defacement is visible to all users
  □ Check cached versions (Google cache, Wayback Machine)

□ Step 2: Document the defacement
  □ Take screenshots of all affected pages
  □ Save HTML source of defaced pages
  □ Record exact URLs affected
  □ Note any messages, names, or signatures left by attacker
  □ Check for embedded scripts or iframes
  □ Document timestamp of discovery
```

### 5.2 Initial Containment Decision

```
□ Step 3: Decide on immediate action

  TAKE SITE OFFLINE if:
  □ Malware is being distributed
  □ Malicious redirects are active
  □ Customer data input forms are compromised
  □ Attack appears ongoing
  □ Cannot quickly restore clean content

  KEEP SITE ONLINE (with monitoring) if:
  □ Defacement is static/cosmetic only
  □ Can quickly restore from backup
  □ Need to preserve evidence
  □ Taking offline causes greater business impact

□ Step 4: If taking offline
  □ Replace with maintenance page
  □ Update DNS or load balancer as needed
  □ Notify stakeholders of intentional outage
  □ Preserve server state for forensics
```

### 5.3 Immediate Notifications

```
□ Step 5: Alert response team
  □ Notify Incident Commander
  □ Alert web/application team
  □ Notify security team
  □ Brief communications team
  □ Establish incident channel (Slack/Teams)
```

---

## 6. Containment

### 6.1 Isolate and Preserve

```
□ Step 6: Preserve evidence before making changes

  Server Evidence:
  □ Take snapshot/image of affected server(s)
  □ Export web server access logs
  □ Export web server error logs
  □ Export application logs
  □ Export FTP/SFTP access logs
  □ Capture file system state (modified files list)

  Network Evidence:
  □ Capture relevant firewall logs
  □ Export WAF logs
  □ Check CDN logs if applicable

  Application Evidence:
  □ Export CMS audit logs
  □ Export database change logs
  □ Document CMS user accounts
```

### 6.2 Contain the Attack

```
□ Step 7: Stop ongoing access

  Credential Actions:
  □ Reset all CMS/admin passwords
  □ Reset FTP/SFTP credentials
  □ Rotate SSH keys
  □ Invalidate all active sessions
  □ Reset database passwords
  □ Rotate API keys

  Access Controls:
  □ Review and restrict admin access
  □ Block suspicious IP addresses
  □ Enable additional authentication (MFA)
  □ Review and remove unknown user accounts

  If Web Shell Suspected:
  □ Scan for known web shell signatures
  □ Check for recently modified PHP/ASP files
  □ Look for files with suspicious names
  □ Check upload directories
```

### 6.3 Check for Deeper Compromise

```
□ Step 8: Assess if compromise extends beyond defacement

  Check for:
  □ Database access or exfiltration
  □ Customer data exposure
  □ Backend system access
  □ Lateral movement to other systems
  □ Persistence mechanisms
  □ Additional malware or backdoors

  If deeper compromise suspected:
  → Escalate to P1
  → Follow Data Breach Playbook if data affected
  → Expand investigation scope
```

---

## 7. Investigation

### 7.1 Determine Attack Vector

```
□ Step 9: Identify how attacker gained access

  Common Attack Vectors:
  □ CMS vulnerability (WordPress, Drupal, etc.)
  □ Plugin/theme vulnerability
  □ Compromised credentials (phishing, reuse)
  □ SQL injection
  □ File upload vulnerability
  □ Server misconfiguration
  □ Compromised hosting account
  □ Supply chain (compromised dependency)
  □ Insider threat

  Investigation Steps:
  □ Review access logs for suspicious activity
  □ Check for vulnerability exploitation patterns
  □ Review authentication logs for unusual logins
  □ Check for recently installed plugins/themes
  □ Review file upload logs
  □ Correlate attack time with log entries
```

### 7.2 Build Timeline

```
□ Step 10: Construct incident timeline

  Determine:
  □ When did unauthorized access first occur?
  □ What was the initial entry point?
  □ What actions did the attacker take?
  □ When was defacement published?
  □ When was it detected?
  □ Were there multiple access sessions?
```

### 7.3 Identify Threat Actor

```
□ Step 11: Gather threat intelligence

  From Defacement:
  □ Any signatures or group names?
  □ Political or ideological messages?
  □ Links to defacement archives?
  □ Known hacktivist group tactics?

  Technical Indicators:
  □ Source IP addresses
  □ User agent strings
  □ Attack patterns
  □ Tools or techniques used
```

---

## 8. Eradication

### 8.1 Remove Malicious Content

```
□ Step 12: Clean the environment

  Option A - Restore from Backup:
  □ Identify last known clean backup
  □ Verify backup integrity
  □ Restore files from backup
  □ Restore database if affected
  □ Verify restoration complete

  Option B - Manual Cleanup:
  □ Remove/replace defaced files
  □ Remove any uploaded malware/shells
  □ Clean injected database content
  □ Remove malicious scripts
  □ Restore original content

  Post-Cleanup:
  □ Verify all malicious content removed
  □ Scan for remaining malware
  □ Check for persistence mechanisms
```

### 8.2 Patch Vulnerabilities

```
□ Step 13: Fix the entry point

  If CMS Vulnerability:
  □ Update CMS to latest version
  □ Update all plugins/themes
  □ Remove unused plugins/themes
  □ Review and harden CMS configuration

  If Credential Compromise:
  □ Enforce strong password policy
  □ Implement MFA for all admin access
  □ Review all user accounts
  □ Implement account lockout

  If Server Vulnerability:
  □ Patch operating system
  □ Update web server software
  □ Review server configuration
  □ Harden server security

  If Application Vulnerability:
  □ Fix vulnerable code
  □ Implement input validation
  □ Deploy WAF rules
```

### 8.3 Harden Environment

```
□ Step 14: Implement additional protections

  □ Enable Web Application Firewall (WAF)
  □ Implement file integrity monitoring
  □ Enable real-time malware scanning
  □ Configure security headers
  □ Implement Content Security Policy (CSP)
  □ Enable access logging and alerting
  □ Restrict file upload capabilities
  □ Implement IP-based admin restrictions
```

---

## 9. Recovery

### 9.1 Restore Service

```
□ Step 15: Bring site back online

  Pre-Launch Checklist:
  □ All malicious content removed
  □ Vulnerability patched
  □ Credentials rotated
  □ Additional security controls in place
  □ Monitoring enabled
  □ Backup verified

□ Step 16: Restore public access
  □ Remove maintenance page
  □ Restore DNS/load balancer if changed
  □ Verify site functioning correctly
  □ Test all critical functionality
  □ Clear CDN cache if applicable
```

### 9.2 Post-Recovery Monitoring

```
□ Step 17: Enhanced monitoring period

  Monitor for 2-4 weeks:
  □ File integrity monitoring alerts
  □ Unusual access patterns
  □ Admin login attempts
  □ Error log anomalies
  □ Performance issues
  □ Reinfection indicators
```

---

## 10. Communication

### 10.1 Internal Communication

| Audience | When | Content |
|----------|------|---------|
| Executive team | P1/P2 immediately | Incident summary, business impact, response status |
| IT/Web teams | Immediately | Technical details, required actions |
| Communications | Immediately | Prepare for external inquiries |
| Customer service | If customer-facing | Talking points for inquiries |
| All staff | If widely known | Brief factual update |

### 10.2 External Communication

| Audience | When | Owner |
|----------|------|-------|
| Customers | If service affected | Communications |
| Media | If newsworthy | Communications + Legal |
| Regulators | If data breach | Legal |
| Hosting provider | If assistance needed | IT |

### 10.3 Communication Templates

**Social Media (If Needed):**
```
We're aware of an issue affecting our website and are working to resolve
it. We apologize for any inconvenience. Updates to follow.
```

**Customer FAQ:**
```
Q: What happened to your website?
A: We experienced a temporary security issue that affected our website's
   appearance. The issue has been resolved and no customer data was affected.

Q: Was my data compromised?
A: [If no data breach] Our investigation confirmed that no customer data
   was accessed or compromised during this incident.
```

---

## 11. Post-Incident

### 11.1 Documentation

```
□ Step 18: Complete incident documentation

  Document:
  □ Complete timeline
  □ Attack vector and root cause
  □ Systems affected
  □ Actions taken
  □ Evidence collected
  □ Business impact
  □ Lessons learned
```

### 11.2 Post-Incident Review

```
□ Step 19: Conduct review (within 1 week)

  Review Questions:
  □ How was initial access gained?
  □ Why wasn't the vulnerability known/patched?
  □ How was defacement detected?
  □ How long was site defaced before detection?
  □ Was response timely and effective?
  □ What controls failed?
  □ What controls would have prevented this?
```

### 11.3 Improvements

```
□ Step 20: Implement improvements

  Consider:
  □ Automated vulnerability scanning
  □ File integrity monitoring
  □ Web Application Firewall
  □ Improved change detection
  □ Regular penetration testing
  □ CMS hardening
  □ Admin access restrictions
  □ Improved backup procedures
```

---

## 12. Prevention Reference

### 12.1 Common Defacement Causes

| Cause | Prevention |
|-------|------------|
| Outdated CMS | Automated patching, vulnerability scanning |
| Vulnerable plugins | Regular updates, minimal plugins, security review |
| Weak credentials | Strong passwords, MFA, account lockout |
| SQL injection | Input validation, parameterized queries, WAF |
| File upload flaws | Restrict upload types, scan uploads, isolate storage |
| Server misconfiguration | Hardening standards, regular audits |

### 12.2 Recommended Controls

| Control | Purpose |
|---------|---------|
| Web Application Firewall | Block common attacks |
| File Integrity Monitoring | Detect unauthorized changes |
| Regular backups | Enable quick restoration |
| Vulnerability scanning | Find issues before attackers |
| Access logging | Detect and investigate intrusions |
| Admin IP restrictions | Limit admin access sources |
| MFA for admin | Prevent credential-based access |
| Content Security Policy | Prevent script injection |

---

## 13. Related Documents

- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Incident Response Procedure](../../procedures/incident-response-procedure.md)
- [Malware Playbook](./malware-playbook.md)
- [Data Breach Playbook](./data-breach-playbook.md)

---

## 14. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

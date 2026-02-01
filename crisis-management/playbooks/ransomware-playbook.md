# Ransomware Incident Playbook

**Severity:** Typically Critical (P1) or High (P2)
**Last Updated:** [DATE]
**Owner:** [ROLE]

---

## 1. Overview

This playbook covers response to ransomware infections, including file encryption, ransom demands, and data theft (double extortion).

## 2. Detection Indicators

### Signs of Ransomware

- [ ] Encrypted files with unusual extensions
- [ ] Ransom notes on desktop or in folders
- [ ] Inability to access files or applications
- [ ] Unusual CPU/disk activity
- [ ] Mass file modifications in logs
- [ ] Users reporting locked files
- [ ] Security alerts for known ransomware

### Initial Assessment Questions

1. How many systems affected?
2. Is encryption still active/spreading?
3. What data may be encrypted?
4. Are backups accessible and clean?
5. Is there evidence of data exfiltration?

## 3. Severity Assessment

| Factor | Critical | High | Medium |
|--------|----------|------|--------|
| Systems Affected | >50% or critical | 10-50% | <10%, non-critical |
| Data Impact | Critical/regulated data | Sensitive data | General data |
| Business Impact | Operations halted | Significant disruption | Limited impact |
| Spreading | Actively spreading | Contained | Single system |

## 4. Immediate Actions (First 30 Minutes)

### DO

- [ ] **Isolate affected systems** - Disconnect from network (unplug cable, disable WiFi)
- [ ] **Do NOT power off** - Memory may contain encryption keys
- [ ] **Photograph ransom note** - Capture full text including addresses
- [ ] **Alert CSIRT and management**
- [ ] **Identify patient zero** - First infected system
- [ ] **Check backup status** - Are backups accessible and clean?
- [ ] **Enable enhanced logging**

### DO NOT

- [ ] Do NOT pay ransom immediately
- [ ] Do NOT communicate with attackers without legal approval
- [ ] Do NOT delete ransom notes or encrypted files
- [ ] Do NOT run antivirus scans (may destroy evidence)
- [ ] Do NOT restore from backups until source identified

## 5. Containment

### Network Containment

1. [ ] Isolate infected network segments
2. [ ] Block known malicious IPs/domains at firewall
3. [ ] Disable file sharing between systems
4. [ ] Restrict lateral movement capabilities
5. [ ] Increase network monitoring

### System Containment

1. [ ] Disable compromised accounts
2. [ ] Block execution of ransomware (if identified)
3. [ ] Preserve affected systems for forensics
4. [ ] Create forensic images before changes

### Prevent Spread

1. [ ] Identify and patch exploitation vector
2. [ ] Reset compromised credentials
3. [ ] Scan all systems for indicators of compromise
4. [ ] Isolate vulnerable systems until patched

## 6. Investigation

### Evidence Collection

- [ ] Memory dumps from infected systems
- [ ] Disk images (before any changes)
- [ ] Network logs and traffic captures
- [ ] Security tool alerts and logs
- [ ] Email logs (for phishing vector)
- [ ] Authentication logs

### Determine Scope

- [ ] Total systems encrypted
- [ ] Types of data affected
- [ ] Is data exfiltrated? (check for prior uploads)
- [ ] Initial infection vector
- [ ] Timeline of infection

### Identify Variant

- [ ] Ransomware family (from note, extension, behavior)
- [ ] Check No More Ransom (nomoreransom.org) for decryptor
- [ ] Research variant capabilities
- [ ] Identify IOCs for detection

## 7. Ransom Decision

### Factors to Consider

| Factor | Notes |
|--------|-------|
| Data criticality | Is data essential and irreplaceable? |
| Backup availability | Can we restore without paying? |
| Decryptor availability | Free decryptor available? |
| Attacker reputation | Do they actually decrypt after payment? |
| Legal implications | Sanctions, regulations |
| Insurance coverage | Does policy cover ransom? |

### Decision Authority

- [ ] Executive and legal approval required for any payment
- [ ] Document decision rationale
- [ ] Consider law enforcement consultation

### If NOT Paying

1. [ ] Proceed with recovery from backups
2. [ ] Wipe and rebuild affected systems
3. [ ] Accept data loss for unrecoverable data

### If Considering Payment (Last Resort)

1. [ ] Consult legal counsel
2. [ ] Verify attacker credibility
3. [ ] Engage professional negotiator (insurance may provide)
4. [ ] Document everything
5. [ ] Report to law enforcement
6. [ ] Plan for decryption process

## 8. Eradication

### Remove Ransomware

1. [ ] Identify all infected systems
2. [ ] Create forensic images
3. [ ] Wipe and rebuild from clean images OR
4. [ ] Remove all malware artifacts if keeping system
5. [ ] Reset all potentially compromised credentials
6. [ ] Patch exploitation vector

### Verify Clean

- [ ] Scan all systems with updated signatures
- [ ] Verify no persistence mechanisms
- [ ] Check for backdoors
- [ ] Monitor for reinfection indicators

## 9. Recovery

### Recovery Priorities

| Priority | Systems |
|----------|---------|
| 1 | [Critical business systems] |
| 2 | [Important systems] |
| 3 | [Standard systems] |
| 4 | [Non-essential] |

### Recovery Steps

1. [ ] Verify backup integrity
2. [ ] Restore systems from clean backups
3. [ ] Apply all patches before reconnecting
4. [ ] Harden configurations
5. [ ] Test functionality
6. [ ] Reconnect to network gradually
7. [ ] Monitor closely for 48-72 hours

### If Using Decryptor

1. [ ] Test on non-critical data first
2. [ ] Verify decrypted files are not corrupted
3. [ ] Keep encrypted copies until verified
4. [ ] Still rebuild systems after decryption

## 10. Communication

### Internal Communication

| Audience | When | Content |
|----------|------|---------|
| Executive team | Immediately | Incident summary, impact, actions |
| IT staff | Immediately | Technical details, response tasks |
| All employees | When stable | What happened, what to do, status |
| Board | Within 24-48h | Impact, response, root cause |

### External Communication

| Audience | When | Content |
|----------|------|---------|
| Legal counsel | Immediately | Full details for advice |
| Law enforcement | ASAP (FBI, CISA) | Report incident |
| Cyber insurance | Per policy | Claim notification |
| Regulators | Per requirements | Breach notification if data exposed |
| Customers | If data affected | Per notification requirements |
| Media | If needed | Prepared statement only |

## 11. Post-Incident

### Documentation

- [ ] Complete incident report
- [ ] Timeline of events
- [ ] Actions taken
- [ ] Costs incurred
- [ ] Data affected

### Lessons Learned

- [ ] How did they get in?
- [ ] Why wasn't it detected sooner?
- [ ] Were backups adequate?
- [ ] What improvements needed?

### Improvements

| Finding | Action | Owner | Due |
|---------|--------|-------|-----|
| | | | |

## 12. Prevention Checklist

Post-incident, verify:

- [ ] Immutable/offline backups implemented
- [ ] Email security enhanced
- [ ] Endpoint protection updated
- [ ] Network segmentation improved
- [ ] Privileged access restricted
- [ ] User awareness training updated
- [ ] Vulnerability management improved
- [ ] Incident response capabilities verified

---

## Quick Reference Card

```
RANSOMWARE RESPONSE - FIRST 30 MINUTES

1. ISOLATE - Disconnect systems from network
2. PRESERVE - Don't power off, don't delete
3. NOTIFY - Alert CSIRT, management
4. PHOTOGRAPH - Capture ransom notes
5. CHECK BACKUPS - Verify clean and accessible
6. DON'T PAY YET - Investigate first

Emergency Contact: [PHONE NUMBER]
Bridge Call: [CONFERENCE URL]
```

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

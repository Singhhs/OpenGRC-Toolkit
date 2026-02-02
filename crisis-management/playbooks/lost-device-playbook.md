# Lost or Stolen Device Playbook

**Severity:** Typically Medium (P3) to High (P2)
**Last Updated:** [DATE]
**Owner:** [ROLE]

---

## 1. Overview

This playbook covers response to lost or stolen devices including laptops, smartphones, tablets, and removable storage media containing company data.

## 2. Device Categories

| Category | Examples | Risk Level |
|----------|----------|------------|
| **High Risk** | Laptops with sensitive data, unencrypted devices | High |
| **Medium Risk** | Encrypted laptops, managed smartphones | Medium |
| **Low Risk** | Encrypted devices with remote wipe, no sensitive data | Low |

## 3. Detection/Reporting

### User Should Report When

- Device cannot be located
- Device may have been stolen
- Device left in unsecured location
- Unauthorized person may have accessed device

### Report To

- IT Help Desk: [PHONE/EMAIL]
- After Hours: [EMERGENCY NUMBER]
- Security Team: [EMAIL]

### Information to Provide

- Device type and model
- Asset tag or serial number
- When device was last seen
- Where device was lost
- What data was on device
- Was device encrypted?
- Was device password protected?
- Circumstances of loss/theft

## 4. Severity Assessment

| Factor | High | Medium | Low |
|--------|------|--------|-----|
| **Encryption** | Unencrypted | Unknown | Encrypted |
| **Data on Device** | Sensitive/Regulated | Internal data | No sensitive data |
| **Authentication** | No password | Weak password | Strong password + MFA |
| **Remote Wipe** | Not possible | Unknown status | Available and confirmed |
| **Circumstances** | Targeted theft | Unknown | Misplaced |

## 5. Immediate Actions (First 30 Minutes)

### For User

1. [ ] **Report immediately** to IT/Security
2. [ ] **Do NOT delay** hoping device will turn up
3. [ ] Provide all details about device and circumstances
4. [ ] **Change passwords** for accounts accessed on device:
   - [ ] Email
   - [ ] VPN
   - [ ] Business applications
   - [ ] Personal accounts (if used on device)

### For IT/Security

1. [ ] **Log incident** and gather details
2. [ ] **Locate device** if MDM/tracking available
3. [ ] **Remote lock** device immediately
4. [ ] **Remote wipe** if appropriate (see decision tree)
5. [ ] **Disable accounts** if high risk
6. [ ] **Revoke access tokens** and certificates
7. [ ] **Force password reset** for affected accounts

---

## 6. Response by Device Type

### Laptop/Computer

#### Encrypted Laptop with MDM

1. [ ] Attempt to locate via MDM
2. [ ] Remote lock device
3. [ ] Assess data risk
4. [ ] Remote wipe if:
   - Device likely stolen
   - Contains sensitive data
   - Recovery unlikely within 24 hours
5. [ ] Force password change
6. [ ] Monitor for suspicious activity

#### Unencrypted Laptop

1. [ ] Treat as potential data breach
2. [ ] Attempt remote lock/wipe if possible
3. [ ] Inventory data on device
4. [ ] Assess sensitive data exposure
5. [ ] Consider breach notification requirements
6. [ ] Force password changes for all accounts
7. [ ] Revoke VPN and remote access
8. [ ] Monitor for unauthorized access

---

### Smartphone/Tablet

#### Managed Device (MDM Enrolled)

1. [ ] Locate device via MDM
2. [ ] Remote lock immediately
3. [ ] Assess location and circumstances:
   - If recoverable location: Allow 2-4 hours before wipe
   - If unrecoverable/stolen: Wipe immediately
4. [ ] Remote wipe:
   - Company device: Full wipe
   - BYOD: Work container wipe only
5. [ ] Revoke email/app access
6. [ ] Remove from corporate systems

#### Unmanaged Device

1. [ ] Disable account access:
   - [ ] Email
   - [ ] Cloud services
   - [ ] VPN
2. [ ] Force password reset
3. [ ] Revoke OAuth tokens
4. [ ] Instruct user to:
   - Use Apple Find My / Google Find My Device
   - Enable lost mode
   - Remote wipe if possible
5. [ ] Monitor for suspicious activity

---

### Removable Media (USB, External Drive)

1. [ ] Determine what data was stored
2. [ ] Was media encrypted?
3. [ ] Assess data sensitivity
4. [ ] If unencrypted sensitive data:
   - Treat as data breach
   - Follow data breach playbook
5. [ ] Document for incident report

---

## 7. Remote Wipe Decision

```
                    ┌─────────────────┐
                    │  Device Lost    │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │  Can Locate?    │
                    └────────┬────────┘
                      Yes    │    No
              ┌──────────────┴─────────────┐
              │                            │
     ┌────────▼────────┐          ┌───────▼────────┐
     │ Safe Location?  │          │ Wipe Device    │
     └────────┬────────┘          └────────────────┘
       Yes    │    No
    ┌─────────┴─────────┐
    │                   │
┌───▼────┐     ┌───────▼───────┐
│ Wait   │     │ Wipe Device   │
│ 2-4 hrs│     └───────────────┘
└───┬────┘
    │ Not Recovered
    ▼
┌──────────┐
│  Wipe    │
└──────────┘
```

### Wipe Immediately If

- Device confirmed stolen
- Located in suspicious location
- Contains highly sensitive data
- Cannot be recovered within 4 hours
- Circumstances indicate targeted theft

### Wait Before Wipe If

- Device in safe location (office, home)
- Low data sensitivity
- User actively attempting recovery
- No indicators of theft

---

## 8. Account Security Actions

| Account Type | Action | Timeline |
|--------------|--------|----------|
| Email | Disable mobile access, force re-auth | Immediate |
| VPN | Revoke certificate/access | Immediate |
| Cloud services | Force sign-out, reset password | Immediate |
| Business apps | Revoke tokens, disable access | Within 1 hour |
| Admin accounts | Emergency password change | Immediate |

---

## 9. Communication

### Internal Notification

| Audience | When | Content |
|----------|------|---------|
| IT Security | Immediately | Full incident details |
| User's manager | Within 1 hour | Summary, actions taken |
| HR | If policy violation | Circumstances |
| Legal | If data breach potential | Assessment |

### User Communication

```
Subject: Lost Device - Actions Required

Your lost device has been reported and we have taken
the following security actions:

- Device remotely locked/wiped
- Account passwords require reset
- [Additional actions]

Actions you need to take:
1. Reset password for [ACCOUNT] at [URL]
2. Reset password for [ACCOUNT] at [URL]
3. Report any suspicious activity
4. Contact IT to arrange replacement device

If you recover the device, DO NOT attempt to use it.
Contact IT immediately.
```

---

## 10. Data Assessment

### Determine Data on Device

| Data Type | Location | Sensitivity |
|-----------|----------|-------------|
| Email (cached) | Email app | [Level] |
| Files (local) | Downloads, Desktop | [Level] |
| Browser data | Saved passwords, history | [Level] |
| Application data | Local databases | [Level] |
| Credentials | Cached tokens | [Level] |

### If Sensitive Data Present

1. [ ] Document data types and volumes
2. [ ] Assess if encryption was active
3. [ ] Determine if data breach threshold met
4. [ ] If breach, follow [Data Breach Playbook](./data-breach-playbook.md)

---

## 11. Police Report

### When to File

- Device stolen (not misplaced)
- High value device
- Sensitive data unencrypted
- Insurance claim needed
- Pattern of thefts

### Information for Report

- Device make/model
- Serial number
- IMEI (for phones)
- Asset tag
- Date/time/location of theft
- Description of circumstances
- Value of device
- Case number (record this)

---

## 12. Recovery

### If Device is Recovered

**Before Return to Service:**

1. [ ] Do NOT power on (preserve evidence if theft)
2. [ ] IT inspects device
3. [ ] Check for tampering
4. [ ] Run security scans
5. [ ] Verify encryption intact
6. [ ] If wiped: Re-image from scratch
7. [ ] If concerns: Forensic analysis first

---

## 13. Replacement

1. [ ] Request replacement via [PROCESS]
2. [ ] Configure new device with standard image
3. [ ] Restore data from backup (if available)
4. [ ] Enroll in MDM
5. [ ] Update asset inventory
6. [ ] User acknowledgment of policies

---

## 14. Post-Incident

### Documentation

- [ ] Complete incident report
- [ ] Document timeline
- [ ] Record all actions taken
- [ ] Note data potentially exposed
- [ ] Archive for future reference

### Review

- [ ] Was encryption enabled?
- [ ] Was MDM functioning?
- [ ] Could we have responded faster?
- [ ] Any policy improvements needed?

---

## 15. Prevention Reminders

After incident, remind users:

- [ ] Enable full disk encryption
- [ ] Use strong password/PIN
- [ ] Never leave devices unattended
- [ ] Use privacy screens in public
- [ ] Don't store sensitive data locally
- [ ] Keep devices in carry-on luggage
- [ ] Report losses immediately

---

## 16. Quick Reference

```
LOST DEVICE - IMMEDIATE STEPS

1. REPORT to IT: [PHONE]
2. LOCATE via MDM (IT will do this)
3. LOCK device remotely
4. CHANGE passwords immediately
5. WIPE if not recoverable
6. ASSESS data exposure
7. FILE police report if stolen

User Password Reset Links:
- Email: [URL]
- VPN: [URL]
- [System]: [URL]
```

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

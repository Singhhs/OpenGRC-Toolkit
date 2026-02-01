# User Offboarding Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Operations Manager] |
| **Classification** | Internal |

---

## 1. Purpose

This procedure ensures timely and complete revocation of access and return of assets when employees, contractors, or third parties leave [ORGANIZATION NAME].

## 2. Scope

Applies to:
- Voluntary resignations
- Involuntary terminations
- Contract completions
- Internal transfers (partial offboarding)
- Extended leaves of absence

## 3. Termination Types

| Type | Access Revocation | Asset Return |
|------|-------------------|--------------|
| **Immediate/Involuntary** | Same day, before notification | Same day |
| **Standard Resignation** | Last day of employment | Last day |
| **Contractor End** | Contract end date | Contract end date |
| **Internal Transfer** | Transfer date (old access) | N/A |
| **Extended Leave** | Leave start date (disable) | N/A or as required |

## 4. Procedure

### Step 1: HR Notification

**Responsibility:** HR Department

**Timeline:** As soon as termination is known

1. [ ] Send termination notification to:
   - [ ] IT Operations (primary)
   - [ ] IT Security
   - [ ] Direct manager
   - [ ] Physical security
   - [ ] Facilities
   - [ ] [Other departments as needed]

2. [ ] Include in notification:
   - Employee name and ID
   - Department and manager
   - Last working day/time
   - Termination type
   - Access revocation deadline
   - Special considerations

**Template:** Use [Termination Notification Template](../templates/termination-notification.md)

---

### Step 2: Manager Preparation

**Responsibility:** Direct Manager

**Timeline:** Upon receiving notification

1. [ ] Schedule exit interview (if appropriate)
2. [ ] Identify knowledge transfer needs
3. [ ] Prepare list of projects/responsibilities to transition
4. [ ] Identify data/files that need to be preserved
5. [ ] Coordinate return of assets
6. [ ] For immediate terminations:
   - [ ] Secure workspace
   - [ ] Arrange for escort if required

---

### Step 3: Access Revocation

**Responsibility:** IT Operations

**Timeline:** As specified by termination type

#### 3.1 Immediate Actions (within specified deadline)

| System/Access | Action | Verified |
|---------------|--------|----------|
| Active Directory / LDAP | Disable account | [ ] |
| Email account | Disable (do not delete) | [ ] |
| VPN access | Revoke | [ ] |
| Remote access tokens | Revoke | [ ] |
| Building access cards | Deactivate | [ ] |
| MFA tokens/apps | Remove | [ ] |

#### 3.2 Application Access (within 24 hours)

| Application | Action | Verified |
|-------------|--------|----------|
| [Application 1] | Disable/remove | [ ] |
| [Application 2] | Disable/remove | [ ] |
| [Cloud services] | Disable/remove | [ ] |
| [Privileged systems] | Disable/remove | [ ] |

#### 3.3 Shared Access (within 24 hours)

- [ ] Remove from distribution lists
- [ ] Remove from shared mailboxes
- [ ] Remove from shared calendars
- [ ] Remove from collaboration tools (Teams, Slack)
- [ ] Remove from file shares
- [ ] Transfer ownership of shared files/folders

---

### Step 4: Asset Return

**Responsibility:** Manager and IT Operations

**Timeline:** Last day of employment

#### 4.1 IT Assets Checklist

| Asset | Serial/Asset # | Returned | Condition |
|-------|----------------|----------|-----------|
| Laptop | | [ ] | |
| Mobile phone | | [ ] | |
| Tablet | | [ ] | |
| Monitors | | [ ] | |
| Keyboard/mouse | | [ ] | |
| Headset | | [ ] | |
| USB drives | | [ ] | |
| External storage | | [ ] | |
| Security tokens | | [ ] | |
| Smart cards | | [ ] | |

#### 4.2 Non-IT Assets

| Asset | Returned | Notes |
|-------|----------|-------|
| Building access cards | [ ] | |
| Keys | [ ] | |
| Parking pass | [ ] | |
| Company credit card | [ ] | |
| ID badge | [ ] | |
| Company documents | [ ] | |

---

### Step 5: Data Handling

**Responsibility:** IT Operations with Manager guidance

**Timeline:** Last day to 30 days post-departure

1. [ ] Backup user data per retention requirements
2. [ ] Preserve mailbox (if required for legal/business reasons)
3. [ ] Transfer ownership of files to manager
4. [ ] Archive shared resources owned by user
5. [ ] Preserve data subject to legal hold
6. [ ] Delete data per retention schedule (after retention period)

**Email Handling:**
- [ ] Set up auto-reply/out of office
- [ ] Forward to manager or alternate (if approved)
- [ ] Export mailbox for archival (if required)
- [ ] Delete mailbox after retention period

---

### Step 6: Device Sanitization

**Responsibility:** IT Operations

**Timeline:** After data backup

1. [ ] Verify data backup complete
2. [ ] Wipe device using approved method
3. [ ] Factory reset mobile devices
4. [ ] Remove from MDM
5. [ ] Document sanitization
6. [ ] Prepare for redeployment or disposal

---

### Step 7: Account Cleanup

**Responsibility:** IT Operations

**Timeline:** 30-90 days post-departure

1. [ ] Review that all access is revoked
2. [ ] Delete accounts per schedule:
   - [ ] AD/Directory account (30 days)
   - [ ] Email account (90 days or per retention)
   - [ ] Application accounts (30 days)
3. [ ] Archive final state
4. [ ] Update asset inventory
5. [ ] Update license counts

---

### Step 8: Documentation

**Responsibility:** IT Operations

**Timeline:** Within 1 week of departure

Complete offboarding record including:
- [ ] All access revocation confirmations
- [ ] Asset return documentation
- [ ] Data handling documentation
- [ ] Any issues or exceptions
- [ ] Manager sign-off

---

## 5. Special Scenarios

### 5.1 Immediate/Involuntary Termination

- Access revoked before or during termination meeting
- Escort arranged if required
- Assets collected same day
- Manager or security secures workspace

### 5.2 Extended Leave (>30 days)

- Disable (don't delete) accounts
- Suspend access, maintain data
- Document expected return date
- Re-enable on return with verification

### 5.3 Internal Transfer

- Remove old department access
- Retain appropriate general access
- Add new department access
- Transfer asset assignment if needed

### 5.4 Contractor Termination

- Sponsor notifies IT Security
- All access revoked on contract end date
- Return all company equipment
- NDA obligations continue

### 5.5 Death of Employee

- Handle with sensitivity
- Disable access immediately
- Work with HR and legal
- Preserve data as required
- Return personal effects per HR guidance

---

## 6. Escalation

Escalate to [IT Security Manager/HR] when:
- Delay in access revocation
- Assets not returned
- Concerns about data theft
- Unusual activity detected
- Any security concerns

---

## 7. Metrics

| Metric | Target |
|--------|--------|
| Access disabled within SLA | 100% |
| Assets returned on time | 95% |
| Offboarding complete within 5 days | 100% |

---

## 8. Related Documents

- [Access Control Policy](../policies/access-control-policy.md)
- [User Access Request Procedure](./user-access-request-procedure.md)
- [Data Disposal Procedure](./data-disposal-procedure.md)
- [Offboarding Checklist](../checklists/offboarding-checklist.md)

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

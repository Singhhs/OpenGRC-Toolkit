# Access Review Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Classification** | Internal |

---

## 1. Purpose

This procedure defines the process for conducting periodic reviews of user access rights to ensure access remains appropriate and follows the principle of least privilege.

## 2. Scope

Applies to:
- All user accounts on business-critical systems
- Privileged and administrative accounts
- Service accounts
- Third-party and contractor access

## 3. Review Schedule

| Access Type | Frequency | Responsible |
|-------------|-----------|-------------|
| Standard User Access | Annually | Line Manager + System Owner |
| Privileged/Admin Access | Quarterly | IT Security + System Owner |
| Service Accounts | Semi-annually | IT Operations + Application Owner |
| Third-Party Access | Annually or contract renewal | Vendor Manager + IT Security |
| Dormant Account Check | Monthly | IT Operations |

## 4. Procedure

### Step 1: Prepare Access Report

**Responsibility:** IT Security / IT Operations

**Timeline:** 1 week before review period

1. [ ] Generate access report from identity management system
2. [ ] Include for each user:
   - Username and full name
   - Department and manager
   - Systems/applications with access
   - Access level/permissions
   - Last login date
   - Account status (active, disabled, locked)
3. [ ] Identify accounts for special attention:
   - Dormant accounts (no login > 90 days)
   - Accounts with elevated privileges
   - Accounts belonging to terminated employees
   - Service accounts
   - Shared accounts
4. [ ] Distribute reports to reviewers

---

### Step 2: Manager Review

**Responsibility:** Line Managers

**Timeline:** 2 weeks from report distribution

For each employee in their team:

1. [ ] Verify employee still requires access
2. [ ] Review each system/application:
   - [ ] Is this access still needed for job function?
   - [ ] Is the access level appropriate?
   - [ ] Has role changed requiring access modification?
3. [ ] Make determination for each access:

| Decision | Action |
|----------|--------|
| **Retain** | Access remains as-is |
| **Modify** | Access level needs adjustment |
| **Remove** | Access no longer needed |
| **Review Further** | Escalate for additional review |

4. [ ] Document decisions and justifications
5. [ ] Submit completed review to IT Security

---

### Step 3: System Owner Review

**Responsibility:** System/Data Owners

**Timeline:** 2 weeks from manager review completion

1. [ ] Review manager recommendations
2. [ ] Validate access decisions against:
   - Data classification requirements
   - Segregation of duties
   - Regulatory requirements
3. [ ] Identify any conflicts or concerns
4. [ ] Approve access decisions
5. [ ] Escalate issues to IT Security

---

### Step 4: IT Security Review

**Responsibility:** IT Security Team

**Timeline:** 1 week from system owner review

1. [ ] Review all access decisions
2. [ ] Verify compliance with policies
3. [ ] Check for:
   - [ ] Segregation of duties violations
   - [ ] Excessive permissions
   - [ ] Orphaned accounts
   - [ ] Non-compliant access patterns
4. [ ] Approve review findings
5. [ ] Create remediation tasks for access changes

---

### Step 5: Implement Access Changes

**Responsibility:** IT Operations

**Timeline:** Within 2 weeks of approval

**For Access Removals:**
1. [ ] Disable/remove access from identified systems
2. [ ] Document changes in ticketing system
3. [ ] Notify user and manager of removal
4. [ ] Verify access successfully removed

**For Access Modifications:**
1. [ ] Modify permissions as directed
2. [ ] Document changes
3. [ ] Notify user of changes
4. [ ] Verify new access is correct

---

### Step 6: Document and Close

**Responsibility:** IT Security

**Timeline:** 1 week after implementation

1. [ ] Verify all changes implemented
2. [ ] Document review completion:
   - Total accounts reviewed
   - Access retained
   - Access removed
   - Access modified
   - Issues identified
3. [ ] Calculate metrics
4. [ ] Report to management
5. [ ] Archive review documentation
6. [ ] Schedule next review

---

## 5. Privileged Access Review

Additional steps for privileged accounts:

### Step 5A: Privileged Access Validation

1. [ ] Verify business justification for privileged access
2. [ ] Confirm approval from IT Security
3. [ ] Review privileged access activity logs
4. [ ] Verify separation from standard accounts
5. [ ] Confirm MFA enabled
6. [ ] Validate privileged access is named (not shared)

---

## 6. Service Account Review

Additional steps for service accounts:

### Step 6A: Service Account Validation

1. [ ] Verify service account is still needed
2. [ ] Confirm application/process using account
3. [ ] Validate account owner
4. [ ] Check password age and rotation
5. [ ] Review permissions (least privilege)
6. [ ] Verify account is not used interactively

---

## 7. Dormant Account Handling

| Days Inactive | Action |
|---------------|--------|
| 60 days | Notify user and manager |
| 90 days | Disable account |
| 120 days | Review for deletion |
| 180 days | Delete account (unless exception) |

**Exceptions:**
- Leave of absence (documented)
- Seasonal employees (documented)
- Approved exception with review date

---

## 8. Escalation

Escalate to [CISO/IT Director] when:
- Manager does not respond within timeframe
- Disagreement on access decisions
- Policy violations discovered
- Segregation of duties conflicts
- Evidence of inappropriate access

---

## 9. Metrics and Reporting

### Key Metrics

| Metric | Target |
|--------|--------|
| Reviews completed on time | 100% |
| Inappropriate access removed | Track number |
| Dormant accounts addressed | 100% |
| Average review completion time | < 4 weeks |

### Reporting

- Monthly status to IT Security management
- Quarterly summary to IT leadership
- Annual summary to executive management

---

## 10. Documentation Requirements

Retain for each review cycle:
- Access reports (input)
- Manager review decisions
- System owner approvals
- Changes implemented
- Exception documentation
- Review summary

**Retention:** [7 years] or per retention policy

---

## 11. Related Documents

- [Access Control Policy](../policies/access-control-policy.md)
- [User Access Request Procedure](./user-access-request-procedure.md)
- [User Offboarding Procedure](./user-offboarding-procedure.md)

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

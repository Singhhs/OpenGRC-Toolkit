# User Access Request Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Operations Manager] |
| **Classification** | Internal |

---

## 1. Purpose

This procedure defines the process for requesting, approving, and provisioning user access to [ORGANIZATION NAME] systems and applications.

## 2. Scope

Applies to:
- New employee access provisioning
- Access changes for existing employees
- Contractor and third-party access
- Temporary and project-based access

## 3. Access Request Types

| Type | Description | Approval Required |
|------|-------------|-------------------|
| **New User** | Initial access for new employee | Manager |
| **Role Change** | Access modification due to job change | New Manager + Old Manager |
| **Additional Access** | Access beyond standard role | Manager + System Owner |
| **Privileged Access** | Administrative or elevated access | Manager + System Owner + IT Security |
| **Temporary Access** | Time-limited access | Manager + IT Security |
| **Third Party** | Vendor or contractor access | Sponsor + System Owner + IT Security |

## 4. Procedure

### Step 1: Submit Access Request

**Requestor/Manager:**

1. [ ] Log into [IT Service Portal / Ticketing System]
2. [ ] Select "Access Request" from service catalog
3. [ ] Complete required fields:

| Field | Description |
|-------|-------------|
| User Name | Full name of person needing access |
| Employee ID | If applicable |
| Department | User's department |
| Start Date | When access is needed |
| End Date | For temporary access only |
| Manager | Approving manager |
| Systems/Applications | List specific systems needed |
| Access Level | Read, write, admin, etc. |
| Business Justification | Why access is needed |

4. [ ] Attach supporting documentation if required
5. [ ] Submit request

---

### Step 2: Manager Approval

**Line Manager:**

1. [ ] Review access request notification
2. [ ] Verify:
   - [ ] User is a valid employee/contractor
   - [ ] Access is appropriate for role
   - [ ] Business justification is valid
3. [ ] **Approve** or **Reject** with comments
4. [ ] For privileged access, route to next approver

**SLA:** 2 business days

---

### Step 3: System Owner Approval (if required)

**System/Data Owner:**

Required for:
- Access to sensitive systems
- Access beyond standard role permissions
- Cross-departmental access

1. [ ] Review access request
2. [ ] Verify:
   - [ ] Need-to-know is established
   - [ ] Access level is appropriate
   - [ ] No segregation of duties conflicts
3. [ ] **Approve** or **Reject** with comments

**SLA:** 2 business days

---

### Step 4: Security Review (if required)

**IT Security:**

Required for:
- Privileged/administrative access
- Third-party access
- Exceptions to standard access

1. [ ] Review request and approvals
2. [ ] Verify:
   - [ ] Complies with Access Control Policy
   - [ ] No security concerns
   - [ ] Background check complete (if required)
   - [ ] NDA signed (for third parties)
3. [ ] **Approve** or **Reject** with comments
4. [ ] Document any conditions or restrictions

**SLA:** 2 business days

---

### Step 5: Access Provisioning

**IT Operations:**

1. [ ] Receive approved access request
2. [ ] Create/modify user account:

   **For New Users:**
   - [ ] Create user account per naming convention
   - [ ] Assign to appropriate groups/roles
   - [ ] Set temporary password
   - [ ] Enable MFA enrollment
   - [ ] Configure email and standard apps

   **For Existing Users:**
   - [ ] Add/remove group memberships
   - [ ] Modify application permissions
   - [ ] Update access control lists

3. [ ] Document changes in access management system
4. [ ] Generate temporary credentials (if new account)

**SLA:**
- Standard access: 2 business days
- Urgent (approved): 4 hours

---

### Step 6: Communicate Access

**IT Operations:**

1. [ ] Notify user of account creation/modification
2. [ ] Provide:
   - [ ] Username
   - [ ] Temporary password (via secure channel)
   - [ ] MFA setup instructions
   - [ ] Link to acceptable use policy
3. [ ] Instruct user to change password on first login

**Secure communication methods:**
- In-person delivery
- Encrypted email
- Separate channels for username and password

---

### Step 7: User Acknowledgment

**User:**

1. [ ] Log into account
2. [ ] Change temporary password
3. [ ] Complete MFA enrollment
4. [ ] Acknowledge policies (if prompted)
5. [ ] Report any issues to Help Desk

---

### Step 8: Request Closure

**IT Operations:**

1. [ ] Confirm user has successfully logged in
2. [ ] Document access granted in:
   - [ ] Ticketing system
   - [ ] Access management database
   - [ ] User's access record
3. [ ] Close request ticket

---

## 5. Special Scenarios

### 5.1 Emergency Access

For urgent business needs:

1. [ ] Manager contacts IT Security directly
2. [ ] Verbal approval with email confirmation within 24 hours
3. [ ] Access granted with monitoring
4. [ ] Formal request submitted within 1 business day
5. [ ] Access reviewed within 1 week

### 5.2 Contractor/Third-Party Access

Additional requirements:

1. [ ] NDA signed and on file
2. [ ] Sponsor identified (internal employee)
3. [ ] Security assessment completed (for vendors)
4. [ ] Defined end date required
5. [ ] Background check (if accessing sensitive data)

### 5.3 Temporary Access

1. [ ] End date must be specified
2. [ ] Automatic deactivation at end date
3. [ ] Extension requires new request
4. [ ] Maximum duration: [90 days, then renewal]

## 6. Access Levels

### Standard Access Levels

| Level | Permissions | Typical Use |
|-------|-------------|-------------|
| **Read** | View only | Reporting, reference |
| **Read/Write** | View and modify | Standard user |
| **Full Control** | View, modify, delete, manage | Power user |
| **Admin** | All permissions + user management | System administrator |

### Role-Based Access

| Role | Standard Access |
|------|-----------------|
| [Role 1] | [Systems and access level] |
| [Role 2] | [Systems and access level] |
| [Role 3] | [Systems and access level] |

<!-- CUSTOMIZE: Define standard roles for your organization -->

## 7. Documentation Requirements

All access requests must retain:
- Original request with justification
- All approvals with timestamps
- Changes made
- Evidence of user acknowledgment

Retention: [7 years or per policy]

## 8. Metrics

| Metric | Target |
|--------|--------|
| Standard access provisioning time | < 2 business days |
| Privileged access provisioning time | < 5 business days |
| Request rejection rate | Tracked monthly |
| Access review completion | 100% annually |

## 9. Related Documents

- [Access Control Policy](../policies/access-control-policy.md)
- [Access Review Procedure](./access-review-procedure.md)
- [User Offboarding Procedure](./user-offboarding-procedure.md)
- [Access Request Form](../templates/access-request-form.md)

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

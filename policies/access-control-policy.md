# Access Control Policy

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Next Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Approved By** | [ROLE - e.g., CISO] |
| **Classification** | Internal |

---

## 1. Purpose

This policy establishes the requirements for controlling access to [ORGANIZATION NAME]'s information systems, applications, and data to ensure that access is granted based on business need and least privilege principles.

## 2. Scope

This policy applies to:
- All information systems and applications
- All users including employees, contractors, and third parties
- All types of access: physical, logical, and remote

## 3. Policy Statements

### 3.1 Access Control Principles

All access to information systems shall be based on:

1. **Need-to-Know**: Access granted only for information required for job function
2. **Least Privilege**: Minimum access necessary to perform duties
3. **Segregation of Duties**: Critical functions split between multiple people
4. **Defense in Depth**: Multiple layers of access controls

### 3.2 User Access Management

#### 3.2.1 User Registration

- All access requests must be formally documented and approved
- Users must be uniquely identified (no shared accounts for individuals)
- Access requests require approval from:
  - Line manager (for standard access)
  - Data/System owner (for privileged or sensitive access)
  - [IT Security / CISO] (for administrative access)

#### 3.2.2 Access Provisioning

| Access Type | Approval Required | Review Frequency |
|-------------|------------------|------------------|
| Standard User | Line Manager | Annual |
| Privileged Access | System Owner + IT Security | Quarterly |
| Administrative | CISO/IT Director | Quarterly |
| Third Party | Sponsor + IT Security | Per contract/Annual |
| Temporary | Line Manager + IT Security | At expiry |

#### 3.2.3 Access Modification

- Access changes require the same approval as new access
- Role changes must trigger access review within [5] business days
- Users must not accumulate unnecessary permissions

#### 3.2.4 Access Removal

Access must be revoked:
- Immediately upon termination (within [4] hours)
- Upon role change (unnecessary access within [5] business days)
- Upon extended leave (>30 days): disable account
- At contract end for third parties

### 3.3 Authentication Requirements

#### 3.3.1 Password Standards

See [Password Policy](./password-policy.md) for detailed requirements.

| Requirement | Standard |
|-------------|----------|
| Minimum Length | [12] characters |
| Complexity | Mix of upper, lower, numbers, symbols |
| Maximum Age | [90] days |
| History | Last [12] passwords |
| Lockout | After [5] failed attempts |

#### 3.3.2 Multi-Factor Authentication (MFA)

MFA is required for:
- All remote access
- Privileged/administrative accounts
- Access to sensitive/confidential systems
- Cloud service administration
- Email access from untrusted devices

<!-- CUSTOMIZE: Specify which systems require MFA -->

### 3.4 Privileged Access Management

#### 3.4.1 Privileged Account Controls

- Privileged accounts must be separate from standard accounts
- Named privileged accounts (no generic admin accounts)
- All privileged access must be logged and monitored
- Privileged access sessions should be time-limited
- Emergency access procedures must be documented

#### 3.4.2 Administrative Access

- Administrative access granted only when necessary
- Requires additional approval and justification
- Subject to enhanced monitoring
- Reviewed quarterly

### 3.5 Access Reviews

| Review Type | Frequency | Responsibility |
|-------------|-----------|----------------|
| User Access Review | Annual | System Owner + Line Manager |
| Privileged Access Review | Quarterly | IT Security |
| Service Account Review | Semi-annual | IT Operations |
| Third Party Access | Annual or contract renewal | Vendor Manager + IT Security |
| Dormant Account Review | Monthly | IT Operations |

### 3.6 Remote Access

- All remote access must use approved, encrypted connections (VPN)
- Remote access requires MFA
- Split tunneling is [prohibited/restricted]
- Remote sessions must time out after [15] minutes of inactivity
- See [Remote Work Policy](./remote-work-policy.md)

### 3.7 Third-Party Access

- Requires formal agreement and security assessment
- Sponsored by internal employee
- Limited to minimum necessary access
- Logged and monitored
- Regular review of continued need
- See [Supplier Security Policy](./supplier-security-policy.md)

## 4. Roles and Responsibilities

### 4.1 IT Security Team
- Maintain access control standards
- Conduct access reviews and audits
- Manage privileged access requests
- Monitor for access violations

### 4.2 IT Operations
- Implement access control mechanisms
- Process access requests
- Remove access upon notification
- Maintain access logs

### 4.3 System/Data Owners
- Approve access to their systems/data
- Define access requirements
- Participate in access reviews
- Report access concerns

### 4.4 Line Managers
- Request access for team members
- Review and approve standard access
- Notify IT of terminations and role changes
- Participate in access reviews

### 4.5 Users
- Use access only for authorized purposes
- Protect authentication credentials
- Report suspicious access or lost credentials
- Not share accounts or credentials

## 5. Compliance

### 5.1 Monitoring
Access control compliance is monitored through:
- Automated access logging
- Regular access reviews
- Security audits
- Incident investigations

### 5.2 Violations
Violations may result in:
- Immediate access revocation
- Disciplinary action
- Security incident investigation

## 6. Exceptions

Exceptions require:
- Written business justification
- Risk assessment
- Compensating controls
- Approval from [CISO]
- Defined expiry date

## 7. Related Documents

- [Password Policy](./password-policy.md)
- [Remote Work Policy](./remote-work-policy.md)
- [Supplier Security Policy](./supplier-security-policy.md)
- [User Access Request Procedure](../procedures/user-access-request-procedure.md)
- [Access Review Procedure](../procedures/access-review-procedure.md)

## 8. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

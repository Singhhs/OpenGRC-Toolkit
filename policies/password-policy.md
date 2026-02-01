# Password Policy

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

This policy establishes requirements for creating, managing, and protecting passwords and other authentication credentials at [ORGANIZATION NAME].

## 2. Scope

This policy applies to:
- All user accounts on [ORGANIZATION NAME] systems
- All employees, contractors, and third parties
- All password-protected resources

## 3. Password Requirements

### 3.1 Standard User Accounts

| Requirement | Standard |
|-------------|----------|
| Minimum Length | 12 characters |
| Complexity | At least 3 of: uppercase, lowercase, numbers, symbols |
| Maximum Age | 90 days |
| Minimum Age | 1 day (prevent rapid cycling) |
| History | Cannot reuse last 12 passwords |
| Lockout Threshold | 5 failed attempts |
| Lockout Duration | 30 minutes or until admin unlock |

### 3.2 Privileged/Administrative Accounts

| Requirement | Standard |
|-------------|----------|
| Minimum Length | 16 characters |
| Complexity | All 4 types: uppercase, lowercase, numbers, symbols |
| Maximum Age | 60 days |
| History | Cannot reuse last 24 passwords |
| Lockout Threshold | 3 failed attempts |
| Lockout Duration | Until admin unlock |
| MFA | Required |

### 3.3 Service Accounts

| Requirement | Standard |
|-------------|----------|
| Minimum Length | 24 characters (preferably random) |
| Complexity | All character types |
| Maximum Age | 365 days or per risk assessment |
| Storage | Encrypted vault/secrets manager |
| Access | Restricted to authorized administrators |

<!-- CUSTOMIZE: Adjust requirements based on your organization's risk tolerance and technical capabilities -->

## 4. Password Creation Guidelines

### 4.1 Do's

- Use passphrases: multiple random words (e.g., "correct-horse-battery-staple")
- Make passwords unique for each account
- Use a password manager for generating and storing passwords
- Include a mix of character types
- Make passwords memorable but not guessable

### 4.2 Don'ts

- Don't use personal information (names, birthdays, pets)
- Don't use dictionary words alone
- Don't use common patterns (Password1!, Qwerty123)
- Don't use keyboard patterns (asdfgh, 12345)
- Don't increment old passwords (Password1 → Password2)
- Don't use same password across accounts
- Don't use variations of username

### 4.3 Prohibited Passwords

Systems should reject:
- Passwords containing the username
- Common passwords (from published breach lists)
- Sequential characters (abc, 123)
- Repeated characters (aaa, 111)
- Context-specific words (company name, "password")

## 5. Password Protection

### 5.1 Handling Requirements

| Requirement | Description |
|-------------|-------------|
| Never share passwords | Even with IT, managers, or colleagues |
| Never write down passwords | Use approved password managers instead |
| Never send in plaintext | No email, chat, or unencrypted channels |
| Never store in browsers | Use enterprise password managers only |
| Never reuse passwords | Each account needs unique password |

### 5.2 Password Storage

**Approved methods:**
- Enterprise password manager: [SPECIFY TOOL]
- Operating system credential store (with device encryption)
- Hardware security tokens (for privileged accounts)

**Not approved:**
- Plain text files
- Spreadsheets
- Sticky notes or paper
- Email or chat
- Personal password managers for work accounts

### 5.3 Password Transmission

- Never transmit passwords via email or unencrypted chat
- Use secure password sharing features of password managers
- For temporary passwords, use separate channel from username
- Change immediately after receiving a temporary password

## 6. Multi-Factor Authentication (MFA)

### 6.1 When Required

MFA is required for:
- All remote/VPN access
- Privileged and administrative accounts
- Cloud service administration
- Access to Confidential or Restricted data
- Email access from non-corporate devices
- Self-service password reset

<!-- CUSTOMIZE: Add or remove MFA requirements based on your systems -->

### 6.2 Approved MFA Methods

| Priority | Method | Use Case |
|----------|--------|----------|
| Preferred | Hardware security keys (FIDO2) | High-value accounts |
| Acceptable | Authenticator apps (TOTP) | Standard accounts |
| Acceptable | Push notifications (verified) | Standard accounts |
| Discouraged | SMS codes | Only when others unavailable |
| Not Allowed | Email codes | Not approved |

### 6.3 MFA Recovery

- Recovery codes must be stored securely
- Report lost MFA devices immediately
- MFA reset requires identity verification

## 7. Password Reset

### 7.1 Self-Service Reset

- Available for standard accounts
- Requires identity verification
- MFA verification when possible
- Security questions as fallback (if used, strong questions)

### 7.2 Help Desk Reset

- Verify user identity before reset
- Use temporary passwords (expire on first use)
- Communicate via secure channel
- Document the reset request

### 7.3 After Reset

- Change temporary password immediately
- Do not reuse previous passwords
- Report if you didn't request the reset

## 8. Compromise Response

### 8.1 If You Suspect Compromise

Immediately:
1. Change the password
2. Report to IT Security: [CONTACT]
3. Review account activity
4. Change passwords on any accounts sharing the same password

### 8.2 System-Detected Compromise

If a password is found in breach databases:
- Immediate forced password change
- Account activity review
- User notification

## 9. Special Account Types

### 9.1 Shared/Group Accounts

- Discouraged; use individual accounts where possible
- Require documented business justification
- Track all authorized users
- Change password when any user's access is removed
- Annual review of necessity

### 9.2 Default/Vendor Accounts

- Change all default passwords before production use
- Disable vendor accounts when not needed
- Document all system accounts

### 9.3 Emergency/Break-Glass Accounts

- Store credentials in secure vault
- Dual control for access
- Automated alerts on use
- Full audit logging
- Password change after each use

## 10. Compliance

### 10.1 Monitoring

- Failed login attempts monitored
- Password changes logged
- Compliance reported to management

### 10.2 Violations

Violations may result in:
- Mandatory password training
- Temporary access suspension
- Disciplinary action

## 11. Related Documents

- [Access Control Policy](./access-control-policy.md)
- [Acceptable Use Policy](./acceptable-use-policy.md)
- [Password Reset Procedure](../procedures/password-reset-procedure.md)

## 12. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

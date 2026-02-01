# Mobile Device Policy

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

This policy establishes security requirements for mobile devices used to access [ORGANIZATION NAME]'s information, systems, and networks.

## 2. Scope

This policy applies to:
- Company-owned mobile devices (smartphones, tablets)
- Personal devices used for work (BYOD)
- All employees, contractors, and third parties
- Any device capable of accessing company email, data, or systems

## 3. Definitions

| Term | Definition |
|------|------------|
| **Mobile Device** | Smartphones, tablets, and similar portable computing devices |
| **BYOD** | Bring Your Own Device - personal devices used for work |
| **MDM** | Mobile Device Management - software to manage and secure devices |
| **MAM** | Mobile Application Management - managing apps without full device control |
| **Container** | Secure, isolated area on device for work data |

## 4. Policy Statements

### 4.1 Device Categories

| Category | Definition | Policy |
|----------|------------|--------|
| **Company-Owned** | Provided by organization | Full MDM control |
| **BYOD - Full** | Personal device with MDM | Work container + policies |
| **BYOD - Limited** | Personal device, email only | MAM for email only |
| **Not Permitted** | Unauthorized devices | No company data access |

### 4.2 Device Requirements

#### 4.2.1 Supported Platforms

| Platform | Minimum Version | Notes |
|----------|-----------------|-------|
| iOS | [iOS 15+] | Supported |
| Android | [Android 12+] | Must support Android Enterprise |
| Other | - | Not supported without approval |

<!-- CUSTOMIZE: Update minimum versions based on your requirements -->

#### 4.2.2 Prohibited Devices

The following are not permitted for company use:
- Jailbroken or rooted devices
- Devices with unknown sources/sideloading enabled
- Devices with outdated operating systems
- Devices that cannot support required security features
- Devices with known security vulnerabilities

### 4.3 Security Requirements

#### 4.3.1 All Mobile Devices

| Requirement | Specification |
|-------------|---------------|
| Screen Lock | Required - PIN (6+ digits), password, or biometric |
| Auto-Lock | Maximum 5 minutes |
| Encryption | Device encryption enabled |
| OS Updates | Installed within 14 days of release |
| MDM/MAM | Enrolled in company management |
| Remote Wipe | Capability enabled |

#### 4.3.2 Additional Requirements by Category

| Requirement | Company-Owned | BYOD-Full | BYOD-Limited |
|-------------|---------------|-----------|--------------|
| Full MDM enrollment | Required | Required | Not required |
| Work container | N/A | Required | N/A |
| Company antimalware | Required | Required | Not required |
| VPN for network access | Required | Required | Required |
| Location services | Optional | Not required | Not required |
| Backup to company systems | Required | Work data only | N/A |

### 4.4 Authentication

#### 4.4.1 Device Authentication

- Strong PIN (6+ numeric) or password (8+ alphanumeric)
- Biometric authentication permitted in addition to PIN/password
- Failed attempt limit: 10 attempts, then wipe (company) or lock (BYOD)

#### 4.4.2 Application Authentication

- Corporate apps require separate authentication
- Multi-factor authentication required for:
  - Email access
  - Access to sensitive applications
  - VPN connection
- Session timeout: Maximum 8 hours

### 4.5 Data Protection

#### 4.5.1 Data Storage

| Data Type | Company Device | BYOD |
|-----------|----------------|------|
| Confidential data | Encrypted container | Work container only |
| Internal data | Device storage OK | Work container only |
| Personal data (company's) | Not permitted locally | Not permitted locally |

#### 4.5.2 Data Transfer

- No transferring sensitive data to personal apps/storage
- Copy/paste between work and personal may be restricted
- Cloud backup of work data only to approved services
- Screenshots may be disabled for sensitive applications

### 4.6 Application Management

#### 4.6.1 Company Devices

- Only approved applications may be installed
- App store access may be restricted
- Company applications pushed via MDM
- Unapproved apps subject to removal

#### 4.6.2 BYOD

- Work applications installed in managed container
- Personal applications not monitored or managed
- Work applications may not access personal data
- Separation enforced technically

#### 4.6.3 Prohibited Applications

The following application categories are prohibited on devices accessing work data:
- Non-official app stores
- Apps requesting excessive permissions
- Known malicious applications
- [Add specific prohibited apps]

### 4.7 Network Security

#### 4.7.1 WiFi

- Use secure networks only (WPA2/WPA3)
- Avoid public WiFi for sensitive work
- Auto-connect to untrusted networks disabled
- VPN required for access to internal resources

#### 4.7.2 Bluetooth

- Keep Bluetooth off when not in use
- Only pair with trusted devices
- Do not accept unknown pairing requests
- Disable discoverability

#### 4.7.3 VPN

- VPN required for accessing internal network
- VPN app managed by MDM
- Per-app VPN may be configured
- Split tunneling [permitted/not permitted]

### 4.8 Lost or Stolen Devices

#### 4.8.1 Immediate Actions

If a device is lost or stolen:

1. **Report immediately** to IT Security: [CONTACT]
2. **Remote locate** (if enabled and appropriate)
3. **Remote lock** device
4. **Remote wipe** if recovery unlikely
5. **Change passwords** for accounts accessed on device
6. **Document** incident

#### 4.8.2 Organizational Response

- IT initiates remote lock/wipe
- Review access logs
- Reset compromised credentials
- Assess data exposure
- File incident report
- Police report if theft

### 4.9 BYOD Specific Requirements

#### 4.9.1 Enrollment

Before BYOD enrollment:
- [ ] Review and accept BYOD agreement
- [ ] Device meets minimum requirements
- [ ] MDM/MAM enrollment completed
- [ ] Work container configured
- [ ] Required apps installed

#### 4.9.2 User Responsibilities

BYOD users must:
- Maintain personal device security
- Keep operating system updated
- Report security issues immediately
- Not remove MDM/MAM software
- Accept company's right to wipe work data

#### 4.9.3 Company Rights

[ORGANIZATION NAME] reserves the right to:
- Remote wipe work container
- Revoke access at any time
- Monitor work applications
- Require device inspection if security concern

Company will NOT:
- Access personal data, photos, or messages
- Track personal location (unless device stolen)
- Read personal emails or app data

#### 4.9.4 BYOD Termination

On employment termination or BYOD revocation:
- Work data remotely wiped
- Work container removed
- Accounts disabled
- Personal data remains intact

### 4.10 Company Device Provisioning

#### 4.10.1 Issuance

- Devices assigned to individual users
- Asset tag and registration
- User signs device agreement
- Device configured with standard profile
- Required apps pre-installed

#### 4.10.2 Return

On termination or device refresh:
- Return device within [5] business days
- Device reset to factory defaults
- Data backed up and verified
- Asset deregistered

## 5. Roles and Responsibilities

### 5.1 Users
- Comply with all mobile device policies
- Protect device from loss or theft
- Report incidents immediately
- Keep device updated

### 5.2 IT Department
- Manage MDM platform
- Provision and configure devices
- Support mobile users
- Enforce compliance

### 5.3 IT Security
- Define security policies
- Monitor compliance
- Investigate incidents
- Review and update policy

## 6. Compliance

### 6.1 Monitoring

IT may monitor:
- Device compliance status
- MDM enrollment
- Security settings
- Work application usage

### 6.2 Non-Compliance

Non-compliant devices may:
- Lose access to company resources
- Be remotely wiped (work data)
- Require remediation before access restored

### 6.3 Violations

Policy violations may result in:
- Loss of BYOD privileges
- Disciplinary action
- Termination in severe cases

## 7. Related Documents

- [Remote Work Policy](./remote-work-policy.md)
- [Acceptable Use Policy](./acceptable-use-policy.md)
- [Data Classification Policy](./data-classification-policy.md)
- [Lost Device Playbook](../crisis-management/playbooks/lost-device-playbook.md)

## 8. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

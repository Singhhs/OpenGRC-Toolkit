# Cryptography Policy

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

This policy establishes requirements for the use of cryptographic controls to protect the confidentiality, integrity, and authenticity of [ORGANIZATION NAME]'s information.

## 2. Scope

This policy applies to:
- All data requiring cryptographic protection
- All systems using encryption
- All encryption keys and certificates
- All personnel implementing or using encryption

## 3. Policy Statements

### 3.1 Cryptographic Requirements

#### 3.1.1 When Encryption is Required

| Data Type | At Rest | In Transit | Notes |
|-----------|---------|------------|-------|
| Restricted | Required | Required | Strongest algorithms |
| Confidential | Required | Required | Standard algorithms |
| Personal Data (PII) | Required | Required | Regulatory compliance |
| Internal | Recommended | Required | Based on risk |
| Public | Optional | Recommended | TLS for websites |

#### 3.1.2 When Encryption is Mandatory

Encryption is mandatory for:
- Data transmitted over public networks
- Wireless network traffic
- Mobile devices and laptops
- Removable media containing sensitive data
- Cloud storage of sensitive data
- Backups of sensitive data
- Authentication credentials
- Remote access connections

### 3.2 Approved Algorithms

#### 3.2.1 Symmetric Encryption

| Algorithm | Key Length | Status |
|-----------|------------|--------|
| AES | 256-bit | Approved (preferred) |
| AES | 128-bit | Approved |
| 3DES | 168-bit | Deprecated - phase out |
| DES | 56-bit | Prohibited |

#### 3.2.2 Asymmetric Encryption

| Algorithm | Key Length | Status |
|-----------|------------|--------|
| RSA | 4096-bit | Approved (preferred) |
| RSA | 2048-bit | Approved (minimum) |
| RSA | 1024-bit | Prohibited |
| ECDSA/ECDH | P-384/P-256 | Approved |
| Ed25519 | 256-bit | Approved |

#### 3.2.3 Hashing Algorithms

| Algorithm | Status | Use Case |
|-----------|--------|----------|
| SHA-512 | Approved | Preferred for new implementations |
| SHA-384 | Approved | Where required |
| SHA-256 | Approved | General purpose |
| SHA-1 | Prohibited | Not for new use |
| MD5 | Prohibited | Not for security |

#### 3.2.4 TLS/SSL

| Version | Status |
|---------|--------|
| TLS 1.3 | Approved (preferred) |
| TLS 1.2 | Approved |
| TLS 1.1 | Prohibited |
| TLS 1.0 | Prohibited |
| SSL 3.0 | Prohibited |
| SSL 2.0 | Prohibited |

### 3.3 Key Management

#### 3.3.1 Key Generation

- Use cryptographically secure random number generators
- Generate keys in secure environment
- Minimum key lengths as specified above
- Document key generation procedures

#### 3.3.2 Key Storage

| Key Type | Storage Method |
|----------|----------------|
| Master keys | Hardware Security Module (HSM) |
| Production keys | Encrypted key vault/HSM |
| Development keys | Encrypted storage, separate from prod |
| User keys | Protected by strong passphrase |

Keys must NOT be:
- Stored in source code
- Stored in plain text
- Transmitted via email
- Stored in shared locations
- Hard-coded in applications

#### 3.3.3 Key Rotation

| Key Type | Rotation Frequency |
|----------|-------------------|
| SSL/TLS certificates | Annually or on compromise |
| Encryption keys (data at rest) | Annually |
| Signing keys | Per risk assessment |
| API keys | [Quarterly/Semi-annually] |
| SSH keys | Annually |

#### 3.3.4 Key Distribution

- Secure channels only for key distribution
- Split knowledge for highly sensitive keys
- Dual control for master keys
- Documented key handoff procedures

#### 3.3.5 Key Backup and Recovery

- Keys backed up securely
- Backup keys stored separately from data
- Recovery procedures documented and tested
- Dual control for key recovery

#### 3.3.6 Key Destruction

- Keys destroyed when no longer needed
- Destruction documented
- All copies destroyed
- Use approved destruction methods

### 3.4 Certificate Management

#### 3.4.1 Certificate Authorities

- Use trusted, well-known CAs for public certificates
- Internal CA for internal certificates
- Document certificate chain

#### 3.4.2 Certificate Requirements

| Certificate Type | Key Length | Validity | Notes |
|------------------|------------|----------|-------|
| Public Web (SSL/TLS) | RSA 2048+ / ECDSA P-256+ | 1 year max | From trusted CA |
| Internal | RSA 2048+ | Per policy | From internal CA |
| Code Signing | RSA 2048+ | Per policy | Secure storage |
| Client Authentication | RSA 2048+ | 1-2 years | User certificates |

#### 3.4.3 Certificate Lifecycle

- Inventory all certificates
- Monitor expiration dates
- Alert before expiration (30/60/90 days)
- Renew or replace before expiration
- Revoke compromised certificates immediately

### 3.5 Encryption Standards by Use Case

#### 3.5.1 Data at Rest

| Use Case | Standard |
|----------|----------|
| Full disk encryption | AES-256 (BitLocker, FileVault, LUKS) |
| Database encryption | TDE or column-level AES-256 |
| File encryption | AES-256 |
| Backup encryption | AES-256 |
| Cloud storage | AES-256, customer-managed keys preferred |

#### 3.5.2 Data in Transit

| Use Case | Standard |
|----------|----------|
| Web traffic | TLS 1.2+ with strong cipher suites |
| Email | TLS 1.2+ (opportunistic), S/MIME for sensitive |
| API communications | TLS 1.2+ with mutual authentication |
| VPN | IKEv2 with AES-256, or WireGuard |
| File transfer | SFTP or FTPS with AES-256 |
| Database connections | TLS 1.2+ |

#### 3.5.3 Authentication

| Use Case | Standard |
|----------|----------|
| Password storage | Argon2id, bcrypt, or scrypt |
| Session tokens | Cryptographically random, 256-bit |
| API tokens | Cryptographically random, 256-bit |
| Digital signatures | RSA-2048+ or ECDSA P-256+ with SHA-256+ |

### 3.6 Implementation Requirements

#### 3.6.1 General Guidelines

- Use established, well-vetted cryptographic libraries
- Do not implement custom cryptography
- Keep cryptographic libraries updated
- Follow vendor/library best practices
- Have cryptographic implementations reviewed

#### 3.6.2 Prohibited Practices

- Using deprecated or weak algorithms
- Hard-coding keys in source code
- Using predictable or weak keys
- Disabling certificate validation
- Implementing homegrown cryptography
- Using ECB mode for block ciphers

## 4. Roles and Responsibilities

### 4.1 IT Security
- Define cryptographic standards
- Approve cryptographic solutions
- Manage key management infrastructure
- Audit compliance

### 4.2 IT Operations
- Implement encryption solutions
- Manage certificates
- Monitor key/certificate expiration
- Execute key rotation

### 4.3 Development Teams
- Follow approved standards
- Use approved libraries
- Protect keys in applications
- Submit designs for review

### 4.4 System Owners
- Ensure encryption for their systems
- Maintain key management for applications
- Report key compromise

## 5. Compliance

### 5.1 Regulatory Requirements

This policy supports:
- PCI DSS (Requirement 3, 4)
- GDPR (Article 32)
- ISO 27001 (A.8.24)
- HIPAA (encryption standards)

### 5.2 Monitoring

- Certificate monitoring tools
- Key management auditing
- Algorithm compliance scanning
- Configuration reviews

### 5.3 Exceptions

Exceptions require:
- Business justification
- Risk assessment
- Compensating controls
- CISO approval
- Defined expiration

## 6. Related Documents

- [Data Classification Policy](./data-classification-policy.md)
- [Key Management Procedure](../procedures/key-management-procedure.md)
- [Certificate Management Procedure](../procedures/certificate-management-procedure.md)

## 7. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

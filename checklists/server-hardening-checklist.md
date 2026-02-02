# Server Hardening Checklist

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Date** | [DATE] |
| **Assessor** | [NAME] |
| **Server Name** | [SERVER] |
| **OS Type** | ☐ Windows Server ☐ Linux ☐ Other |

---

## Purpose

Use this checklist to verify security hardening of servers before deployment to production or during periodic security reviews. Adapt based on operating system and server role.

---

## Section 1: Server Information

| Field | Information |
|-------|-------------|
| Server Name/Hostname | |
| IP Address(es) | |
| Operating System | |
| OS Version | |
| Server Role | |
| Environment | ☐ Production ☐ Staging ☐ Development ☐ Test |
| Data Classification | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Server Owner | |
| Last Hardening Date | |

---

## Section 2: Operating System Hardening

### 2.1 Installation and Configuration

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 2.1.1 | Minimal installation (only required components) | ☐ Yes ☐ No ☐ N/A | |
| 2.1.2 | Latest OS version/service pack installed | ☐ Yes ☐ No | Version: |
| 2.1.3 | All security patches applied | ☐ Yes ☐ No | Last patched: |
| 2.1.4 | Automatic updates configured (or patch management) | ☐ Yes ☐ No | |
| 2.1.5 | Unnecessary services disabled | ☐ Yes ☐ No ☐ Partial | |
| 2.1.6 | Unnecessary features/roles removed | ☐ Yes ☐ No ☐ Partial | |
| 2.1.7 | Default accounts disabled or renamed | ☐ Yes ☐ No | |
| 2.1.8 | Guest accounts disabled | ☐ Yes ☐ No | |
| 2.1.9 | System time synchronized (NTP) | ☐ Yes ☐ No | |
| 2.1.10 | Appropriate hostname configured | ☐ Yes ☐ No | |

### 2.2 Windows-Specific

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 2.2.1 | Windows Firewall enabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.2 | Windows Defender/antimalware enabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.3 | PowerShell execution policy configured | ☐ Yes ☐ No ☐ N/A | Policy: |
| 2.2.4 | PowerShell logging enabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.5 | LAPS configured for local admin | ☐ Yes ☐ No ☐ N/A | |
| 2.2.6 | SMBv1 disabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.7 | LLMNR disabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.8 | NetBIOS over TCP/IP disabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.9 | Remote Desktop secured (NLA enabled) | ☐ Yes ☐ No ☐ N/A | |
| 2.2.10 | Credential Guard enabled (if supported) | ☐ Yes ☐ No ☐ N/A | |

### 2.3 Linux-Specific

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 2.3.1 | SELinux/AppArmor enabled and enforcing | ☐ Yes ☐ No ☐ N/A | |
| 2.3.2 | Firewall enabled (iptables/firewalld/ufw) | ☐ Yes ☐ No ☐ N/A | |
| 2.3.3 | Root login disabled for SSH | ☐ Yes ☐ No ☐ N/A | |
| 2.3.4 | SSH protocol 2 only | ☐ Yes ☐ No ☐ N/A | |
| 2.3.5 | SSH key-based authentication preferred | ☐ Yes ☐ No ☐ N/A | |
| 2.3.6 | Unnecessary SUID/SGID binaries removed | ☐ Yes ☐ No ☐ N/A | |
| 2.3.7 | /tmp mounted with noexec,nosuid | ☐ Yes ☐ No ☐ N/A | |
| 2.3.8 | Core dumps disabled | ☐ Yes ☐ No ☐ N/A | |
| 2.3.9 | Secure boot parameters configured | ☐ Yes ☐ No ☐ N/A | |
| 2.3.10 | Automatic security updates configured | ☐ Yes ☐ No ☐ N/A | |

---

## Section 3: Account and Access Control

### 3.1 Account Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.1.1 | Local admin/root password strong and unique | ☐ Yes ☐ No | |
| 3.1.2 | Service accounts use minimum privileges | ☐ Yes ☐ No | |
| 3.1.3 | Service account passwords managed securely | ☐ Yes ☐ No | |
| 3.1.4 | Unused accounts disabled or removed | ☐ Yes ☐ No | |
| 3.1.5 | Account lockout policy configured | ☐ Yes ☐ No | Threshold: |
| 3.1.6 | Password complexity requirements enforced | ☐ Yes ☐ No | |
| 3.1.7 | Password expiration configured (if applicable) | ☐ Yes ☐ No ☐ N/A | Days: |
| 3.1.8 | Password history enforced | ☐ Yes ☐ No | Count: |

### 3.2 Access Control

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.2.1 | File system permissions follow least privilege | ☐ Yes ☐ No ☐ Partial | |
| 3.2.2 | Sensitive files have restricted permissions | ☐ Yes ☐ No | |
| 3.2.3 | Admin/sudo access restricted | ☐ Yes ☐ No | |
| 3.2.4 | Interactive login restricted to required accounts | ☐ Yes ☐ No | |
| 3.2.5 | Remote access restricted to specific users/groups | ☐ Yes ☐ No | |

---

## Section 4: Network Hardening

### 4.1 Network Configuration

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.1.1 | Only required network ports open | ☐ Yes ☐ No | Ports: |
| 4.1.2 | Host-based firewall enabled | ☐ Yes ☐ No | |
| 4.1.3 | Firewall rules follow least privilege | ☐ Yes ☐ No | |
| 4.1.4 | IP forwarding disabled (unless required) | ☐ Yes ☐ No ☐ N/A | |
| 4.1.5 | Source routing disabled | ☐ Yes ☐ No | |
| 4.1.6 | ICMP redirects disabled | ☐ Yes ☐ No | |
| 4.1.7 | TCP SYN cookies enabled | ☐ Yes ☐ No ☐ N/A | |
| 4.1.8 | Unnecessary network protocols disabled | ☐ Yes ☐ No | |

### 4.2 Remote Access

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.2.1 | SSH/RDP restricted to specific networks | ☐ Yes ☐ No | |
| 4.2.2 | SSH using strong ciphers only | ☐ Yes ☐ No ☐ N/A | |
| 4.2.3 | SSH idle timeout configured | ☐ Yes ☐ No ☐ N/A | Timeout: |
| 4.2.4 | SSH banner configured | ☐ Yes ☐ No ☐ N/A | |
| 4.2.5 | Remote management via encrypted protocols | ☐ Yes ☐ No | |
| 4.2.6 | Management interface on separate network | ☐ Yes ☐ No ☐ N/A | |

---

## Section 5: Security Software

### 5.1 Antimalware

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.1.1 | Antimalware/EDR solution installed | ☐ Yes ☐ No | Product: |
| 5.1.2 | Real-time protection enabled | ☐ Yes ☐ No | |
| 5.1.3 | Signatures updated automatically | ☐ Yes ☐ No | |
| 5.1.4 | Regular scheduled scans configured | ☐ Yes ☐ No | Frequency: |
| 5.1.5 | Centralized management and reporting | ☐ Yes ☐ No | |

### 5.2 Host Intrusion Prevention

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.2.1 | HIPS/HIDS installed (if required) | ☐ Yes ☐ No ☐ N/A | |
| 5.2.2 | File integrity monitoring configured | ☐ Yes ☐ No ☐ N/A | |
| 5.2.3 | Critical file changes alerted | ☐ Yes ☐ No ☐ N/A | |

---

## Section 6: Logging and Auditing

### 6.1 Audit Configuration

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 6.1.1 | Audit logging enabled | ☐ Yes ☐ No | |
| 6.1.2 | Login attempts logged (success and failure) | ☐ Yes ☐ No | |
| 6.1.3 | Privilege escalation logged | ☐ Yes ☐ No | |
| 6.1.4 | Account management logged | ☐ Yes ☐ No | |
| 6.1.5 | System events logged | ☐ Yes ☐ No | |
| 6.1.6 | Security policy changes logged | ☐ Yes ☐ No | |
| 6.1.7 | Object access logging configured (if required) | ☐ Yes ☐ No ☐ N/A | |
| 6.1.8 | Command/shell history logging | ☐ Yes ☐ No | |

### 6.2 Log Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 6.2.1 | Logs forwarded to central logging | ☐ Yes ☐ No | |
| 6.2.2 | Log retention meets requirements | ☐ Yes ☐ No | Retention: |
| 6.2.3 | Logs protected from tampering | ☐ Yes ☐ No | |
| 6.2.4 | Log rotation configured | ☐ Yes ☐ No | |
| 6.2.5 | Logs do not contain sensitive data | ☐ Yes ☐ No ☐ Partial | |

---

## Section 7: Data Protection

### 7.1 Encryption

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.1.1 | Disk encryption enabled (if required) | ☐ Yes ☐ No ☐ N/A | Method: |
| 7.1.2 | Encryption keys properly managed | ☐ Yes ☐ No ☐ N/A | |
| 7.1.3 | TLS/SSL configured for services | ☐ Yes ☐ No ☐ Partial | |
| 7.1.4 | Weak ciphers disabled | ☐ Yes ☐ No | |
| 7.1.5 | Certificates valid and trusted | ☐ Yes ☐ No ☐ N/A | |

### 7.2 Data Handling

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.2.1 | Sensitive data identified and protected | ☐ Yes ☐ No ☐ N/A | |
| 7.2.2 | Temporary files cleaned up | ☐ Yes ☐ No | |
| 7.2.3 | Swap/pagefile encrypted (if sensitive data) | ☐ Yes ☐ No ☐ N/A | |

---

## Section 8: Application Hardening

### 8.1 Web Server (if applicable)

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 8.1.1 | Server version hidden | ☐ Yes ☐ No ☐ N/A | |
| 8.1.2 | Directory listing disabled | ☐ Yes ☐ No ☐ N/A | |
| 8.1.3 | Default content removed | ☐ Yes ☐ No ☐ N/A | |
| 8.1.4 | Security headers configured | ☐ Yes ☐ No ☐ N/A | |
| 8.1.5 | HTTPS enforced | ☐ Yes ☐ No ☐ N/A | |
| 8.1.6 | Request size limits configured | ☐ Yes ☐ No ☐ N/A | |

### 8.2 Database Server (if applicable)

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 8.2.1 | Default accounts removed/disabled | ☐ Yes ☐ No ☐ N/A | |
| 8.2.2 | Strong authentication required | ☐ Yes ☐ No ☐ N/A | |
| 8.2.3 | Network access restricted | ☐ Yes ☐ No ☐ N/A | |
| 8.2.4 | Audit logging enabled | ☐ Yes ☐ No ☐ N/A | |
| 8.2.5 | Encryption enabled (TDE, connections) | ☐ Yes ☐ No ☐ N/A | |
| 8.2.6 | Backup encryption enabled | ☐ Yes ☐ No ☐ N/A | |

---

## Section 9: Backup and Recovery

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 9.1 | Regular backups configured | ☐ Yes ☐ No | Frequency: |
| 9.2 | Backups tested for recoverability | ☐ Yes ☐ No | Last test: |
| 9.3 | Backup data encrypted | ☐ Yes ☐ No | |
| 9.4 | Backups stored securely (offsite/separate) | ☐ Yes ☐ No | |
| 9.5 | Recovery procedures documented | ☐ Yes ☐ No | |

---

## Section 10: Compliance Verification

### 10.1 Benchmark Compliance

| Benchmark | Compliant | Score | Notes |
|-----------|-----------|-------|-------|
| CIS Benchmark | ☐ Yes ☐ No ☐ Partial | | |
| DISA STIG | ☐ Yes ☐ No ☐ Partial ☐ N/A | | |
| Vendor Security Baseline | ☐ Yes ☐ No ☐ Partial | | |
| Organization Baseline | ☐ Yes ☐ No ☐ Partial | | |

### 10.2 Vulnerability Assessment

| # | Item | Status | Notes |
|---|------|--------|-------|
| 10.2.1 | Vulnerability scan performed | ☐ Yes ☐ No | Date: |
| 10.2.2 | Critical vulnerabilities remediated | ☐ Yes ☐ No ☐ N/A | |
| 10.2.3 | High vulnerabilities remediated | ☐ Yes ☐ No ☐ N/A | |
| 10.2.4 | Remaining vulnerabilities documented | ☐ Yes ☐ No ☐ N/A | |

---

## Section 11: Assessment Summary

### 11.1 Findings

| # | Finding | Severity | Remediation Required |
|---|---------|----------|---------------------|
| 1 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 2 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 3 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 4 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 5 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |

### 11.2 Approval Decision

☐ **Approved** - Server meets hardening requirements
☐ **Approved with Conditions** - Must address findings within [timeframe]
☐ **Not Approved** - Significant hardening gaps exist

---

## Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Assessor | | | |
| Server Owner | | | |
| Security Manager | | | |

---

[Back to Checklists](./README.md) | [Back to Home](../README.md)

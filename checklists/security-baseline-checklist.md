# Security Baseline Checklist

**Organization:** [ORGANIZATION NAME]
**Assessment Date:** [DATE]
**Assessor:** [NAME]
**Scope:** [DEPARTMENT/SYSTEM/ORGANIZATION-WIDE]

---

## Purpose

This checklist provides a baseline security assessment covering fundamental security controls that every organization should have in place.

---

## 1. Governance and Policy

### 1.1 Security Program

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Information security policy documented and approved | [ ] | [ ] | [ ] | |
| Security responsibilities assigned | [ ] | [ ] | [ ] | |
| Management demonstrates commitment to security | [ ] | [ ] | [ ] | |
| Security budget allocated | [ ] | [ ] | [ ] | |
| Regular security reporting to management | [ ] | [ ] | [ ] | |

### 1.2 Policies and Procedures

| Policy | Exists | Current (<2 yrs) | Communicated | Notes |
|--------|--------|------------------|--------------|-------|
| Information Security Policy | [ ] | [ ] | [ ] | |
| Acceptable Use Policy | [ ] | [ ] | [ ] | |
| Access Control Policy | [ ] | [ ] | [ ] | |
| Data Classification Policy | [ ] | [ ] | [ ] | |
| Incident Response Policy | [ ] | [ ] | [ ] | |
| Password Policy | [ ] | [ ] | [ ] | |
| Remote Work Policy | [ ] | [ ] | [ ] | |
| Backup Policy | [ ] | [ ] | [ ] | |

---

## 2. Access Control

### 2.1 Identity Management

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Unique user IDs for all users | [ ] | [ ] | [ ] | |
| Access based on job requirements | [ ] | [ ] | [ ] | |
| Access provisioning process documented | [ ] | [ ] | [ ] | |
| Access revoked on termination | [ ] | [ ] | [ ] | |
| Regular access reviews performed | [ ] | [ ] | [ ] | |

### 2.2 Authentication

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Strong password requirements enforced | [ ] | [ ] | [ ] | |
| Account lockout after failed attempts | [ ] | [ ] | [ ] | |
| MFA for remote access | [ ] | [ ] | [ ] | |
| MFA for privileged accounts | [ ] | [ ] | [ ] | |
| MFA for cloud services | [ ] | [ ] | [ ] | |
| Password manager available/encouraged | [ ] | [ ] | [ ] | |

### 2.3 Privileged Access

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Privileged accounts identified and documented | [ ] | [ ] | [ ] | |
| Separate accounts for admin activities | [ ] | [ ] | [ ] | |
| Privileged access logging enabled | [ ] | [ ] | [ ] | |
| Privileged access reviewed regularly | [ ] | [ ] | [ ] | |
| Just-in-time access considered | [ ] | [ ] | [ ] | |

---

## 3. Endpoint Security

### 3.1 Workstations

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Anti-malware installed and updated | [ ] | [ ] | [ ] | |
| Operating system patched regularly | [ ] | [ ] | [ ] | |
| Local firewall enabled | [ ] | [ ] | [ ] | |
| Full disk encryption enabled | [ ] | [ ] | [ ] | |
| Automatic screen lock configured | [ ] | [ ] | [ ] | |
| USB restrictions in place | [ ] | [ ] | [ ] | |
| Endpoint detection & response (EDR) | [ ] | [ ] | [ ] | |

### 3.2 Mobile Devices

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| MDM solution deployed | [ ] | [ ] | [ ] | |
| Device encryption required | [ ] | [ ] | [ ] | |
| PIN/password required | [ ] | [ ] | [ ] | |
| Remote wipe capability | [ ] | [ ] | [ ] | |
| App restrictions in place | [ ] | [ ] | [ ] | |

### 3.3 Servers

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Hardened configurations | [ ] | [ ] | [ ] | |
| Regular patching | [ ] | [ ] | [ ] | |
| Anti-malware installed | [ ] | [ ] | [ ] | |
| Logging enabled | [ ] | [ ] | [ ] | |
| Unnecessary services disabled | [ ] | [ ] | [ ] | |

---

## 4. Network Security

### 4.1 Perimeter Security

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Firewall deployed | [ ] | [ ] | [ ] | |
| Default deny rule implemented | [ ] | [ ] | [ ] | |
| Firewall rules documented and reviewed | [ ] | [ ] | [ ] | |
| IDS/IPS deployed | [ ] | [ ] | [ ] | |
| DDoS protection for critical services | [ ] | [ ] | [ ] | |

### 4.2 Network Segmentation

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Network segmented by function | [ ] | [ ] | [ ] | |
| Sensitive systems isolated | [ ] | [ ] | [ ] | |
| Guest network separated | [ ] | [ ] | [ ] | |
| Development/test separated from production | [ ] | [ ] | [ ] | |

### 4.3 Wireless Security

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| WPA3/WPA2 Enterprise used | [ ] | [ ] | [ ] | |
| Strong WiFi passwords | [ ] | [ ] | [ ] | |
| Guest network isolated | [ ] | [ ] | [ ] | |
| Rogue AP detection | [ ] | [ ] | [ ] | |

### 4.4 Remote Access

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| VPN for remote network access | [ ] | [ ] | [ ] | |
| MFA required for VPN | [ ] | [ ] | [ ] | |
| VPN logging enabled | [ ] | [ ] | [ ] | |
| Split tunneling controlled | [ ] | [ ] | [ ] | |

---

## 5. Data Protection

### 5.1 Data Classification

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Data classification scheme defined | [ ] | [ ] | [ ] | |
| Sensitive data identified | [ ] | [ ] | [ ] | |
| Data handling procedures documented | [ ] | [ ] | [ ] | |
| Data labeling in use | [ ] | [ ] | [ ] | |

### 5.2 Encryption

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Data encrypted at rest (sensitive) | [ ] | [ ] | [ ] | |
| Data encrypted in transit (TLS) | [ ] | [ ] | [ ] | |
| Email encryption available | [ ] | [ ] | [ ] | |
| Encryption keys properly managed | [ ] | [ ] | [ ] | |

### 5.3 Data Loss Prevention

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| DLP solution implemented | [ ] | [ ] | [ ] | |
| USB/removable media controlled | [ ] | [ ] | [ ] | |
| Cloud storage controlled | [ ] | [ ] | [ ] | |
| Email DLP in place | [ ] | [ ] | [ ] | |

---

## 6. Backup and Recovery

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Regular backups performed | [ ] | [ ] | [ ] | |
| Backups stored offsite/cloud | [ ] | [ ] | [ ] | |
| Backups encrypted | [ ] | [ ] | [ ] | |
| Backup restoration tested | [ ] | [ ] | [ ] | |
| Immutable/air-gapped backups | [ ] | [ ] | [ ] | |
| RTO/RPO defined | [ ] | [ ] | [ ] | |

---

## 7. Vulnerability Management

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Regular vulnerability scanning | [ ] | [ ] | [ ] | |
| Patch management process | [ ] | [ ] | [ ] | |
| Critical patches applied within SLA | [ ] | [ ] | [ ] | |
| Penetration testing performed | [ ] | [ ] | [ ] | |
| Vulnerability remediation tracked | [ ] | [ ] | [ ] | |

---

## 8. Email Security

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Email filtering/gateway | [ ] | [ ] | [ ] | |
| Anti-phishing protection | [ ] | [ ] | [ ] | |
| SPF/DKIM/DMARC implemented | [ ] | [ ] | [ ] | |
| Attachment scanning | [ ] | [ ] | [ ] | |
| Link rewriting/sandboxing | [ ] | [ ] | [ ] | |
| User reporting mechanism | [ ] | [ ] | [ ] | |

---

## 9. Logging and Monitoring

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Security logging enabled | [ ] | [ ] | [ ] | |
| Logs centrally collected | [ ] | [ ] | [ ] | |
| Log retention adequate | [ ] | [ ] | [ ] | |
| Logs protected from tampering | [ ] | [ ] | [ ] | |
| Security monitoring in place | [ ] | [ ] | [ ] | |
| Alerts configured for key events | [ ] | [ ] | [ ] | |
| Regular log review | [ ] | [ ] | [ ] | |

---

## 10. Incident Response

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Incident response plan documented | [ ] | [ ] | [ ] | |
| Incident response team defined | [ ] | [ ] | [ ] | |
| Incident reporting mechanism | [ ] | [ ] | [ ] | |
| Contact information current | [ ] | [ ] | [ ] | |
| Incident response tested | [ ] | [ ] | [ ] | |

---

## 11. Security Awareness

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Security awareness training program | [ ] | [ ] | [ ] | |
| Training for all employees | [ ] | [ ] | [ ] | |
| Training records maintained | [ ] | [ ] | [ ] | |
| Phishing simulations conducted | [ ] | [ ] | [ ] | |
| Role-specific training | [ ] | [ ] | [ ] | |

---

## 12. Third-Party Security

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Vendor security assessments | [ ] | [ ] | [ ] | |
| Security requirements in contracts | [ ] | [ ] | [ ] | |
| Vendor access controlled | [ ] | [ ] | [ ] | |
| Critical vendors identified | [ ] | [ ] | [ ] | |

---

## 13. Physical Security

| Control | In Place | Partial | Not In Place | Notes |
|---------|----------|---------|--------------|-------|
| Building access controlled | [ ] | [ ] | [ ] | |
| Visitor management | [ ] | [ ] | [ ] | |
| Server room secured | [ ] | [ ] | [ ] | |
| Clean desk policy | [ ] | [ ] | [ ] | |
| Equipment disposal secure | [ ] | [ ] | [ ] | |

---

## Summary

| Category | In Place | Partial | Not In Place | Score |
|----------|----------|---------|--------------|-------|
| Governance | /5 | /5 | /5 | % |
| Access Control | /15 | /15 | /15 | % |
| Endpoint Security | /17 | /17 | /17 | % |
| Network Security | /16 | /16 | /16 | % |
| Data Protection | /12 | /12 | /12 | % |
| Backup | /6 | /6 | /6 | % |
| Vulnerability Mgmt | /5 | /5 | /5 | % |
| Email Security | /6 | /6 | /6 | % |
| Logging | /7 | /7 | /7 | % |
| Incident Response | /5 | /5 | /5 | % |
| Awareness | /5 | /5 | /5 | % |
| Third Party | /4 | /4 | /4 | % |
| Physical | /5 | /5 | /5 | % |
| **TOTAL** | | | | **%** |

---

## Priority Findings

| # | Finding | Risk Level | Recommendation |
|---|---------|------------|----------------|
| 1 | | High/Medium/Low | |
| 2 | | | |
| 3 | | | |

---

**Assessed By:** ___________________ **Date:** ___________

**Reviewed By:** ___________________ **Date:** ___________

---

[Back to Checklists](./README.md) | [Back to Home](../README.md)

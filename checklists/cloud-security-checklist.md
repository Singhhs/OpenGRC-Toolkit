# Cloud Security Checklist

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Date** | [DATE] |
| **Assessor** | [NAME] |
| **Cloud Service** | [SERVICE NAME] |
| **Provider** | [AWS / Azure / GCP / Other] |

---

## Purpose

Use this checklist to assess the security configuration and controls of cloud services and environments. Applicable for IaaS, PaaS, and SaaS deployments.

---

## Section 1: Service Information

| Field | Information |
|-------|-------------|
| Service/Application Name | |
| Cloud Provider | |
| Service Type | ☐ IaaS ☐ PaaS ☐ SaaS |
| Account/Subscription ID | |
| Regions Used | |
| Data Classification | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Service Owner | |

---

## Section 2: Identity and Access Management

### 2.1 Account Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 2.1.1 | Root/global admin account secured and rarely used | ☐ Yes ☐ No ☐ N/A | |
| 2.1.2 | MFA enabled for all users | ☐ Yes ☐ No ☐ Partial | |
| 2.1.3 | MFA required for root/admin accounts | ☐ Yes ☐ No | |
| 2.1.4 | Service accounts have minimum required permissions | ☐ Yes ☐ No ☐ Partial | |
| 2.1.5 | API keys/access keys rotated regularly | ☐ Yes ☐ No | Frequency: |
| 2.1.6 | Unused accounts and keys removed | ☐ Yes ☐ No | |
| 2.1.7 | SSO/federation configured (if applicable) | ☐ Yes ☐ No ☐ N/A | |
| 2.1.8 | Break-glass/emergency access procedures documented | ☐ Yes ☐ No | |

### 2.2 Access Control

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 2.2.1 | Principle of least privilege implemented | ☐ Yes ☐ No ☐ Partial | |
| 2.2.2 | Role-based access control (RBAC) configured | ☐ Yes ☐ No | |
| 2.2.3 | Custom roles reviewed and justified | ☐ Yes ☐ No ☐ N/A | |
| 2.2.4 | Access permissions reviewed periodically | ☐ Yes ☐ No | Frequency: |
| 2.2.5 | Conditional access policies configured | ☐ Yes ☐ No ☐ N/A | |
| 2.2.6 | Privileged Identity Management (PIM) enabled | ☐ Yes ☐ No ☐ N/A | |
| 2.2.7 | Just-in-time access for privileged operations | ☐ Yes ☐ No ☐ N/A | |

---

## Section 3: Network Security

### 3.1 Network Configuration

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.1.1 | Virtual networks/VPCs properly segmented | ☐ Yes ☐ No ☐ N/A | |
| 3.1.2 | Network security groups configured | ☐ Yes ☐ No | |
| 3.1.3 | Inbound rules follow least privilege | ☐ Yes ☐ No ☐ Partial | |
| 3.1.4 | SSH/RDP not exposed to internet (0.0.0.0/0) | ☐ Yes ☐ No | |
| 3.1.5 | Database ports not exposed to internet | ☐ Yes ☐ No | |
| 3.1.6 | Private endpoints used for PaaS services | ☐ Yes ☐ No ☐ Partial | |
| 3.1.7 | VPN or private connectivity for sensitive workloads | ☐ Yes ☐ No ☐ N/A | |
| 3.1.8 | Web Application Firewall (WAF) deployed | ☐ Yes ☐ No ☐ N/A | |
| 3.1.9 | DDoS protection enabled | ☐ Yes ☐ No | |
| 3.1.10 | Egress traffic controlled and monitored | ☐ Yes ☐ No ☐ Partial | |

### 3.2 DNS and Certificates

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.2.1 | DNS records properly configured | ☐ Yes ☐ No | |
| 3.2.2 | SSL/TLS certificates valid and managed | ☐ Yes ☐ No | |
| 3.2.3 | Certificate expiry monitored | ☐ Yes ☐ No | |
| 3.2.4 | HTTPS enforced for web applications | ☐ Yes ☐ No | |
| 3.2.5 | TLS 1.2+ required | ☐ Yes ☐ No | |

---

## Section 4: Data Protection

### 4.1 Encryption

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.1.1 | Encryption at rest enabled for storage | ☐ Yes ☐ No ☐ Partial | |
| 4.1.2 | Encryption at rest enabled for databases | ☐ Yes ☐ No ☐ Partial | |
| 4.1.3 | Customer-managed keys (CMK) used where required | ☐ Yes ☐ No ☐ N/A | |
| 4.1.4 | Key management service properly configured | ☐ Yes ☐ No | |
| 4.1.5 | Key rotation enabled | ☐ Yes ☐ No | Frequency: |
| 4.1.6 | Encryption in transit enforced | ☐ Yes ☐ No ☐ Partial | |

### 4.2 Storage Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.2.1 | Storage accounts not publicly accessible | ☐ Yes ☐ No | |
| 4.2.2 | Blob/object storage permissions reviewed | ☐ Yes ☐ No | |
| 4.2.3 | Soft delete enabled for critical data | ☐ Yes ☐ No | |
| 4.2.4 | Versioning enabled where appropriate | ☐ Yes ☐ No | |
| 4.2.5 | Access logging enabled for storage | ☐ Yes ☐ No | |
| 4.2.6 | Lifecycle policies configured | ☐ Yes ☐ No ☐ N/A | |

### 4.3 Database Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.3.1 | Database encryption enabled | ☐ Yes ☐ No | |
| 4.3.2 | Database firewall rules configured | ☐ Yes ☐ No | |
| 4.3.3 | Database audit logging enabled | ☐ Yes ☐ No | |
| 4.3.4 | Sensitive data discovery/classification used | ☐ Yes ☐ No ☐ N/A | |
| 4.3.5 | Database backups encrypted | ☐ Yes ☐ No | |
| 4.3.6 | Point-in-time restore configured | ☐ Yes ☐ No | Retention: |

---

## Section 5: Compute Security

### 5.1 Virtual Machines

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.1.1 | VM images from trusted sources | ☐ Yes ☐ No | |
| 5.1.2 | OS patches applied regularly | ☐ Yes ☐ No | |
| 5.1.3 | Auto-update enabled where appropriate | ☐ Yes ☐ No ☐ N/A | |
| 5.1.4 | Antimalware/EDR installed | ☐ Yes ☐ No | |
| 5.1.5 | Disk encryption enabled | ☐ Yes ☐ No | |
| 5.1.6 | Instance metadata service secured | ☐ Yes ☐ No ☐ N/A | |
| 5.1.7 | Boot diagnostics enabled | ☐ Yes ☐ No | |
| 5.1.8 | Just-in-time VM access configured | ☐ Yes ☐ No ☐ N/A | |

### 5.2 Containers and Serverless

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.2.1 | Container images scanned for vulnerabilities | ☐ Yes ☐ No ☐ N/A | |
| 5.2.2 | Base images from trusted registries | ☐ Yes ☐ No ☐ N/A | |
| 5.2.3 | Containers run as non-root | ☐ Yes ☐ No ☐ N/A | |
| 5.2.4 | Container registry secured | ☐ Yes ☐ No ☐ N/A | |
| 5.2.5 | Kubernetes/orchestration secured | ☐ Yes ☐ No ☐ N/A | |
| 5.2.6 | Serverless functions use least privilege | ☐ Yes ☐ No ☐ N/A | |
| 5.2.7 | Function secrets properly managed | ☐ Yes ☐ No ☐ N/A | |

---

## Section 6: Logging and Monitoring

### 6.1 Logging Configuration

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 6.1.1 | Cloud audit/activity logging enabled | ☐ Yes ☐ No | |
| 6.1.2 | Logs sent to centralized logging | ☐ Yes ☐ No ☐ Partial | |
| 6.1.3 | Log retention meets requirements | ☐ Yes ☐ No | Retention: |
| 6.1.4 | Logs protected from tampering | ☐ Yes ☐ No | |
| 6.1.5 | Resource logging enabled (network, storage, etc.) | ☐ Yes ☐ No ☐ Partial | |
| 6.1.6 | Application logging configured | ☐ Yes ☐ No | |

### 6.2 Monitoring and Alerting

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 6.2.1 | Security monitoring/SIEM integrated | ☐ Yes ☐ No | |
| 6.2.2 | Alerts configured for security events | ☐ Yes ☐ No ☐ Partial | |
| 6.2.3 | Alerts for unauthorized access attempts | ☐ Yes ☐ No | |
| 6.2.4 | Alerts for configuration changes | ☐ Yes ☐ No | |
| 6.2.5 | Alerts for resource creation/deletion | ☐ Yes ☐ No | |
| 6.2.6 | Budget/cost alerts configured | ☐ Yes ☐ No | |
| 6.2.7 | Cloud security posture management (CSPM) used | ☐ Yes ☐ No ☐ N/A | |

---

## Section 7: Security Services

### 7.1 Native Security Services

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.1.1 | Cloud security center/advisor enabled | ☐ Yes ☐ No | |
| 7.1.2 | Security recommendations reviewed and addressed | ☐ Yes ☐ No ☐ Partial | |
| 7.1.3 | Threat detection service enabled | ☐ Yes ☐ No | |
| 7.1.4 | Vulnerability assessment enabled | ☐ Yes ☐ No | |
| 7.1.5 | Security benchmarks/compliance checked | ☐ Yes ☐ No | |

### 7.2 Secrets Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.2.1 | Secrets stored in vault/secrets manager | ☐ Yes ☐ No | |
| 7.2.2 | No secrets in code or configuration | ☐ Yes ☐ No | |
| 7.2.3 | Secret rotation configured | ☐ Yes ☐ No | |
| 7.2.4 | Access to secrets logged | ☐ Yes ☐ No | |
| 7.2.5 | Secrets access follows least privilege | ☐ Yes ☐ No | |

---

## Section 8: Backup and Recovery

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 8.1 | Backup policies configured | ☐ Yes ☐ No | |
| 8.2 | Critical resources backed up | ☐ Yes ☐ No ☐ Partial | |
| 8.3 | Backup retention meets requirements | ☐ Yes ☐ No | Retention: |
| 8.4 | Backups stored in different region | ☐ Yes ☐ No | |
| 8.5 | Backup restoration tested | ☐ Yes ☐ No | Frequency: |
| 8.6 | Infrastructure as Code backed up | ☐ Yes ☐ No ☐ N/A | |

---

## Section 9: Compliance and Governance

### 9.1 Resource Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 9.1.1 | Resource tagging policy implemented | ☐ Yes ☐ No ☐ Partial | |
| 9.1.2 | Resources tagged with owner/cost center | ☐ Yes ☐ No | |
| 9.1.3 | Unused resources identified and removed | ☐ Yes ☐ No | |
| 9.1.4 | Resource locks on critical resources | ☐ Yes ☐ No | |
| 9.1.5 | Policies/guardrails configured | ☐ Yes ☐ No ☐ Partial | |

### 9.2 Compliance

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 9.2.1 | Data residency requirements met | ☐ Yes ☐ No ☐ N/A | |
| 9.2.2 | Industry compliance requirements addressed | ☐ Yes ☐ No ☐ N/A | |
| 9.2.3 | Compliance reports available from provider | ☐ Yes ☐ No | |
| 9.2.4 | Regular compliance assessments performed | ☐ Yes ☐ No | |

---

## Section 10: DevOps Security (if applicable)

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 10.1 | Infrastructure as Code (IaC) scanned | ☐ Yes ☐ No ☐ N/A | |
| 10.2 | CI/CD pipelines secured | ☐ Yes ☐ No ☐ N/A | |
| 10.3 | Pipeline secrets properly managed | ☐ Yes ☐ No ☐ N/A | |
| 10.4 | Deployment requires approval for production | ☐ Yes ☐ No ☐ N/A | |
| 10.5 | Source code repositories secured | ☐ Yes ☐ No ☐ N/A | |
| 10.6 | Branch protection enabled | ☐ Yes ☐ No ☐ N/A | |

---

## Section 11: Assessment Summary

### 11.1 Scoring

| Domain | Weight | Score (1-5) | Weighted Score |
|--------|--------|-------------|----------------|
| Identity & Access | 20% | | |
| Network Security | 15% | | |
| Data Protection | 20% | | |
| Compute Security | 15% | | |
| Logging & Monitoring | 15% | | |
| Backup & Recovery | 10% | | |
| Governance | 5% | | |
| **Total** | **100%** | | |

### 11.2 Critical Findings

| # | Finding | Severity | Remediation |
|---|---------|----------|-------------|
| 1 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 2 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 3 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |

### 11.3 Recommendations

| Priority | Recommendation | Owner | Target Date |
|----------|----------------|-------|-------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Assessor | | | |
| Cloud Admin | | | |
| Security Manager | | | |

---

[Back to Checklists](./README.md) | [Back to Home](../README.md)

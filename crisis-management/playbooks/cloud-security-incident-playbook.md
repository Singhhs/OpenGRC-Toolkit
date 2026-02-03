# Cloud Security Incident Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., Cloud Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides guidance for responding to security incidents in cloud environments (AWS, Azure, GCP, and other cloud platforms) at [ORGANIZATION NAME].

### Scenarios Covered
- Compromised cloud credentials/accounts
- Cloud resource misconfiguration exploitation
- Unauthorized resource deployment (cryptomining, etc.)
- Data exposure via misconfigured storage
- Cloud-based malware or backdoors
- Lateral movement within cloud environment
- Cloud service abuse
- API key compromise

### Cloud-Specific Considerations

Cloud incidents differ from traditional incidents:
- **Shared responsibility** - Know what you control vs. provider
- **API-driven** - All actions logged, attackers use APIs too
- **Ephemeral resources** - Evidence can disappear quickly
- **Global scope** - Incidents can span regions instantly
- **Scalability** - Attackers can rapidly scale their access
- **Billing impact** - Unauthorized usage creates immediate costs

---

## 2. Detection Indicators

### 2.1 Identity and Access Indicators

| Indicator | Description |
|-----------|-------------|
| Root/admin account usage | Unexpected use of highly privileged accounts |
| Impossible travel | Console logins from geographically distant locations |
| Unusual login times | Access outside normal business hours |
| MFA bypass or removal | MFA disabled or circumvented |
| New IAM users/roles | Unauthorized identity creation |
| Privilege escalation | Users gaining unexpected permissions |
| Access key usage anomalies | Keys used from unexpected locations |
| Failed authentication spikes | Brute force or credential stuffing |

### 2.2 Resource and Configuration Indicators

| Indicator | Description |
|-----------|-------------|
| New resources in unusual regions | Compute deployed where you don't operate |
| High-powered instances | GPU or high-CPU instances for cryptomining |
| Modified security groups | Firewall rules opened unexpectedly |
| Public S3/storage buckets | Storage exposed to internet |
| Modified IAM policies | Permission changes |
| Disabled logging | CloudTrail/audit logs disabled |
| New network configurations | VPC peering, VPN, or routing changes |
| Lambda/function changes | Serverless code modified |

### 2.3 Data and Network Indicators

| Indicator | Description |
|-----------|-------------|
| Large data transfers | Unusual egress to external destinations |
| Snapshot sharing | AMIs/snapshots shared externally |
| Database exports | RDS snapshots or exports created |
| Cross-account access | Resources shared with unknown accounts |
| Unusual API calls | High volume or suspicious API activity |
| Data exfiltration patterns | Systematic access to sensitive data |

### 2.4 Billing Indicators

| Indicator | Description |
|-----------|-------------|
| Unexpected cost spike | Sudden increase in cloud spending |
| New service usage | Services you don't normally use |
| Usage in new regions | Costs from unexpected regions |
| Reserved instance purchases | Unauthorized commitments |

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Root/admin account compromised, active data exfiltration, production systems impacted, widespread access | Immediate, all hands |
| **P2 High** | Privileged account compromised, sensitive data exposed, multiple resources affected | Priority response |
| **P3 Medium** | Limited account compromise, misconfiguration exploited, contained scope | Standard response |
| **P4 Low** | Minor misconfiguration, no data exposure, quickly contained | Normal process |

### Escalation Triggers

Escalate to P1 if:
- Root or organization admin account compromised
- Customer data confirmed exposed
- Production workloads impacted
- Attacker has persistent access mechanisms
- Billing/financial fraud occurring
- Attack spreading across accounts

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Incident Commander | Overall coordination | [NAME/PHONE] |
| Cloud Security Lead | Cloud investigation, containment | [NAME/PHONE] |
| Cloud Platform Team | Resource management, access | [NAME/PHONE] |
| Security Operations | Monitoring, detection | [NAME/PHONE] |
| Identity Team | Credential management | [NAME/PHONE] |
| Legal/Privacy | If data breach | [NAME/PHONE] |
| Finance | If billing impact | [NAME/PHONE] |
| Cloud Provider Support | Escalation if needed | [SUPPORT CONTACT] |

---

## 5. Immediate Actions (First 30 Minutes)

### 5.1 Confirm and Assess

```
□ Step 1: Verify the incident
  □ Review alerting source (SIEM, CSPM, CloudTrail, etc.)
  □ Confirm suspicious activity is not authorized
  □ Identify affected cloud account(s)
  □ Identify affected resources
  □ Determine initial scope

□ Step 2: Initial assessment
  □ Which cloud platform(s) affected?
  □ What type of compromise (credentials, config, etc.)?
  □ Is the attack ongoing or historical?
  □ What data/systems are at risk?
  □ What is the potential business impact?
```

### 5.2 Preserve Evidence

```
□ Step 3: Ensure logging is intact (CRITICAL - do this first)

  AWS:
  □ Verify CloudTrail is enabled and logging
  □ Check CloudTrail logs haven't been deleted
  □ Verify S3 access logging if storage involved
  □ Check VPC Flow Logs status

  Azure:
  □ Verify Azure Activity Log retention
  □ Check Azure AD sign-in logs
  □ Verify diagnostic settings

  GCP:
  □ Verify Cloud Audit Logs enabled
  □ Check Admin Activity logs
  □ Verify Data Access logs if enabled

□ Step 4: Export critical logs immediately
  □ Export last 24-72 hours of audit logs
  □ Export IAM/identity logs
  □ Export affected resource logs
  □ Store in secure, separate location
```

### 5.3 Initial Containment Decision

```
□ Step 5: Decide on immediate containment

  For Compromised Credentials:
  □ Disable compromised access keys immediately
  □ Revoke active sessions
  □ Do NOT delete the user yet (preserve for investigation)

  For Compromised Resources:
  □ Isolate resource (modify security groups)
  □ Do NOT terminate yet (preserve for forensics)
  □ Snapshot instances before any changes

  For Active Data Exfiltration:
  □ Revoke public access immediately
  □ Block suspicious IPs at network level
  □ Disable compromised credentials
```

---

## 6. Containment

### 6.1 Credential Compromise Containment

```
□ Step 6: Contain compromised identities

  For IAM Users:
  □ Disable all access keys for the user
  □ Disable console password
  □ Remove from all groups (preserve group list first)
  □ Attach explicit deny policy
  □ Revoke active sessions

  For IAM Roles:
  □ Modify trust policy to prevent assumption
  □ Attach explicit deny policy
  □ Update role session duration to minimum
  □ Revoke existing sessions

  For Root Account:
  □ Change root password immediately
  □ Rotate root access keys (if any exist, delete them)
  □ Enable/reset MFA
  □ Review and remove root account access keys
  □ Contact cloud provider support

  For Service Accounts/Principals:
  □ Rotate credentials/secrets
  □ Review and restrict permissions
  □ Check for unauthorized usage
```

### 6.2 Resource Containment

```
□ Step 7: Contain affected resources

  Compute Instances:
  □ Snapshot the instance (evidence preservation)
  □ Modify security group to isolate (deny all inbound/outbound)
  □ Do NOT terminate until investigation complete
  □ If must terminate, snapshot first

  Storage (S3/Blob/GCS):
  □ Remove public access
  □ Block public access at account level
  □ Review and revoke bucket policies
  □ Enable versioning if not enabled
  □ Check for data exfiltration in logs

  Databases:
  □ Remove public accessibility
  □ Modify security groups to restrict access
  □ Create snapshot for forensics
  □ Rotate database credentials

  Serverless (Lambda/Functions):
  □ Disable the function
  □ Preserve function code and configuration
  □ Review execution logs
  □ Check for unauthorized invocations
```

### 6.3 Network Containment

```
□ Step 8: Network-level containment

  □ Update NACLs to block suspicious IPs
  □ Modify security groups to restrict access
  □ Review and remove unauthorized VPC peering
  □ Check for unauthorized VPN connections
  □ Review route tables for modifications
  □ Check for unauthorized load balancers or endpoints
```

### 6.4 Stop Billing Impact

```
□ Step 9: Address unauthorized resource usage

  □ Identify all unauthorized resources
  □ Terminate cryptomining or other abuse resources
  □ Cancel any unauthorized reserved instances
  □ Set up billing alerts if not present
  □ Contact cloud provider about fraudulent charges
```

---

## 7. Investigation

### 7.1 Log Analysis

```
□ Step 10: Analyze cloud audit logs

  Key Questions:
  □ When did unauthorized access begin?
  □ What credentials were used?
  □ From what IP addresses?
  □ What actions were taken?
  □ What resources were created/modified?
  □ Was data accessed or exfiltrated?

  AWS CloudTrail Analysis:
  □ Filter by compromised user/role
  □ Look for ConsoleLogin events
  □ Check CreateUser, CreateAccessKey events
  □ Review AssumeRole events
  □ Check S3 GetObject/PutObject for data access
  □ Look for EC2 RunInstances in unusual regions

  Azure Activity Log Analysis:
  □ Filter by compromised principal
  □ Review sign-in logs for location/device
  □ Check role assignments
  □ Review resource creation events

  GCP Audit Log Analysis:
  □ Filter by compromised account
  □ Review Admin Activity logs
  □ Check IAM policy changes
  □ Review Data Access logs if enabled
```

### 7.2 Determine Attack Vector

```
□ Step 11: Identify how access was gained

  Common Cloud Attack Vectors:
  □ Phished credentials
  □ Leaked access keys (GitHub, etc.)
  □ Credential stuffing
  □ Exploited application vulnerability (SSRF, etc.)
  □ Metadata service exploitation (IMDSv1)
  □ Misconfigured resource (public bucket, etc.)
  □ Compromised CI/CD pipeline
  □ Third-party integration compromise
  □ Insider threat

  Investigation:
  □ Check for access keys in public repositories
  □ Review how compromised credentials were issued
  □ Check for application vulnerabilities (SSRF)
  □ Review instance metadata access patterns
  □ Check third-party OAuth app permissions
```

### 7.3 Assess Data Impact

```
□ Step 12: Determine data exposure

  □ What storage was accessible?
  □ What data was accessed (check access logs)?
  □ Was data downloaded or exfiltrated?
  □ What databases were accessible?
  □ What queries were run?
  □ Were snapshots created or shared?
  □ Was data copied to external accounts?

  If Data Breach Confirmed:
  → Follow Data Breach Playbook
  → Engage Legal and Privacy
  → Assess notification requirements
```

### 7.4 Check for Persistence

```
□ Step 13: Look for persistence mechanisms

  IAM Persistence:
  □ New IAM users created
  □ New access keys on existing users
  □ New roles with external trust
  □ Modified assume role policies
  □ Backdoor policies attached

  Resource Persistence:
  □ New EC2 instances (backdoors)
  □ Modified Lambda functions
  □ New scheduled tasks/automation
  □ Modified startup scripts/user data
  □ New AMIs or snapshots shared

  Network Persistence:
  □ New VPC peering connections
  □ New VPN or Direct Connect
  □ Modified DNS settings
  □ New load balancers or endpoints
```

---

## 8. Eradication

### 8.1 Remove Unauthorized Access

```
□ Step 14: Eliminate attacker access

  Credentials:
  □ Delete all unauthorized IAM users
  □ Delete unauthorized access keys
  □ Remove unauthorized roles
  □ Remove backdoor policies
  □ Rotate all potentially exposed credentials
  □ Rotate all secrets in Secrets Manager/Key Vault

  Resources:
  □ Terminate unauthorized compute resources
  □ Delete unauthorized storage
  □ Remove unauthorized network resources
  □ Delete unauthorized snapshots/AMIs
  □ Remove unauthorized Lambda functions
```

### 8.2 Restore Secure Configuration

```
□ Step 15: Fix vulnerabilities and misconfigurations

  □ Enable MFA on all privileged accounts
  □ Review and restrict IAM policies (least privilege)
  □ Enable account-level public access blocks
  □ Review and tighten security groups
  □ Enable IMDSv2 on EC2 instances
  □ Review and fix CSPM findings
  □ Enable GuardDuty/Security Center/SCC
  □ Review third-party integrations
```

### 8.3 Credential Rotation

```
□ Step 16: Comprehensive credential rotation

  Rotate:
  □ All IAM user passwords
  □ All access keys (delete and recreate)
  □ All application secrets
  □ Database passwords
  □ API keys
  □ Service account credentials
  □ SSH keys if used
  □ Any credentials that may have been exposed
```

---

## 9. Recovery

### 9.1 Restore Normal Operations

```
□ Step 17: Restore services

  □ Verify all unauthorized access removed
  □ Restore legitimate access
  □ Re-enable services that were disabled
  □ Restore network connectivity
  □ Verify applications functioning
  □ Restore from clean backups if needed
  □ Update and redeploy applications if compromised
```

### 9.2 Enhanced Monitoring

```
□ Step 18: Implement enhanced monitoring

  Enable/Configure:
  □ CloudTrail logging to secure bucket
  □ GuardDuty / Security Center / SCC
  □ VPC Flow Logs
  □ S3 access logging
  □ Database activity monitoring
  □ SIEM integration for cloud logs
  □ Billing alerts and anomaly detection
  □ CSPM tool monitoring

  Create Alerts For:
  □ Root account usage
  □ IAM changes
  □ Security group changes
  □ Public access changes
  □ New regions usage
  □ High API call volumes
  □ Failed authentication
```

---

## 10. Communication

### 10.1 Internal Communication

| Audience | When | Content |
|----------|------|---------|
| Executive team | P1/P2 immediately | Business impact, response status |
| Cloud/IT teams | Immediately | Technical details, required actions |
| Application owners | If their resources affected | Impact and recovery timeline |
| Finance | If billing impact | Cost impact and recovery |
| Legal | If data breach | Regulatory implications |

### 10.2 External Communication

| Audience | When | Owner |
|----------|------|-------|
| Cloud provider | If assistance needed | Cloud team |
| Customers | If their data affected | Legal + Communications |
| Regulators | If required | Legal |
| Law enforcement | If criminal activity | Legal |

### 10.3 Cloud Provider Escalation

**When to Contact Provider:**
- Root/organization account compromise
- Suspected provider-side vulnerability
- Need log data beyond retention
- Disputing fraudulent charges
- Need emergency support

**AWS:** Open Security case in Support Center
**Azure:** Open Security incident in Azure Portal
**GCP:** Contact Cloud Support with Security priority

---

## 11. Post-Incident

### 11.1 Documentation

```
□ Step 19: Complete documentation

  Document:
  □ Complete incident timeline
  □ Attack vector and root cause
  □ All affected accounts and resources
  □ Data exposure assessment
  □ Actions taken
  □ Evidence preserved
  □ Business and billing impact
  □ Lessons learned
```

### 11.2 Post-Incident Review

```
□ Step 20: Conduct review (within 1 week)

  Review Questions:
  □ How did the attacker gain initial access?
  □ Why wasn't this detected earlier?
  □ What controls failed or were missing?
  □ Was our response effective?
  □ What would we do differently?
  □ What additional controls are needed?
```

### 11.3 Improvements

```
□ Step 21: Implement improvements

  Consider:
  □ Enhanced identity controls (MFA everywhere)
  □ Least privilege review
  □ CSPM tool deployment
  □ Improved detection rules
  □ Security group/network review
  □ Public access controls
  □ Secrets management improvement
  □ Cloud security training
  □ Automated remediation
```

---

## 12. Cloud-Specific Response Quick Reference

### 12.1 AWS Quick Actions

| Scenario | Immediate Action |
|----------|------------------|
| Compromised IAM User | `aws iam update-login-profile --user-name X --no-password-reset-required` then disable keys |
| Compromised Access Key | `aws iam update-access-key --access-key-id X --status Inactive --user-name Y` |
| Compromised Role | Modify trust policy, attach deny-all policy |
| Root Account Compromise | Change password, rotate keys, enable MFA, contact AWS |
| Public S3 Bucket | `aws s3api put-public-access-block --bucket X --public-access-block-configuration BlockPublicAcls=true...` |
| Suspicious EC2 | Snapshot then isolate security group |

### 12.2 Azure Quick Actions

| Scenario | Immediate Action |
|----------|------------------|
| Compromised User | Disable user in Azure AD, revoke sessions |
| Compromised Service Principal | Remove credentials, disable if possible |
| Compromised Subscription | Remove compromised access, review RBAC |
| Public Storage | Set container access to Private |
| Suspicious VM | Create snapshot, modify NSG to block |

### 12.3 GCP Quick Actions

| Scenario | Immediate Action |
|----------|------------------|
| Compromised User | Suspend user in Admin Console |
| Compromised Service Account | Disable service account, delete keys |
| Public GCS Bucket | Remove allUsers/allAuthenticatedUsers |
| Suspicious Instance | Create snapshot, modify firewall rules |

---

## 13. Prevention Reference

### 13.1 Cloud Security Controls

| Control | Purpose |
|---------|---------|
| MFA everywhere | Prevent credential-based compromise |
| No root/admin access keys | Eliminate highest-risk credentials |
| Least privilege IAM | Minimize blast radius |
| CSPM tool | Detect misconfigurations |
| GuardDuty/Security Center | Detect threats |
| Block public access (account level) | Prevent accidental exposure |
| VPC Flow Logs | Network visibility |
| CloudTrail to secure bucket | Tamper-proof audit trail |
| SCPs/Guardrails | Prevent dangerous actions |
| Secrets management | Secure credential storage |

### 13.2 Cloud Security Checklist

- [ ] MFA enabled on all users
- [ ] No long-lived access keys (use roles)
- [ ] Root account secured with MFA, no access keys
- [ ] CloudTrail/audit logging enabled
- [ ] Logs sent to secure, separate bucket/project
- [ ] GuardDuty/Security Center enabled
- [ ] Account-level public access blocks
- [ ] CSPM tool monitoring
- [ ] Billing alerts configured
- [ ] Break-glass procedures documented
- [ ] Regular IAM access reviews

---

## 14. Related Documents

- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Cloud Security Checklist](../../checklists/cloud-security-checklist.md)
- [Account Compromise Playbook](./account-compromise-playbook.md)
- [Data Breach Playbook](./data-breach-playbook.md)
- [Third-Party Breach Playbook](./third-party-breach-playbook.md)

---

## 15. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

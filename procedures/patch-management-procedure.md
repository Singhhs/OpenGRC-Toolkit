# Patch Management Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Operations Manager] |
| **Approved By** | [ROLE - e.g., CISO / IT Director] |
| **Related Policy** | [Vulnerability Management Policy](../policies/vulnerability-management-policy.md) |

---

## 1. Purpose

This procedure defines the process for identifying, evaluating, testing, and deploying security patches and updates to protect [ORGANIZATION NAME] systems from known vulnerabilities.

## 2. Scope

This procedure applies to:
- All servers (physical and virtual)
- All workstations and laptops
- Network devices (routers, switches, firewalls)
- Security appliances
- Applications and databases
- Cloud infrastructure
- Mobile devices

## 3. Definitions

| Term | Definition |
|------|------------|
| **Patch** | Software update that fixes bugs, vulnerabilities, or adds features |
| **Hotfix** | Emergency patch for critical issues |
| **Service Pack** | Collection of updates bundled together |
| **Zero-Day** | Vulnerability with no available patch |
| **CVE** | Common Vulnerabilities and Exposures identifier |
| **CVSS** | Common Vulnerability Scoring System |

## 4. Patch Classification

### 4.1 Severity Levels

| Severity | CVSS Score | Description | Deployment Timeline |
|----------|------------|-------------|---------------------|
| **Critical** | 9.0 - 10.0 | Actively exploited or imminent threat | Within 72 hours |
| **High** | 7.0 - 8.9 | Significant risk, exploit likely | Within 7 days |
| **Medium** | 4.0 - 6.9 | Moderate risk | Within 30 days |
| **Low** | 0.1 - 3.9 | Limited risk | Within 90 days |

### 4.2 System Classification

| Tier | Systems | Patch Window | Testing Required |
|------|---------|--------------|------------------|
| **Tier 1** | Production critical systems | Scheduled maintenance window | Full testing |
| **Tier 2** | Production non-critical | Extended window | Standard testing |
| **Tier 3** | Development/Test | Flexible | Minimal testing |
| **Tier 4** | Isolated/Air-gapped | Manual process | Per system requirements |

## 5. Procedure

### 5.1 Patch Identification

**Step 1: Monitor for New Patches**

Sources to monitor:
- [ ] Vendor security bulletins (Microsoft, Oracle, etc.)
- [ ] CVE databases (NVD, MITRE)
- [ ] Security mailing lists (US-CERT, vendor lists)
- [ ] Vulnerability scanning results
- [ ] Threat intelligence feeds
- [ ] CISA Known Exploited Vulnerabilities catalog

**Step 2: Document New Patches**

For each patch, record:
| Field | Information |
|-------|-------------|
| Patch ID | Vendor identifier |
| CVE(s) | Associated vulnerabilities |
| CVSS Score | Severity rating |
| Affected Systems | Products/versions impacted |
| Release Date | When patch was released |
| Vendor Recommendation | Vendor guidance |

### 5.2 Patch Assessment

**Step 3: Assess Applicability**

Determine:
- Which systems are affected
- Current patch status of those systems
- Dependencies and prerequisites
- Potential conflicts

**Step 4: Prioritize Patches**

Consider:
- Severity (CVSS score)
- Exploitability (active exploits in wild)
- System criticality
- Exposure (internet-facing vs internal)
- Compensating controls in place

**Step 5: Risk Assessment**

For each applicable patch:
```
Risk = (Vulnerability Severity) × (System Criticality) × (Exposure)
```

Document decision:
- [ ] Apply immediately (emergency)
- [ ] Apply in next maintenance window
- [ ] Schedule for regular cycle
- [ ] Defer with compensating controls
- [ ] Accept risk (with approval)

### 5.3 Patch Testing

**Step 6: Prepare Test Environment**

- Ensure test environment mirrors production
- Create system backups/snapshots
- Document current configuration

**Step 7: Test Patch**

| Test Type | Description | Required For |
|-----------|-------------|--------------|
| Installation test | Verify patch installs correctly | All patches |
| Functionality test | Verify systems work after patch | Tier 1, Tier 2 |
| Regression test | Verify no new issues introduced | Tier 1 |
| Rollback test | Verify patch can be removed | Critical systems |
| Performance test | Verify no performance degradation | High-load systems |

**Step 8: Document Test Results**

Record:
- Test date and tester
- Environment tested
- Test cases executed
- Results (pass/fail)
- Issues discovered
- Recommendation (proceed/do not proceed)

### 5.4 Patch Approval

**Step 9: Obtain Approval**

| Patch Type | Approver | Process |
|------------|----------|---------|
| Emergency/Critical | IT Director + CISO | Expedited approval |
| Standard | Change Advisory Board | Normal change process |
| Low risk | IT Operations Manager | Delegated approval |

**Step 10: Create Change Request**

Follow [Change Management Procedure](./change-management-procedure.md):
- Document patch details
- Specify deployment plan
- Include rollback plan
- Identify affected systems
- Schedule maintenance window

### 5.5 Patch Deployment

**Step 11: Pre-Deployment Preparation**

- [ ] Notify stakeholders of maintenance window
- [ ] Create system backups/snapshots
- [ ] Verify rollback procedure
- [ ] Confirm deployment tools ready
- [ ] Stage patch files
- [ ] Prepare monitoring dashboards

**Step 12: Deploy Patches**

Deployment methods:

| Method | Use Case |
|--------|----------|
| WSUS/SCCM | Windows servers and workstations |
| Ansible/Puppet/Chef | Linux/Unix systems |
| Vendor tools | Network devices, applications |
| Manual | Isolated systems, special cases |
| Cloud native | AWS SSM, Azure Update Management |

**Deployment sequence:**
1. Deploy to pilot group (5-10% of systems)
2. Monitor for 2-4 hours
3. If successful, deploy to remaining systems in waves
4. Monitor throughout deployment

**Step 13: Verify Deployment**

- [ ] Confirm patch installed successfully
- [ ] Verify system functionality
- [ ] Check application availability
- [ ] Review error logs
- [ ] Update asset inventory

### 5.6 Post-Deployment

**Step 14: Monitor for Issues**

For 24-48 hours after deployment:
- Monitor system health
- Review help desk tickets
- Check application performance
- Watch for unexpected behavior

**Step 15: Handle Failures**

If issues occur:
1. Assess severity of issue
2. Determine if rollback needed
3. Execute rollback if necessary
4. Document incident
5. Investigate root cause
6. Plan remediation

**Step 16: Documentation**

Update records:
- [ ] Asset inventory (patch status)
- [ ] Change management records
- [ ] Vulnerability tracking
- [ ] Compliance reports

### 5.7 Exception Handling

**Step 17: Document Exceptions**

For systems that cannot be patched:

| Field | Information Required |
|-------|---------------------|
| System | Affected system(s) |
| Patch | Patch that cannot be applied |
| Reason | Technical/business justification |
| Risk | Assessment of unpatched risk |
| Compensating Controls | Mitigations in place |
| Review Date | When to reassess |
| Approval | Risk owner sign-off |

Compensating controls may include:
- Network segmentation
- Enhanced monitoring
- Application whitelisting
- Web application firewall
- IPS signatures
- Access restrictions

## 6. Emergency Patching

For critical vulnerabilities with active exploitation:

### 6.1 Emergency Process

1. **Immediate notification** to IT Security and IT Operations
2. **Emergency assessment** (within 2 hours)
3. **Abbreviated testing** (critical function only)
4. **Emergency approval** (verbal, documented after)
5. **Immediate deployment** to critical/exposed systems
6. **Continuous monitoring** during and after
7. **Post-incident review** within 1 week

### 6.2 Emergency Contacts

| Role | Contact | Backup |
|------|---------|--------|
| IT Security Lead | [NAME/PHONE] | [NAME/PHONE] |
| IT Operations Lead | [NAME/PHONE] | [NAME/PHONE] |
| Change Manager | [NAME/PHONE] | [NAME/PHONE] |
| IT Director | [NAME/PHONE] | [NAME/PHONE] |

## 7. Patch Metrics

Track and report:

| Metric | Target | Frequency |
|--------|--------|-----------|
| Critical patches within SLA | 100% | Monthly |
| High patches within SLA | 95% | Monthly |
| Systems fully patched | >95% | Monthly |
| Patch-related incidents | <2% | Monthly |
| Mean time to patch (critical) | <72 hours | Monthly |
| Patch exceptions | <5% of systems | Quarterly |

## 8. Roles and Responsibilities

### 8.1 IT Security
- Monitor vulnerability sources
- Assess patch criticality
- Approve security aspects
- Track compliance

### 8.2 IT Operations
- Test and deploy patches
- Maintain patching tools
- Execute rollbacks
- Report deployment status

### 8.3 System Owners
- Approve maintenance windows
- Accept risks for exceptions
- Validate system functionality

### 8.4 Change Management
- Coordinate change approvals
- Schedule maintenance windows
- Track change records

## 9. Tools

| Purpose | Tool(s) |
|---------|---------|
| Vulnerability scanning | [e.g., Nessus, Qualys, Rapid7] |
| Windows patching | [e.g., WSUS, SCCM, Intune] |
| Linux patching | [e.g., Ansible, Satellite, Landscape] |
| Patch reporting | [e.g., ServiceNow, Jira] |
| Asset inventory | [e.g., CMDB, asset management tool] |

## 10. Related Documents

- [Vulnerability Management Policy](../policies/vulnerability-management-policy.md)
- [Change Management Policy](../policies/change-management-policy.md)
- [Change Management Procedure](./change-management-procedure.md)
- [Incident Response Procedure](./incident-response-procedure.md)
- [Asset Inventory Template](../risk-assessment/templates/asset-inventory-template.md)

## 11. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

# Vendor Security Assessment Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager / Procurement Manager] |
| **Approved By** | [ROLE - e.g., CISO] |
| **Related Policy** | [Supplier Security Policy](../policies/supplier-security-policy.md) |

---

## 1. Purpose

This procedure defines the process for assessing the security posture of vendors, suppliers, and third parties before and during engagement to manage supply chain security risks at [ORGANIZATION NAME].

## 2. Scope

This procedure applies to:
- All new vendor engagements
- Vendor contract renewals
- Existing vendors (periodic reassessment)
- Vendors with access to company data or systems
- Cloud service providers
- Software vendors
- Outsourced service providers
- Consultants and contractors

## 3. Vendor Risk Classification

### 3.1 Risk Tiers

| Tier | Criteria | Assessment Level |
|------|----------|------------------|
| **Critical** | Access to restricted data, critical systems, or large-scale processing | Full assessment + onsite audit |
| **High** | Access to confidential data or significant systems | Full assessment |
| **Medium** | Access to internal data or limited systems | Standard assessment |
| **Low** | No data access, non-critical services | Basic assessment |

### 3.2 Classification Factors

Score each factor (1-5) to determine tier:

| Factor | Description |
|--------|-------------|
| Data sensitivity | Classification of data vendor will access |
| Data volume | Amount of data processed |
| System access | Level of access to company systems |
| Business criticality | Impact if vendor fails |
| Regulatory scope | Compliance requirements involved |
| Integration depth | How deeply integrated with operations |

**Scoring:**
- Total 25-30: Critical
- Total 18-24: High
- Total 10-17: Medium
- Total 6-9: Low

## 4. Procedure

### 4.1 Pre-Assessment

**Step 1: Initiate Assessment Request**

Requester provides:
- [ ] Vendor name and contact information
- [ ] Description of services/products
- [ ] Data types to be shared
- [ ] Systems vendor will access
- [ ] Contract value and duration
- [ ] Business justification

**Step 2: Determine Risk Tier**

Security team:
- Reviews request details
- Applies classification factors
- Assigns risk tier
- Determines assessment scope

**Step 3: Notify Vendor**

Send to vendor:
- Assessment requirements notification
- Security questionnaire (based on tier)
- Documentation requests
- Timeline expectations

### 4.2 Documentation Collection

**Step 4: Request Documentation**

| Document | Critical | High | Medium | Low |
|----------|----------|------|--------|-----|
| Security questionnaire | ✓ | ✓ | ✓ | ✓ |
| Information security policy | ✓ | ✓ | ✓ | |
| SOC 2 Type II report | ✓ | ✓ | | |
| ISO 27001 certificate | ✓ | ✓ | | |
| Penetration test summary | ✓ | ✓ | | |
| Business continuity plan | ✓ | ✓ | | |
| Insurance certificates | ✓ | ✓ | ✓ | |
| Data processing agreement | ✓ | ✓ | ✓ | |
| Subcontractor list | ✓ | ✓ | | |
| Incident response plan | ✓ | | | |

**Step 5: Send Security Questionnaire**

Use [Vendor Security Questionnaire](../templates/vendor-security-questionnaire.md)

Set deadline for response:
- Critical/High: 10 business days
- Medium/Low: 15 business days

### 4.3 Assessment Review

**Step 6: Review Questionnaire Responses**

Evaluate responses against requirements:

| Domain | Key Areas to Review |
|--------|---------------------|
| **Governance** | Policies, roles, management commitment |
| **Access Control** | Authentication, authorization, access reviews |
| **Data Protection** | Encryption, classification, handling |
| **Network Security** | Segmentation, monitoring, firewalls |
| **Endpoint Security** | Antivirus, patching, hardening |
| **Incident Response** | Detection, response, notification |
| **Business Continuity** | Backup, recovery, resilience |
| **HR Security** | Background checks, training, termination |
| **Physical Security** | Facility access, environmental controls |
| **Compliance** | Certifications, audits, regulations |

**Step 7: Review Supporting Documentation**

For each document:
- Verify authenticity (check certificate validity, report dates)
- Check scope covers relevant services
- Note any exceptions or qualifications
- Identify gaps or concerns

**Step 8: Identify Gaps and Risks**

Document findings:

| Finding ID | Domain | Description | Risk Level | Remediation Required |
|------------|--------|-------------|------------|---------------------|
| F-001 | Example | Example finding | High/Med/Low | Yes/No |

### 4.4 Additional Assessment Activities

**Step 9: Conduct Additional Reviews (as needed)**

| Activity | When Required |
|----------|---------------|
| Technical review call | Clarify questionnaire responses |
| Reference check | New critical vendors |
| Onsite audit | Critical tier vendors |
| Penetration test review | Vendors with system access |
| Architecture review | Deep integrations |

**Step 10: Onsite Audit (Critical Tier)**

If required, conduct onsite assessment:
- Physical security review
- Data center inspection
- Process observation
- Staff interviews
- Evidence collection

### 4.5 Risk Assessment

**Step 11: Calculate Vendor Risk Score**

| Category | Weight | Score (1-5) | Weighted |
|----------|--------|-------------|----------|
| Security governance | 15% | | |
| Access control | 15% | | |
| Data protection | 20% | | |
| Technical security | 15% | | |
| Incident response | 10% | | |
| Business continuity | 10% | | |
| Compliance | 15% | | |
| **Total** | 100% | | |

**Risk Rating:**
- 4.0-5.0: Low Risk (Approve)
- 3.0-3.9: Medium Risk (Approve with conditions)
- 2.0-2.9: High Risk (Remediation required)
- 1.0-1.9: Critical Risk (Do not approve)

**Step 12: Document Risk Assessment**

Create vendor risk assessment report including:
- Executive summary
- Assessment scope and methodology
- Findings and gaps
- Risk rating
- Recommendations
- Remediation requirements

### 4.6 Decision and Approval

**Step 13: Make Recommendation**

| Risk Level | Recommendation |
|------------|----------------|
| Low | Approve engagement |
| Medium | Approve with security requirements |
| High | Approve only with remediation plan |
| Critical | Do not approve / escalate to CISO |

**Step 14: Obtain Approval**

| Vendor Tier | Approver |
|-------------|----------|
| Critical | CISO + Business Executive |
| High | CISO or IT Security Manager |
| Medium | IT Security Manager |
| Low | Security Analyst |

**Step 15: Communicate Decision**

Notify:
- Requesting business unit
- Procurement
- Vendor (if remediation required)
- Legal (contract requirements)

### 4.7 Remediation (if required)

**Step 16: Define Remediation Requirements**

For each finding requiring remediation:
- Specific action required
- Acceptance criteria
- Timeline for completion
- Evidence required

**Step 17: Track Remediation**

- Monitor vendor progress
- Request evidence of completion
- Verify remediation effectiveness
- Update risk assessment

### 4.8 Contract Requirements

**Step 18: Define Security Contract Terms**

Ensure contracts include:
- [ ] Data protection requirements
- [ ] Security standards to maintain
- [ ] Right to audit
- [ ] Breach notification requirements
- [ ] Subcontractor restrictions
- [ ] Data return/destruction on termination
- [ ] Insurance requirements
- [ ] Liability provisions
- [ ] Compliance certifications required

See [Supplier Security Policy](../policies/supplier-security-policy.md) for standard terms.

### 4.9 Ongoing Monitoring

**Step 19: Schedule Reassessment**

| Vendor Tier | Reassessment Frequency |
|-------------|------------------------|
| Critical | Annually |
| High | Every 18 months |
| Medium | Every 2 years |
| Low | Every 3 years or contract renewal |

**Step 20: Continuous Monitoring**

Monitor between assessments:
- Security rating services (BitSight, SecurityScorecard)
- News and breach notifications
- SOC report updates
- Certificate renewals
- Significant vendor changes

## 5. Assessment Triggers

Conduct assessment when:
- New vendor engagement
- Contract renewal
- Significant scope change
- Security incident at vendor
- Material change in vendor ownership
- New regulatory requirements
- Significant security rating change

## 6. Expedited Assessment

For urgent business needs:

**Expedited Process:**
1. Business justification for urgency
2. CISO approval to expedite
3. Abbreviated questionnaire
4. Focus on critical controls
5. Conditional approval with full assessment to follow
6. Enhanced monitoring until complete

**Maximum expedited approval:** 90 days conditional

## 7. Records

Maintain for each vendor:
- Assessment request
- Questionnaire responses
- Supporting documentation
- Risk assessment report
- Approval records
- Remediation tracking
- Reassessment history

**Retention:** Duration of relationship + 3 years

## 8. Metrics

Track and report:
- Vendors assessed per period
- Assessment completion time
- Vendors by risk tier
- Findings by category
- Remediation completion rate
- Reassessment compliance

## 9. Roles and Responsibilities

### 9.1 IT Security
- Conduct assessments
- Review documentation
- Calculate risk ratings
- Make recommendations
- Track remediation

### 9.2 Procurement
- Initiate assessment requests
- Include security in RFPs
- Ensure contract compliance
- Track vendor inventory

### 9.3 Business Units
- Identify vendor needs
- Provide business context
- Accept residual risks
- Support assessment process

### 9.4 Legal
- Review contract terms
- Ensure regulatory compliance
- Advise on liability

## 10. Related Documents

- [Supplier Security Policy](../policies/supplier-security-policy.md)
- [Vendor Security Questionnaire](../templates/vendor-security-questionnaire.md)
- [Data Protection Policy](../policies/data-protection-policy.md)
- [Data Classification Policy](../policies/data-classification-policy.md)
- [Risk Assessment Methodology](../risk-assessment/methodologies/risk-assessment-methodology.md)

## 11. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

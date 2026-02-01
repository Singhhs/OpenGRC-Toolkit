# Risk Assessment Methodology

**Version:** [VERSION]
**Effective Date:** [DATE]
**Owner:** [ROLE]

---

## 1. Purpose

This document defines [ORGANIZATION NAME]'s methodology for conducting information security risk assessments in alignment with ISO 27001 and ISO 27005 standards.

## 2. Scope

This methodology applies to:
- Annual enterprise risk assessments
- System and project risk assessments
- Risk assessments triggered by significant changes
- Compliance-driven assessments

## 3. Risk Assessment Process

### 3.1 Phase 1: Context Establishment

#### 3.1.1 Define Objectives
- Purpose of the assessment
- Scope boundaries
- Key stakeholders
- Success criteria

#### 3.1.2 Gather Information
- Organization structure
- Business processes
- IT infrastructure
- Existing controls
- Previous assessments
- Threat intelligence

#### 3.1.3 Define Risk Criteria

**Risk Appetite Statement:**
[ORGANIZATION NAME] has a [conservative/moderate/aggressive] risk appetite for information security. We will accept residual risks up to [Medium] level for most systems, and require treatment plans for all [High/Critical] risks.

### 3.2 Phase 2: Risk Identification

#### 3.2.1 Asset Identification

Identify and document:
- Information assets (data)
- Software assets (applications)
- Physical assets (hardware)
- Services (cloud, network)
- People (roles with key responsibilities)

Use [Asset Inventory Template](../templates/asset-inventory-template.md).

#### 3.2.2 Threat Identification

Consider threats from:

| Source | Examples |
|--------|----------|
| **External Malicious** | Hackers, nation-states, hacktivists |
| **Internal Malicious** | Disgruntled employees, fraud |
| **Accidental Internal** | Human error, misconfiguration |
| **Environmental** | Natural disasters, power failure |
| **Technical** | System failure, software bugs |
| **Third Party** | Vendor compromise, supply chain |

Use [Threat Catalog](../templates/threat-catalog.md) as reference.

#### 3.2.3 Vulnerability Identification

Identify weaknesses through:
- Vulnerability scans
- Penetration tests
- Configuration reviews
- Policy compliance checks
- Interviews and workshops
- Previous incidents

#### 3.2.4 Control Identification

Document existing controls:
- Preventive controls
- Detective controls
- Corrective controls
- Assess current effectiveness

### 3.3 Phase 3: Risk Analysis

#### 3.3.1 Determine Likelihood

| Level | Score | Criteria |
|-------|-------|----------|
| Rare | 1 | May occur only in exceptional circumstances (<5% annual probability) |
| Unlikely | 2 | Could occur but not expected (5-25% annual probability) |
| Possible | 3 | Might occur at some time (25-50% annual probability) |
| Likely | 4 | Will probably occur (50-90% annual probability) |
| Almost Certain | 5 | Expected to occur frequently (>90% annual probability) |

**Factors affecting likelihood:**
- Historical frequency
- Threat actor capability and motivation
- Vulnerability exploitability
- Current control effectiveness
- Industry threat data

#### 3.3.2 Determine Impact

| Level | Score | Financial | Operational | Reputational | Regulatory |
|-------|-------|-----------|-------------|--------------|------------|
| Negligible | 1 | < $[10K] | < 4 hours | None | None |
| Low | 2 | $[10K-50K] | 4-24 hours | Local | Minor finding |
| Medium | 3 | $[50K-250K] | 1-3 days | Regional | Investigation |
| High | 4 | $[250K-1M] | 3-7 days | National | Significant penalty |
| Critical | 5 | > $[1M] | > 7 days | International | Business threatening |

<!-- CUSTOMIZE: Adjust financial thresholds for your organization -->

#### 3.3.3 Calculate Risk Level

**Risk Score = Likelihood × Impact**

| Score | Risk Level | Color |
|-------|------------|-------|
| 1-4 | Low | Green |
| 5-9 | Medium | Yellow |
| 10-16 | High | Orange |
| 17-25 | Critical | Red |

### 3.4 Phase 4: Risk Evaluation

#### 3.4.1 Compare Against Criteria

| Risk Level | Required Action |
|------------|-----------------|
| **Critical** | Immediate action required. Escalate to executive. Treatment mandatory. |
| **High** | Treatment plan required within 30 days. Report to management. |
| **Medium** | Treatment plan or documented acceptance within 90 days. |
| **Low** | Monitor and include in regular reviews. May accept. |

#### 3.4.2 Prioritization Factors

Beyond risk score, consider:
- Regulatory requirements
- Contractual obligations
- Strategic importance
- Treatment feasibility
- Resource availability

### 3.5 Phase 5: Risk Treatment

#### 3.5.1 Treatment Options

| Option | Description | Example |
|--------|-------------|---------|
| **Avoid** | Stop the activity causing risk | Discontinue vulnerable service |
| **Mitigate** | Implement controls to reduce risk | Add MFA, encryption |
| **Transfer** | Share risk with third party | Cyber insurance, outsource |
| **Accept** | Acknowledge risk without treatment | Document and monitor |

#### 3.5.2 Treatment Selection Criteria

- Cost-benefit analysis
- Control effectiveness
- Implementation complexity
- Impact on business operations
- Alignment with risk appetite

#### 3.5.3 Document Treatment Plan

For each risk requiring treatment:
- Specific actions to take
- Responsible party
- Target completion date
- Required resources
- Expected residual risk

Use [Risk Treatment Plan Template](../templates/risk-treatment-plan-template.md).

### 3.6 Phase 6: Risk Acceptance

#### 3.6.1 Acceptance Authority

| Residual Risk Level | Acceptance Authority |
|--------------------|---------------------|
| Low | Risk Owner |
| Medium | [Department Head / Security Manager] |
| High | [CISO / Senior Management] |
| Critical | [Executive Committee / Board] |

#### 3.6.2 Acceptance Documentation

Risk acceptance must include:
- Risk description
- Residual risk level
- Justification for acceptance
- Compensating controls (if any)
- Review date
- Acceptor signature

### 3.7 Phase 7: Communication & Reporting

#### 3.7.1 Assessment Report

Include:
- Executive summary
- Scope and methodology
- Key findings (prioritized)
- Risk register
- Treatment recommendations
- Appendices

#### 3.7.2 Stakeholder Communication

| Audience | Content | Frequency |
|----------|---------|-----------|
| Executive/Board | Summary, critical risks, trends | Quarterly |
| Management | All high+ risks, treatment status | Monthly |
| Risk Owners | Their assigned risks | As needed |
| Audit Committee | Compliance status | Per schedule |

### 3.8 Phase 8: Monitoring & Review

#### 3.8.1 Ongoing Monitoring

- Track treatment plan progress
- Monitor risk indicators
- Review incident data
- Update for changes

#### 3.8.2 Periodic Review

| Review | Frequency |
|--------|-----------|
| Risk register review | Quarterly |
| Full risk assessment | Annually |
| Post-incident review | After incidents |
| Change-triggered review | As needed |

## 4. Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| **Executive Management** | Approve methodology, risk appetite, major acceptances |
| **Risk Manager/CISO** | Lead assessment, maintain methodology, report |
| **Risk Owners** | Assess risks in their area, implement treatments |
| **IT/Security Team** | Provide technical input, implement controls |
| **Business Units** | Participate in assessment, identify assets/risks |

## 5. Tools and Templates

- [Risk Register Template](../templates/risk-register-template.md)
- [Risk Assessment Template](../templates/risk-assessment-template.md)
- [Risk Treatment Plan Template](../templates/risk-treatment-plan-template.md)
- [Asset Inventory Template](../templates/asset-inventory-template.md)
- [Threat Catalog](../templates/threat-catalog.md)

## 6. Related Documents

- [Information Security Policy](../../policies/information-security-policy.md)
- [ISO 27001 Framework](../../frameworks/iso-27001/README.md)

---

[Back to Methodologies](./README.md) | [Back to Risk Assessment](../README.md)

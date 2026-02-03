# Risk Assessment Methodology

**Version:** [VERSION]
**Effective Date:** [DATE]
**Owner:** [ROLE - e.g., CISO, Risk Manager]
**Classification:** Internal

---

## 1. Purpose

This document defines [ORGANIZATION NAME]'s methodology for conducting information security risk assessments in alignment with ISO 27001:2022 and ISO 27005 standards.

ISO 27001 is fundamentally **risk-based**. This methodology ensures that security decisions are driven by an understanding of business context, process criticality, and the potential impact of threats on business operations.

## 2. Scope

This methodology applies to:
- Annual enterprise risk assessments (ISO 27001 Clause 8.2)
- System and project risk assessments
- Risk assessments triggered by significant changes (ISO 27001 Clause 8.1)
- Compliance-driven assessments
- Third-party and supply chain risk assessments

## 3. ISO 27001 Risk-Based Approach

### 3.1 Fundamental Principles

ISO 27001 requires organizations to:

1. **Understand the organizational context** (Clause 4) - Including business objectives, stakeholder needs, and internal/external issues
2. **Assess risks to information** (Clause 6.1.2) - Based on confidentiality, integrity, and availability impacts
3. **Treat risks appropriately** (Clause 6.1.3) - Selecting controls from Annex A or elsewhere
4. **Continually improve** (Clause 10) - Based on risk monitoring and changing circumstances

### 3.2 Key Insight: Business Process Primacy

**Security exists to protect the business, not the other way around.**

Risk assessment must start with understanding:
- What business processes are critical to the organization?
- What systems and data support those processes?
- What is the business impact if those processes are disrupted?

Only then can threats and vulnerabilities be meaningfully assessed.

---

## 4. Prerequisites: Business Impact Analysis

### 4.1 BIA as Foundation

**A Business Impact Analysis (BIA) must be completed before or alongside risk assessment.**

The BIA establishes:
- Critical business processes
- Process dependencies on systems and data
- Recovery Time Objectives (RTO)
- Recovery Point Objectives (RPO)
- Financial and operational impact of disruption

Without BIA, risk assessment becomes a technical exercise disconnected from business reality.

### 4.2 BIA Outputs Required for Risk Assessment

| BIA Output | Use in Risk Assessment |
|------------|------------------------|
| Process criticality ratings | Determines impact severity |
| Process-to-system mapping | Identifies which systems matter most |
| RTO/RPO requirements | Informs availability risk ratings |
| Single points of failure | Highlights concentration risk |
| Dependencies | Reveals cascade effects |
| Financial impact data | Quantifies potential losses |

### 4.3 Process Criticality Levels

| Level | Definition | RTO Guidance | Examples |
|-------|------------|--------------|----------|
| **Critical** | Failure causes immediate, severe business impact; potential safety, legal, or existential consequences | < 4 hours | Payment processing, emergency services, trading |
| **High** | Significant impact on revenue, customers, or operations | 4-24 hours | Order management, core production, customer service |
| **Medium** | Moderate impact; business can function with workarounds | 1-3 days | Reporting, HR systems, internal tools |
| **Low** | Minimal immediate impact; inconvenience | 3+ days | Archives, training systems, development |

---

## 5. Risk Assessment Process

### 5.1 Process Overview

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    PREREQUISITE: Business Impact Analysis                │
│         Identify processes → Map systems → Determine criticality        │
└─────────────────────────────────────────────────────────────────────────┘
                                     │
                                     ▼
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  1. Establish   │────▶│   2. Identify   │────▶│   3. Analyze    │
│    Context      │     │     Risks       │     │     Risks       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
                                                        │
                                                        ▼
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  6. Monitor &   │◀────│   5. Treat      │◀────│   4. Evaluate   │
│     Review      │     │     Risks       │     │     Risks       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

---

### 5.2 Phase 1: Context Establishment

#### 5.2.1 Organizational Context (ISO 27001 Clause 4.1)

Document:
- Business objectives and strategy
- Regulatory and contractual obligations
- Industry and competitive environment
- Internal capabilities and constraints

#### 5.2.2 Interested Parties (ISO 27001 Clause 4.2)

Identify stakeholders and their security requirements:

| Stakeholder | Security Requirements |
|-------------|----------------------|
| Customers | Data protection, service availability |
| Regulators | Compliance with laws (GDPR, HIPAA, etc.) |
| Shareholders | Protection of assets and reputation |
| Employees | Personal data protection, safe working |
| Partners | Secure information exchange |

#### 5.2.3 ISMS Scope (ISO 27001 Clause 4.3)

Define boundaries:
- Organizational units included
- Locations covered
- Systems and networks in scope
- Processes covered
- Exclusions with justification

#### 5.2.4 Risk Criteria Definition

**Risk Appetite Statement:**

> [ORGANIZATION NAME] maintains a [conservative/moderate/risk-tolerant] approach to information security risk. We prioritize protection of [critical business processes/customer data/intellectual property]. We will not accept residual risks rated [High or Critical] without explicit executive approval and documented compensating controls.

---

### 5.3 Phase 2: Risk Identification

#### 5.3.1 Asset Identification (Process-Based Approach)

**Step 1: Start with Business Processes**

| Process | Criticality | Owner | Description |
|---------|-------------|-------|-------------|
| [Process name] | [Critical/High/Medium/Low] | [Role] | [Brief description] |

**Step 2: Map Supporting Systems**

For each process, identify:

| Process | Supporting Systems | Supporting Data | External Dependencies |
|---------|-------------------|-----------------|----------------------|
| [Process] | [System A, System B] | [Data type 1, Data type 2] | [Vendor X, Cloud Y] |

**Step 3: Document System Details**

| System | Type | Location | Owner | Criticality (from BIA) |
|--------|------|----------|-------|------------------------|
| [Name] | [App/Infra/Cloud] | [Location] | [Role] | [Inherited from process] |

Use [Asset Inventory Template](../templates/asset-inventory-template.md).

#### 5.3.2 Threat Identification

Using the [Threat Catalog](../threat-catalog.md), identify applicable threats for each critical system:

| System | Applicable Threats | Rationale |
|--------|-------------------|-----------|
| [System] | [T-MAL-001 Ransomware] | Processes sensitive data, internet-connected |
| [System] | [T-SOC-001 Phishing] | User-operated system |

**Threat Sources to Consider:**

| Category | Examples | Relevance |
|----------|----------|-----------|
| External Malicious | Hackers, organized crime, nation-states | [High/Medium/Low for your org] |
| Internal Malicious | Disgruntled employees, fraud | [High/Medium/Low] |
| Accidental Internal | Human error, misconfiguration | [High/Medium/Low] |
| Environmental | Natural disasters, power failure | [High/Medium/Low] |
| Third Party | Vendor compromise, supply chain | [High/Medium/Low] |

#### 5.3.3 Vulnerability Identification

Methods:
- Automated vulnerability scanning
- Penetration testing results
- Configuration compliance scans
- Architecture reviews
- Process and procedure gaps
- Historical incident analysis
- Audit findings

#### 5.3.4 Existing Control Assessment

Document current controls and their effectiveness:

| Control | Type | Effectiveness | Gaps |
|---------|------|---------------|------|
| [Control name] | Preventive/Detective/Corrective | [Effective/Partial/Ineffective] | [Identified gaps] |

---

### 5.4 Phase 3: Risk Analysis

#### 5.4.1 Determining Likelihood

| Level | Score | Criteria |
|-------|-------|----------|
| **Rare** | 1 | May occur only in exceptional circumstances (<5% annual) |
| **Unlikely** | 2 | Could occur but not expected (5-25% annual) |
| **Possible** | 3 | Might occur at some time (25-50% annual) |
| **Likely** | 4 | Will probably occur (50-90% annual) |
| **Almost Certain** | 5 | Expected to occur frequently (>90% annual) |

**Factors Affecting Likelihood:**
- Historical frequency of similar events
- Threat actor capability and motivation
- Vulnerability exploitability (CVSS score)
- Effectiveness of existing controls
- Industry threat intelligence
- Exposure (internet-facing, user-accessible)

#### 5.4.2 Determining Impact (Process-Driven)

**Base Impact Criteria:**

| Level | Score | Financial | Operational | Reputational | Regulatory |
|-------|-------|-----------|-------------|--------------|------------|
| **Negligible** | 1 | < $[10K] | < 4 hours | None | None |
| **Minor** | 2 | $[10K-50K] | 4-24 hours | Local | Minor finding |
| **Moderate** | 3 | $[50K-250K] | 1-3 days | Regional | Investigation |
| **Major** | 4 | $[250K-1M] | 3-7 days | National | Significant penalty |
| **Catastrophic** | 5 | > $[1M] | > 7 days | International | Business threatening |

<!-- CUSTOMIZE: Adjust financial thresholds for your organization -->

**Critical: Adjust Impact Based on Process Criticality**

The impact of a threat is determined by the criticality of the process it affects:

| Base Technical Impact | Critical Process | High Process | Medium Process | Low Process |
|-----------------------|------------------|--------------|----------------|-------------|
| Catastrophic (5) | 5 | 5 | 4 | 3 |
| Major (4) | 5 | 4 | 3 | 2 |
| Moderate (3) | 4 | 3 | 3 | 2 |
| Minor (2) | 3 | 2 | 2 | 1 |
| Negligible (1) | 2 | 1 | 1 | 1 |

**Example:**
- Ransomware affecting a billing system (Critical process) = Impact 5
- Same ransomware affecting a training system (Low process) = Impact 3

#### 5.4.3 Calculate Risk Level

**Risk Score = Likelihood × Adjusted Impact**

| Score Range | Risk Level | Color |
|-------------|------------|-------|
| 1-4 | Low | Green |
| 5-9 | Medium | Yellow |
| 10-16 | High | Orange |
| 17-25 | Critical | Red |

**Risk Matrix:**

|  | Negligible (1) | Minor (2) | Moderate (3) | Major (4) | Catastrophic (5) |
|--|----------------|-----------|--------------|-----------|------------------|
| **Almost Certain (5)** | 5 Medium | 10 High | 15 High | 20 Critical | 25 Critical |
| **Likely (4)** | 4 Low | 8 Medium | 12 High | 16 High | 20 Critical |
| **Possible (3)** | 3 Low | 6 Medium | 9 Medium | 12 High | 15 High |
| **Unlikely (2)** | 2 Low | 4 Low | 6 Medium | 8 Medium | 10 High |
| **Rare (1)** | 1 Low | 2 Low | 3 Low | 4 Low | 5 Medium |

---

### 5.5 Phase 4: Risk Evaluation

#### 5.5.1 Compare Against Risk Criteria

| Risk Level | Required Action | Timeline |
|------------|-----------------|----------|
| **Critical** | Immediate action required. Escalate to executive. Treatment mandatory. | Immediate |
| **High** | Treatment plan required. Report to senior management. | 30 days |
| **Medium** | Treatment plan or documented acceptance required. | 90 days |
| **Low** | Monitor and include in regular reviews. May accept. | Next review |

#### 5.5.2 Additional Prioritization Factors

Beyond risk score, consider:

| Factor | Consideration |
|--------|---------------|
| **Regulatory requirement** | Must address regardless of score |
| **Contractual obligation** | Customer or partner requirements |
| **Process criticality** | Risks to critical processes take priority |
| **Concentration risk** | Multiple processes depending on one system |
| **Treatment feasibility** | Quick wins vs. complex implementations |
| **Resource availability** | Budget and staff constraints |

#### 5.5.3 Single Points of Failure

Flag systems that are:
- The sole support for a critical process
- Required by multiple critical processes
- Without viable manual workarounds
- Difficult to recover quickly

These warrant elevated risk treatment priority regardless of calculated score.

---

### 5.6 Phase 5: Risk Treatment (ISO 27001 Clause 6.1.3)

#### 5.6.1 Treatment Options

| Option | Description | When to Use | Example |
|--------|-------------|-------------|---------|
| **Avoid** | Eliminate the risk by removing the source | Unacceptable risk; viable alternative exists | Discontinue vulnerable service |
| **Modify** | Implement controls to reduce likelihood or impact | Cost-effective controls available | Add MFA, encryption, segmentation |
| **Share** | Transfer risk to third party | Insurance appropriate; outsourcing viable | Cyber insurance, managed services |
| **Retain** | Accept risk with monitoring | Low risk; no cost-effective treatment | Document and monitor |

#### 5.6.2 Control Selection

Select controls from:
- ISO 27001 Annex A (93 controls)
- Industry frameworks (NIST, CIS)
- Regulatory requirements
- Vendor recommendations
- Best practices

**Control Selection Criteria:**

| Criterion | Question |
|-----------|----------|
| Effectiveness | Will this control meaningfully reduce risk? |
| Cost | Is the control cost proportionate to risk reduction? |
| Feasibility | Can we implement this with available resources? |
| Compatibility | Does it work with existing systems and processes? |
| Usability | Will users accept and comply with the control? |
| Maintenance | Can we sustain this control over time? |

#### 5.6.3 Treatment Plans

For each risk requiring treatment:

| Element | Description |
|---------|-------------|
| Risk ID | Unique identifier |
| Risk description | Clear statement of the risk |
| Current risk level | Before treatment |
| Treatment option | Avoid/Modify/Share/Retain |
| Specific controls | What will be implemented |
| Responsible party | Who owns implementation |
| Target date | When treatment will be complete |
| Resources required | Budget, staff, tools |
| Target residual risk | Expected level after treatment |

Use [Risk Treatment Plan Template](../templates/risk-treatment-plan-template.md).

#### 5.6.4 Statement of Applicability (SoA)

Document for each Annex A control:
- Whether the control is applicable
- Justification if excluded
- Implementation status
- How the control is implemented

Reference: [Statement of Applicability Template](../../frameworks/iso-27001/statement-of-applicability.md)

---

### 5.7 Phase 6: Risk Acceptance

#### 5.7.1 Acceptance Authority

| Residual Risk Level | Acceptance Authority |
|--------------------|---------------------|
| Low | Risk Owner / Department Manager |
| Medium | [CISO / Security Manager] |
| High | [Executive Management / CIO] |
| Critical | [Board / Executive Committee] |

#### 5.7.2 Acceptance Requirements

Risk acceptance must document:
- Risk description and current level
- Justification for acceptance (why not treating further)
- Compensating controls in place
- Conditions or timeframe for acceptance
- Review date
- Formal sign-off by appropriate authority

#### 5.7.3 Unacceptable Risks

Some risks may not be acceptable regardless of business pressure:
- Risks violating legal requirements
- Risks violating ethical obligations
- Risks with potential for catastrophic, unrecoverable harm

These require escalation and executive decision.

---

### 5.8 Phase 7: Communication and Reporting

#### 5.8.1 Risk Register

Maintain a central risk register containing:
- All identified risks
- Current assessment (likelihood, impact, level)
- Treatment status
- Risk ownership
- Review dates

Use [Risk Register Template](../templates/risk-register-template.md).

#### 5.8.2 Reporting

| Audience | Content | Frequency |
|----------|---------|-----------|
| Board/Executive | Critical and high risks, trends, major decisions | Quarterly |
| Management | All high+ risks, treatment progress, resource needs | Monthly |
| Risk Owners | Their assigned risks, required actions | As needed |
| Audit Committee | Compliance status, control effectiveness | Per schedule |
| ISMS Committee | Full risk register review | Quarterly |

#### 5.8.3 Risk Assessment Report

Include:
- Executive summary
- Scope and methodology
- Business process context
- Key findings (prioritized by process criticality)
- Risk register snapshot
- Treatment recommendations
- Resource requirements
- Appendices

---

### 5.9 Phase 8: Monitoring and Review (ISO 27001 Clause 9)

#### 5.9.1 Ongoing Monitoring

| Activity | Frequency | Responsibility |
|----------|-----------|----------------|
| Track treatment plan progress | Weekly | Risk owners |
| Review risk indicators/KRIs | Monthly | Security team |
| Assess new threats | Continuous | Security team |
| Review incident data for risk insights | After incidents | Security team |
| Update for organizational changes | As needed | Risk manager |

#### 5.9.2 Periodic Review

| Review Type | Frequency | Trigger |
|-------------|-----------|---------|
| Risk register review | Quarterly | Scheduled |
| Full risk assessment | Annually | Scheduled + Clause 8.2 |
| Post-incident risk review | After significant incidents | Event-driven |
| Change-triggered review | As needed | Significant changes |
| BIA refresh | Annually or after major changes | Scheduled |

#### 5.9.3 Continual Improvement

Use risk assessment outputs to:
- Update security policies and procedures
- Adjust security awareness training
- Improve detection and response capabilities
- Inform budget and resource allocation
- Enhance business continuity plans

---

## 6. Integration with Business Continuity

### 6.1 BIA and Risk Assessment Alignment

| BIA Output | Risk Assessment Use |
|------------|---------------------|
| Process criticality | Drives impact ratings |
| RTO requirements | Informs availability risk severity |
| Dependencies | Identifies cascade risks |
| Single points of failure | Highlights concentration risk |
| Workaround availability | Affects actual impact assessment |

### 6.2 Recovery Planning Integration

Risk treatment should consider:
- Does the treatment reduce RTO/RPO risk?
- Does it eliminate single points of failure?
- Does it enable process resilience?
- Does it support business continuity objectives?

---

## 7. Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| **Executive Management** | Approve methodology, set risk appetite, accept high/critical risks |
| **Risk Manager/CISO** | Lead assessments, maintain methodology, report to management |
| **Process Owners** | Provide BIA input, assess process-specific risks |
| **System Owners** | Assess system risks, implement treatments |
| **IT/Security Team** | Provide technical input, implement controls, monitor |
| **Business Units** | Participate in BIA and assessment, identify assets/risks |
| **Internal Audit** | Independently assess risk management effectiveness |

---

## 8. Tools and Templates

| Document | Purpose |
|----------|---------|
| [Business Impact Analysis Template](../../templates/business-impact-analysis.md) | Assess process criticality |
| [Risk Register Template](../templates/risk-register-template.md) | Track identified risks |
| [Risk Assessment Template](../templates/risk-assessment-template.md) | Document assessment findings |
| [Risk Treatment Plan Template](../templates/risk-treatment-plan-template.md) | Plan risk responses |
| [Asset Inventory Template](../templates/asset-inventory-template.md) | Catalog information assets |
| [Threat Catalog](../threat-catalog.md) | Reference for threat identification |
| [Statement of Applicability](../../frameworks/iso-27001/statement-of-applicability.md) | Document control decisions |

---

## 9. Related Documents

- [Information Security Policy](../../policies/information-security-policy.md)
- [ISO 27001 Framework](../../frameworks/iso-27001/README.md)
- [Risk Treatment Procedure](../../frameworks/iso-27001/procedures/risk-treatment-procedure.md)
- [Business Continuity Policy](../../policies/business-continuity-policy.md)

---

## 10. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |
| 2.0 | [DATE] | [AUTHOR] | Added BIA integration, process-based approach |

---

[Back to Methodologies](./README.md) | [Back to Risk Assessment](../README.md)

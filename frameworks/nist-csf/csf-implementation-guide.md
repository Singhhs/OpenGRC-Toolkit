# NIST CSF 2.0 Implementation Guide

A practical step-by-step guide for implementing the NIST Cybersecurity Framework 2.0.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE] |
| **Classification** | Internal |

---

## 1. Introduction

### 1.1 Purpose

This guide provides a practical roadmap for implementing the NIST Cybersecurity Framework 2.0, from initial planning through ongoing operations.

### 1.2 Who Should Use This Guide

- CISOs and security leaders implementing CSF
- Consultants guiding clients through CSF adoption
- IT managers building cybersecurity programs
- Risk managers integrating cyber risk management
- Compliance teams aligning with frameworks

### 1.3 Implementation Approach

This guide follows a seven-step implementation process aligned with NIST recommendations:

```
┌────────────────────────────────────────────────────────┐
│  Step 1: Prioritize and Scope                          │
├────────────────────────────────────────────────────────┤
│  Step 2: Orient                                        │
├────────────────────────────────────────────────────────┤
│  Step 3: Create Current Profile                        │
├────────────────────────────────────────────────────────┤
│  Step 4: Conduct Risk Assessment                       │
├────────────────────────────────────────────────────────┤
│  Step 5: Create Target Profile                         │
├────────────────────────────────────────────────────────┤
│  Step 6: Determine, Analyze, and Prioritize Gaps       │
├────────────────────────────────────────────────────────┤
│  Step 7: Implement Action Plan                         │
└────────────────────────────────────────────────────────┘
```

---

## 2. Pre-Implementation

### 2.1 Readiness Assessment

Before beginning, assess organizational readiness:

```
□ Executive Support
  □ Executive sponsor identified
  □ Leadership understands CSF value
  □ Resources approved for implementation

□ Team Readiness
  □ Implementation team identified
  □ Roles and responsibilities defined
  □ CSF training completed

□ Organizational Factors
  □ Current security state understood
  □ Regulatory requirements documented
  □ Business objectives clear

□ Resources
  □ Budget allocated
  □ Tools and templates available
  □ Timeline established
```

### 2.2 Implementation Team

| Role | Responsibilities | Suggested Member |
|------|------------------|------------------|
| **Executive Sponsor** | Champions initiative, removes barriers | C-level executive |
| **Program Manager** | Overall coordination, timeline, deliverables | Project/program manager |
| **Technical Lead** | Technical assessment, implementation | CISO, Security Manager |
| **Business Liaison** | Business context, requirements | Business unit representatives |
| **Risk Manager** | Risk assessment, integration with ERM | Risk/compliance manager |
| **Subject Matter Experts** | Specific domain expertise | IT, HR, Legal, Operations |

### 2.3 Timeline Expectations

| Organization Size | Typical Timeline |
|-------------------|------------------|
| Small (< 100 employees) | 3-6 months |
| Medium (100-1000 employees) | 6-12 months |
| Large (1000+ employees) | 12-18 months |
| Complex/regulated | 18-24 months |

---

## 3. Step 1: Prioritize and Scope

### 3.1 Objectives

- Define business and mission objectives
- Determine systems and assets in scope
- Identify regulatory and contractual requirements
- Establish priorities for implementation

### 3.2 Activities

#### 3.2.1 Define Business Objectives

```
□ Document organization's mission statement
□ Identify key business objectives
□ Determine how cybersecurity supports objectives
□ List critical business processes
□ Identify key stakeholders and their expectations
```

**Questions to Answer:**
- What is the organization's mission?
- What are the most critical business functions?
- What would happen if those functions were disrupted?
- What are stakeholder expectations for security?

#### 3.2.2 Define Scope

| Scope Element | Questions | Documentation |
|---------------|-----------|---------------|
| **Business Units** | Which units are included? | List of units |
| **Systems** | Which systems are in scope? | System inventory |
| **Data** | What data types are covered? | Data classification |
| **Locations** | Which locations are included? | Location list |
| **Third Parties** | Which vendors are in scope? | Vendor list |

**Scope Statement Template:**
```
This CSF implementation covers:
- Business Units: [LIST]
- Systems: [LIST OR REFERENCE]
- Data Types: [CLASSIFICATION LEVELS]
- Locations: [LIST]
- Third Parties: [CATEGORIES]

Out of scope:
- [EXCLUSIONS]
```

#### 3.2.3 Identify Requirements

| Requirement Type | Examples | Documentation |
|------------------|----------|---------------|
| **Regulatory** | GDPR, HIPAA, PCI DSS, SOX | Compliance matrix |
| **Contractual** | Customer requirements, SLAs | Contract review |
| **Industry** | Sector-specific standards | Standards list |
| **Internal** | Policies, risk appetite | Policy review |

### 3.3 Deliverables

- [ ] Scope document
- [ ] Business objectives statement
- [ ] Requirements matrix
- [ ] Stakeholder list
- [ ] Initial timeline

---

## 4. Step 2: Orient

### 4.1 Objectives

- Identify related systems and assets
- Identify threats and vulnerabilities
- Determine applicable CSF subcategories
- Understand current cybersecurity landscape

### 4.2 Activities

#### 4.2.1 Asset Identification

```
□ Inventory hardware assets
  □ Servers and endpoints
  □ Network devices
  □ Mobile devices
  □ IoT devices

□ Inventory software assets
  □ Operating systems
  □ Applications
  □ Cloud services
  □ Development tools

□ Inventory data assets
  □ Customer data
  □ Employee data
  □ Financial data
  □ Intellectual property

□ Document dependencies
  □ Internal dependencies
  □ External dependencies (suppliers, cloud)
  □ Data flows
```

#### 4.2.2 Threat and Vulnerability Identification

| Activity | Tools/Methods | Output |
|----------|---------------|--------|
| Threat identification | Threat intelligence, MITRE ATT&CK | Threat catalog |
| Vulnerability scanning | Automated scanners | Vulnerability report |
| Penetration testing | Internal/external testing | Test results |
| Risk scenarios | Workshops, analysis | Scenario documentation |

#### 4.2.3 CSF Subcategory Selection

Review all 106 subcategories and determine applicability:

| Applicability | Criteria | Action |
|---------------|----------|--------|
| **Applicable** | Relevant to scope and risk | Include in assessment |
| **Partially Applicable** | Relevant in limited context | Note limitations |
| **Not Applicable** | Not relevant to organization | Document rationale |

### 4.3 Deliverables

- [ ] Asset inventory
- [ ] Threat and vulnerability report
- [ ] Data flow diagrams
- [ ] Applicable subcategory list
- [ ] Initial risk landscape

---

## 5. Step 3: Create Current Profile

### 5.1 Objectives

- Document current cybersecurity state
- Assess each applicable subcategory
- Identify existing controls and capabilities
- Establish baseline for improvement

### 5.2 Activities

#### 5.2.1 Gather Evidence

| Evidence Type | Examples | Collection Method |
|---------------|----------|-------------------|
| **Policies** | Security policies, standards | Document review |
| **Procedures** | Operational procedures | Document review |
| **Technical Controls** | Security tools, configurations | Technical assessment |
| **Records** | Audit logs, training records | Record review |
| **Interviews** | Staff knowledge, practices | Stakeholder interviews |

#### 5.2.2 Assess Each Subcategory

For each applicable subcategory:

```
1. Review subcategory description
2. Identify relevant controls/practices
3. Gather evidence of implementation
4. Rate current state (0-4 scale)
5. Document gaps and observations
6. Note improvement opportunities
```

**Rating Scale:**

| Rating | Description | Evidence Expected |
|--------|-------------|-------------------|
| 0 | Not implemented | No evidence |
| 1 | Partial | Ad hoc practices, limited evidence |
| 2 | Risk informed | Documented but inconsistent |
| 3 | Repeatable | Formal, consistent, documented |
| 4 | Adaptive | Continuously improved, metrics-driven |

#### 5.2.3 Document Current State

Use the [CSF Profile Template](./csf-profile-template.md) to document:

- Current state for each subcategory
- Evidence supporting the rating
- Gaps identified
- Observations and notes

### 5.3 Deliverables

- [ ] Completed Current Profile
- [ ] Evidence documentation
- [ ] Gap inventory
- [ ] Current tier assessment

---

## 6. Step 4: Conduct Risk Assessment

### 6.1 Objectives

- Analyze the operating environment
- Determine likelihood and impact of threats
- Prioritize risks based on business impact
- Inform target state decisions

### 6.2 Activities

#### 6.2.1 Identify Risks

For each identified threat and vulnerability:

| Risk Element | Analysis |
|--------------|----------|
| **Threat Source** | Who or what could exploit? |
| **Threat Action** | What action could occur? |
| **Vulnerability** | What weakness could be exploited? |
| **Impact** | What is the business impact? |
| **Likelihood** | How likely is this scenario? |

#### 6.2.2 Risk Analysis

**Likelihood Assessment:**

| Level | Description | Criteria |
|-------|-------------|----------|
| High | Very likely | Has occurred, easy to exploit |
| Medium | Possible | Could occur, requires effort |
| Low | Unlikely | Remote possibility |

**Impact Assessment:**

| Level | Description | Criteria |
|-------|-------------|----------|
| High | Severe | Major financial, operational, or reputational harm |
| Medium | Significant | Moderate harm, recoverable |
| Low | Minor | Limited harm, easily addressed |

**Risk Matrix:**

| | Low Impact | Medium Impact | High Impact |
|---|---|---|---|
| **High Likelihood** | Medium | High | Critical |
| **Medium Likelihood** | Low | Medium | High |
| **Low Likelihood** | Low | Low | Medium |

#### 6.2.3 Prioritize Risks

Rank risks by:
1. Risk level (Critical, High, Medium, Low)
2. Business impact
3. Regulatory implications
4. Remediation cost and effort

### 6.3 Deliverables

- [ ] Risk register
- [ ] Risk assessment report
- [ ] Prioritized risk list
- [ ] Risk treatment recommendations

---

## 7. Step 5: Create Target Profile

### 7.1 Objectives

- Define desired future state
- Align targets with risk tolerance
- Set realistic, achievable goals
- Consider resource constraints

### 7.2 Activities

#### 7.2.1 Define Target State

For each applicable subcategory, determine:

| Factor | Consideration |
|--------|---------------|
| **Risk priority** | Higher risk = higher priority target |
| **Regulatory requirements** | Compliance drives minimum target |
| **Business objectives** | Alignment with strategy |
| **Resource availability** | What can be achieved? |
| **Timeline** | When can it be achieved? |

#### 7.2.2 Target Setting Guidelines

| Current State | Typical Target | Rationale |
|---------------|----------------|-----------|
| 0 - Not implemented | 2 | Establish basic capability |
| 1 - Partial | 2-3 | Formalize and document |
| 2 - Risk informed | 3 | Standardize organization-wide |
| 3 - Repeatable | 3-4 | Optimize and improve |
| 4 - Adaptive | 4 | Maintain excellence |

#### 7.2.3 Validate Targets

```
□ Targets align with risk tolerance
□ Targets are achievable with available resources
□ Targets meet regulatory requirements
□ Targets support business objectives
□ Leadership has approved targets
```

### 7.3 Deliverables

- [ ] Completed Target Profile
- [ ] Target rationale documentation
- [ ] Leadership approval
- [ ] Timeline for achievement

---

## 8. Step 6: Determine, Analyze, and Prioritize Gaps

### 8.1 Objectives

- Compare current to target profiles
- Identify and analyze gaps
- Prioritize based on risk and resources
- Develop remediation approaches

### 8.2 Activities

#### 8.2.1 Gap Analysis

| Subcategory | Current | Target | Gap | Priority |
|-------------|---------|--------|-----|----------|
| [ID] | [0-4] | [0-4] | [Difference] | [H/M/L] |

#### 8.2.2 Gap Prioritization

Prioritize gaps based on:

| Factor | Weight | Description |
|--------|--------|-------------|
| Risk impact | 40% | How much does the gap increase risk? |
| Regulatory requirement | 25% | Is it required for compliance? |
| Implementation effort | 20% | How difficult to remediate? |
| Dependencies | 15% | Are other improvements dependent on this? |

**Priority Matrix:**

| Priority | Criteria | Action |
|----------|----------|--------|
| **Critical** | High risk + compliance required | Immediate action |
| **High** | High risk or compliance required | Near-term action |
| **Medium** | Moderate risk, improvement opportunity | Planned action |
| **Low** | Low risk, nice to have | As resources allow |

#### 8.2.3 Develop Remediation Approaches

For each gap, identify:

```
Gap: [SUBCATEGORY ID]
Current State: [DESCRIPTION]
Target State: [DESCRIPTION]

Remediation Options:
□ Option A: [DESCRIPTION]
  - Effort: [HIGH/MEDIUM/LOW]
  - Cost: [ESTIMATE]
  - Timeline: [ESTIMATE]

□ Option B: [DESCRIPTION]
  - Effort: [HIGH/MEDIUM/LOW]
  - Cost: [ESTIMATE]
  - Timeline: [ESTIMATE]

Recommended Approach: [OPTION]
Rationale: [EXPLANATION]
```

### 8.3 Deliverables

- [ ] Gap analysis report
- [ ] Prioritized gap list
- [ ] Remediation recommendations
- [ ] Resource requirements

---

## 9. Step 7: Implement Action Plan

### 9.1 Objectives

- Create detailed implementation roadmap
- Execute remediation activities
- Monitor progress and adjust
- Achieve target profile

### 9.2 Activities

#### 9.2.1 Create Implementation Roadmap

**Phase Structure:**

| Phase | Timeframe | Focus |
|-------|-----------|-------|
| **Phase 1: Foundation** | 0-6 months | Critical gaps, quick wins |
| **Phase 2: Build** | 6-12 months | High priority improvements |
| **Phase 3: Enhance** | 12-18 months | Medium priority, optimization |
| **Phase 4: Sustain** | Ongoing | Continuous improvement |

**Roadmap Template:**

| Phase | Gap | Action | Owner | Start | End | Dependencies | Status |
|-------|-----|--------|-------|-------|-----|--------------|--------|
| 1 | [ID] | [Action] | [Name] | [Date] | [Date] | [Deps] | [ ] |

#### 9.2.2 Quick Wins

Identify and prioritize quick wins:

```
□ Policy updates and documentation
□ Configuration hardening
□ Access control improvements
□ Security awareness training
□ Logging and monitoring enablement
□ Backup verification
```

#### 9.2.3 Execute and Monitor

**Weekly Activities:**
- Track task completion
- Address blockers
- Update stakeholders

**Monthly Activities:**
- Review progress against plan
- Assess risk reduction
- Adjust priorities as needed
- Report to leadership

**Quarterly Activities:**
- Reassess current profile
- Review effectiveness of controls
- Update target profile if needed
- Strategic planning review

### 9.3 Deliverables

- [ ] Implementation roadmap
- [ ] Detailed project plans
- [ ] Progress reports
- [ ] Updated profiles

---

## 10. Ongoing Operations

### 10.1 Continuous Monitoring

| Activity | Frequency | Purpose |
|----------|-----------|---------|
| Control effectiveness | Ongoing | Verify controls working |
| Risk assessment | Quarterly | Update risk landscape |
| Profile assessment | Annually | Measure progress |
| Tier assessment | Annually | Evaluate maturity |

### 10.2 Continuous Improvement

```
┌─────────────────────────────────────┐
│         PLAN                        │
│   Identify improvements             │
│   Plan changes                      │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│         DO                          │
│   Implement changes                 │
│   Document actions                  │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│         CHECK                       │
│   Measure effectiveness             │
│   Compare to targets                │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│         ACT                         │
│   Standardize improvements          │
│   Identify next improvements        │
└─────────────────┬───────────────────┘
                  │
                  └────────► [Back to PLAN]
```

### 10.3 Profile Maintenance

| Trigger | Action |
|---------|--------|
| Annual review | Full profile reassessment |
| Major incident | Review relevant subcategories |
| Organizational change | Update scope, reassess affected areas |
| Regulatory change | Review compliance requirements |
| Technology change | Assess new risks and controls |

---

## 11. Success Factors

### 11.1 Critical Success Factors

| Factor | Why It Matters |
|--------|----------------|
| **Executive sponsorship** | Resources, priority, barriers removed |
| **Clear scope** | Focus, achievable goals |
| **Risk-based approach** | Prioritize what matters |
| **Cross-functional involvement** | Security is everyone's responsibility |
| **Documentation** | Evidence, repeatability, knowledge |
| **Continuous improvement** | Security is a journey, not destination |

### 11.2 Common Pitfalls

| Pitfall | Mitigation |
|---------|------------|
| Scope creep | Clear scope document, change control |
| Analysis paralysis | Time-box assessments, good enough |
| Tool dependency | Process first, tools support |
| Checkbox mentality | Focus on outcomes, not compliance |
| One-time effort | Build into ongoing operations |

---

## 12. Templates and Tools

### 12.1 Available Templates

| Template | Purpose | Link |
|----------|---------|------|
| Assessment Template | Rate current state | [CSF Assessment](./csf-assessment-template.md) |
| Profile Template | Document current/target | [CSF Profile](./csf-profile-template.md) |
| Gap Analysis | Compare and prioritize | Included in Profile |
| Implementation Roadmap | Plan improvements | Section 9 |

### 12.2 Recommended Tools

| Category | Examples |
|----------|----------|
| GRC Platforms | ServiceNow, RSA Archer, OneTrust |
| Assessment Tools | NIST CSF Tools, CIS-CAT |
| Risk Management | Risk registers, heat maps |
| Project Management | MS Project, Jira, Monday.com |

---

## 13. Related Documents

- [NIST CSF 2.0 Guide](./nist-csf-guide.md)
- [CSF Assessment Template](./csf-assessment-template.md)
- [CSF Profile Template](./csf-profile-template.md)
- [Implementation Tiers Guide](./implementation-tiers-guide.md)
- [NIST CSF to ISO 27001 Mapping](./nist-iso27001-mapping.md)

---

## 14. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to NIST CSF](./README.md) | [Back to Frameworks](../README.md)

# NIST Cybersecurity Framework 2.0 Guide

A comprehensive guide to implementing the NIST Cybersecurity Framework (CSF) 2.0.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., CISO, Security Manager] |
| **Classification** | Internal |

---

## 1. Introduction

### 1.1 What is the NIST CSF?

The NIST Cybersecurity Framework (CSF) is a voluntary framework developed by the National Institute of Standards and Technology (NIST) that provides organizations with guidance to manage and reduce cybersecurity risk.

**CSF 2.0** was released in February 2024 and includes significant updates from the original 2014 framework and 2018 update.

### 1.2 Key Changes in CSF 2.0

| Change | Description |
|--------|-------------|
| **New GOVERN Function** | Added sixth function focused on governance and risk management strategy |
| **Broader Scope** | Expanded beyond critical infrastructure to all organizations |
| **Supply Chain Focus** | Enhanced emphasis on supply chain risk management |
| **Implementation Examples** | New resources with practical implementation guidance |
| **Profiles Enhanced** | Improved guidance for creating organizational and community profiles |

### 1.3 Who Should Use CSF?

The CSF is designed for:
- Organizations of all sizes and sectors
- Critical infrastructure operators
- Government agencies
- Private sector companies
- International organizations

### 1.4 CSF Benefits

| Benefit | Description |
|---------|-------------|
| **Risk-Based** | Focus resources on highest-priority risks |
| **Flexible** | Adaptable to any organization size or sector |
| **Common Language** | Shared vocabulary for cybersecurity discussions |
| **Integration** | Works with existing standards (ISO, COBIT, CIS) |
| **Continuous Improvement** | Supports maturity progression |

---

## 2. Framework Structure

### 2.1 Core Components

The CSF consists of three main components:

```
┌─────────────────────────────────────────────────────┐
│                    CSF CORE                         │
│  ┌─────────┐  ┌─────────┐  ┌─────────────────────┐ │
│  │Functions│─▶│Categories│─▶│    Subcategories    │ │
│  │   (6)   │  │   (22)   │  │       (106)         │ │
│  └─────────┘  └─────────┘  └─────────────────────┘ │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│               ORGANIZATIONAL PROFILES               │
│         Current State ──▶ Target State              │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│              IMPLEMENTATION TIERS                   │
│    Tier 1 ──▶ Tier 2 ──▶ Tier 3 ──▶ Tier 4        │
│   Partial    Risk       Repeatable   Adaptive      │
│              Informed                               │
└─────────────────────────────────────────────────────┘
```

### 2.2 The Six Functions

| Function | ID | Purpose | Focus |
|----------|-------|---------|-------|
| **GOVERN** | GV | Establish cybersecurity risk management strategy | Strategy, policy, oversight |
| **IDENTIFY** | ID | Understand organizational context and risks | Assets, risks, environment |
| **PROTECT** | PR | Implement appropriate safeguards | Access, training, security |
| **DETECT** | DE | Identify cybersecurity events | Monitoring, detection |
| **RESPOND** | RS | Take action on detected events | Response, mitigation |
| **RECOVER** | RC | Restore capabilities and resilience | Recovery, improvements |

---

## 3. GOVERN Function (GV)

*New in CSF 2.0 - The foundation for cybersecurity risk management*

### 3.1 Overview

The GOVERN function establishes and monitors the organization's cybersecurity risk management strategy, expectations, and policy. It provides context for all other functions.

### 3.2 Categories

#### GV.OC - Organizational Context

Understanding the organization's mission, stakeholder expectations, and dependencies.

| Subcategory | Description |
|-------------|-------------|
| GV.OC-01 | Organizational mission is understood and informs cybersecurity risk management |
| GV.OC-02 | Internal and external stakeholders are understood, and their needs and expectations are understood and considered |
| GV.OC-03 | Legal, regulatory, and contractual requirements are understood and managed |
| GV.OC-04 | Critical objectives, capabilities, and services are understood and communicated |
| GV.OC-05 | Outcomes, capabilities, and services that depend on or are enabled by other organizations are understood and communicated |

#### GV.RM - Risk Management Strategy

Establishing priorities, constraints, risk tolerance, and assumptions.

| Subcategory | Description |
|-------------|-------------|
| GV.RM-01 | Risk management objectives are established and agreed to by organizational stakeholders |
| GV.RM-02 | Risk appetite and risk tolerance statements are established, communicated, and maintained |
| GV.RM-03 | Cybersecurity risk management activities and outcomes are included in enterprise risk management processes |
| GV.RM-04 | Strategic direction that describes appropriate risk response options is established and communicated |
| GV.RM-05 | Lines of communication across the organization are established for cybersecurity risks |
| GV.RM-06 | A standardized method for calculating, documenting, categorizing, and prioritizing cybersecurity risks is established and communicated |
| GV.RM-07 | Strategic opportunities are characterized and communicated |

#### GV.RR - Roles, Responsibilities, and Authorities

Establishing accountability for cybersecurity.

| Subcategory | Description |
|-------------|-------------|
| GV.RR-01 | Organizational leadership is responsible for cybersecurity risk and fosters a culture of security |
| GV.RR-02 | Roles, responsibilities, and authorities for cybersecurity risk management are established, communicated, and enforced |
| GV.RR-03 | Adequate resources are allocated for cybersecurity risk management |
| GV.RR-04 | Cybersecurity is included in human resources practices |

#### GV.PO - Policy

Establishing, communicating, and enforcing policy.

| Subcategory | Description |
|-------------|-------------|
| GV.PO-01 | Policy for managing cybersecurity risks is established based on organizational context, cybersecurity strategy, and priorities |
| GV.PO-02 | Policy for managing cybersecurity risks is reviewed, updated, communicated, and enforced |

#### GV.OV - Oversight

Ongoing review and adjustment of risk management.

| Subcategory | Description |
|-------------|-------------|
| GV.OV-01 | Cybersecurity risk management strategy outcomes are reviewed to inform and adjust strategy |
| GV.OV-02 | The cybersecurity risk management strategy is reviewed and adjusted |
| GV.OV-03 | Organizational cybersecurity risk management performance is evaluated and reviewed |

#### GV.SC - Cybersecurity Supply Chain Risk Management

Managing supply chain risks.

| Subcategory | Description |
|-------------|-------------|
| GV.SC-01 | A cybersecurity supply chain risk management program is established |
| GV.SC-02 | Cybersecurity roles and responsibilities for suppliers, customers, and partners are established |
| GV.SC-03 | Cybersecurity supply chain risk management is integrated into broader risk management |
| GV.SC-04 | Suppliers are known and prioritized by criticality |
| GV.SC-05 | Requirements are established, prioritized, and integrated into contracts and agreements |
| GV.SC-06 | Planning and due diligence are conducted to reduce risks before entering relationships |
| GV.SC-07 | Risks posed by suppliers and partners are understood, recorded, prioritized, assessed, responded to, and monitored |
| GV.SC-08 | Relevant suppliers and partners are included in incident planning, response, and recovery |
| GV.SC-09 | Supply chain security practices are integrated into cybersecurity programs |
| GV.SC-10 | Cybersecurity supply chain risk management plans include provisions for activities after conclusion of relationships |

---

## 4. IDENTIFY Function (ID)

*Understanding the organization's cybersecurity risks*

### 4.1 Overview

The IDENTIFY function helps develop an organizational understanding of managing cybersecurity risk to systems, people, assets, data, and capabilities.

### 4.2 Categories

#### ID.AM - Asset Management

Managing assets that enable the organization to achieve business purposes.

| Subcategory | Description |
|-------------|-------------|
| ID.AM-01 | Inventories of hardware managed by the organization are maintained |
| ID.AM-02 | Inventories of software, services, and systems managed by the organization are maintained |
| ID.AM-03 | Representations of the organization's authorized network communication and data flows are maintained |
| ID.AM-04 | Inventories of services provided by suppliers are maintained |
| ID.AM-05 | Assets are prioritized based on classification, criticality, resources, and mission impact |
| ID.AM-07 | Inventories of data and corresponding metadata are maintained |
| ID.AM-08 | Systems, hardware, software, and services are managed throughout their life cycles |

#### ID.RA - Risk Assessment

Understanding cybersecurity risks.

| Subcategory | Description |
|-------------|-------------|
| ID.RA-01 | Vulnerabilities in assets are identified, validated, and recorded |
| ID.RA-02 | Cyber threat intelligence is received from information sharing forums and sources |
| ID.RA-03 | Internal and external threats are identified and recorded |
| ID.RA-04 | Potential impacts and likelihoods of threats exploiting vulnerabilities are identified and recorded |
| ID.RA-05 | Threats, vulnerabilities, likelihoods, and impacts are used to understand inherent risk |
| ID.RA-06 | Risk responses are chosen, prioritized, planned, tracked, and communicated |
| ID.RA-07 | Changes and exceptions are managed, assessed for risk impact, recorded, and tracked |
| ID.RA-08 | Processes for receiving, analyzing, and responding to vulnerability disclosures are established |
| ID.RA-09 | The authenticity and integrity of hardware and software are assessed prior to acquisition and use |
| ID.RA-10 | Critical suppliers are assessed prior to acquisition |

#### ID.IM - Improvement

Improving cybersecurity risk management processes.

| Subcategory | Description |
|-------------|-------------|
| ID.IM-01 | Improvements are identified from evaluations |
| ID.IM-02 | Improvements are identified from security tests and exercises |
| ID.IM-03 | Improvements are identified from execution of operational processes, procedures, and activities |
| ID.IM-04 | Incident response plans and other cybersecurity plans are established, communicated, maintained, and improved |

---

## 5. PROTECT Function (PR)

*Implementing appropriate safeguards*

### 5.1 Overview

The PROTECT function supports the ability to secure assets and prevent or lower the likelihood and impact of cybersecurity events.

### 5.2 Categories

#### PR.AA - Identity Management, Authentication, and Access Control

Limiting access to assets.

| Subcategory | Description |
|-------------|-------------|
| PR.AA-01 | Identities and credentials for authorized users, services, and hardware are managed |
| PR.AA-02 | Identities are proofed and bound to credentials based on context of interactions |
| PR.AA-03 | Users, services, and hardware are authenticated |
| PR.AA-04 | Identity assertions are protected, conveyed, and verified |
| PR.AA-05 | Access permissions, entitlements, and authorizations are defined and managed |
| PR.AA-06 | Physical access to assets is managed, monitored, and enforced |

#### PR.AT - Awareness and Training

Ensuring personnel have cybersecurity knowledge and skills.

| Subcategory | Description |
|-------------|-------------|
| PR.AT-01 | Personnel are provided awareness and training so they have knowledge and skills to perform tasks with security in mind |
| PR.AT-02 | Individuals in specialized roles are provided awareness and training for their roles |

#### PR.DS - Data Security

Managing data consistent with risk strategy.

| Subcategory | Description |
|-------------|-------------|
| PR.DS-01 | Data-at-rest is protected |
| PR.DS-02 | Data-in-transit is protected |
| PR.DS-10 | Data-in-use is protected |
| PR.DS-11 | Backups of data are created, protected, maintained, and tested |

#### PR.PS - Platform Security

Securing hardware, software, and services.

| Subcategory | Description |
|-------------|-------------|
| PR.PS-01 | Configuration management practices are established and applied |
| PR.PS-02 | Software is maintained, replaced, and removed |
| PR.PS-03 | Hardware is maintained, replaced, and removed |
| PR.PS-04 | Log records are generated and made available for continuous monitoring |
| PR.PS-05 | Installation and execution of unauthorized software are prevented |
| PR.PS-06 | Secure software development practices are integrated |

#### PR.IR - Technology Infrastructure Resilience

Managing security architecture for resilience.

| Subcategory | Description |
|-------------|-------------|
| PR.IR-01 | Networks and environments are protected from unauthorized logical access |
| PR.IR-02 | The organization's technology assets are protected from environmental threats |
| PR.IR-03 | Mechanisms are implemented to achieve resilience requirements |
| PR.IR-04 | Adequate resource capacity to ensure availability is maintained |

---

## 6. DETECT Function (DE)

*Identifying cybersecurity events*

### 6.1 Overview

The DETECT function enables timely discovery and analysis of anomalies, indicators of compromise, and other potentially adverse events.

### 6.2 Categories

#### DE.CM - Continuous Monitoring

Monitoring assets to identify anomalies and adverse events.

| Subcategory | Description |
|-------------|-------------|
| DE.CM-01 | Networks and network services are monitored to find potentially adverse events |
| DE.CM-02 | The physical environment is monitored to find potentially adverse events |
| DE.CM-03 | Personnel activity and technology usage are monitored |
| DE.CM-06 | External service provider activities and services are monitored |
| DE.CM-09 | Computing hardware and software, runtime environments, and their data are monitored |

#### DE.AE - Adverse Event Analysis

Analyzing anomalies and events.

| Subcategory | Description |
|-------------|-------------|
| DE.AE-02 | Potentially adverse events are analyzed to better understand associated activities |
| DE.AE-03 | Information is correlated from multiple sources |
| DE.AE-04 | The estimated impact and scope of adverse events are understood |
| DE.AE-06 | Information on adverse events is provided to authorized staff and tools |
| DE.AE-07 | Cyber threat intelligence and other contextual information are integrated into the analysis |
| DE.AE-08 | Incidents are declared when adverse events meet defined criteria |

---

## 7. RESPOND Function (RS)

*Taking action on detected incidents*

### 7.1 Overview

The RESPOND function supports the ability to contain the effects of cybersecurity incidents.

### 7.2 Categories

#### RS.MA - Incident Management

Managing incidents.

| Subcategory | Description |
|-------------|-------------|
| RS.MA-01 | The incident response plan is executed in coordination with relevant third parties |
| RS.MA-02 | Incident reports are triaged and validated |
| RS.MA-03 | Incidents are categorized and prioritized |
| RS.MA-04 | Incidents are escalated or elevated as needed |
| RS.MA-05 | The criteria for initiating incident recovery are applied |

#### RS.AN - Incident Analysis

Investigating incidents.

| Subcategory | Description |
|-------------|-------------|
| RS.AN-03 | Analysis is performed to establish what has taken place during an incident |
| RS.AN-06 | Actions performed during an investigation are recorded |
| RS.AN-07 | Incident data and metadata are collected and their integrity preserved |
| RS.AN-08 | An incident's magnitude is estimated and validated |

#### RS.CO - Incident Response Reporting and Communication

Coordinating response activities.

| Subcategory | Description |
|-------------|-------------|
| RS.CO-02 | Internal and external stakeholders are notified of incidents |
| RS.CO-03 | Information is shared with designated internal and external stakeholders |

#### RS.MI - Incident Mitigation

Preventing expansion and mitigating effects.

| Subcategory | Description |
|-------------|-------------|
| RS.MI-01 | Incidents are contained |
| RS.MI-02 | Incidents are eradicated |

---

## 8. RECOVER Function (RC)

*Restoring capabilities and resilience*

### 8.1 Overview

The RECOVER function supports timely restoration of normal operations to reduce the impact of cybersecurity incidents.

### 8.2 Categories

#### RC.RP - Incident Recovery Plan Execution

Restoring systems and assets.

| Subcategory | Description |
|-------------|-------------|
| RC.RP-01 | The incident recovery portion of the incident response plan is executed |
| RC.RP-02 | Recovery actions are selected, scoped, prioritized, and performed |
| RC.RP-03 | The integrity of backups and other restoration assets is verified before using them |
| RC.RP-04 | Critical mission functions and cybersecurity risk management are considered as part of recovery |
| RC.RP-05 | The integrity of restored assets is verified, systems and services are restored, and normal operations are confirmed |
| RC.RP-06 | The end of incident recovery is declared based on criteria, and documentation is complete |

#### RC.CO - Incident Recovery Communication

Coordinating recovery activities.

| Subcategory | Description |
|-------------|-------------|
| RC.CO-03 | Recovery activities and progress are communicated to internal and external stakeholders |
| RC.CO-04 | Public updates on incident recovery are shared using approved methods and messaging |

---

## 9. Implementation Tiers

### 9.1 Overview

Implementation Tiers describe the degree to which an organization's cybersecurity risk management practices exhibit the characteristics defined in the Framework.

### 9.2 Tier Definitions

| Tier | Name | Characteristics |
|------|------|-----------------|
| **Tier 1** | Partial | Ad hoc, reactive, limited awareness |
| **Tier 2** | Risk Informed | Risk-aware but not organization-wide |
| **Tier 3** | Repeatable | Formal, consistent, organization-wide |
| **Tier 4** | Adaptive | Continuous improvement, predictive |

### 9.3 Tier Characteristics

#### Tier 1 - Partial

| Dimension | Characteristics |
|-----------|-----------------|
| **Risk Management Process** | Ad hoc, reactive, case-by-case |
| **Integrated Program** | Limited awareness of cybersecurity risk at organizational level |
| **External Participation** | Does not understand role in larger ecosystem |

#### Tier 2 - Risk Informed

| Dimension | Characteristics |
|-----------|-----------------|
| **Risk Management Process** | Risk-aware but not organization-wide policy |
| **Integrated Program** | Awareness exists but not consistent implementation |
| **External Participation** | Understands role but limited formal collaboration |

#### Tier 3 - Repeatable

| Dimension | Characteristics |
|-----------|-----------------|
| **Risk Management Process** | Formal, expressed as policy, regularly updated |
| **Integrated Program** | Organization-wide approach, roles defined, resources allocated |
| **External Participation** | Understands dependencies, collaborates formally |

#### Tier 4 - Adaptive

| Dimension | Characteristics |
|-----------|-----------------|
| **Risk Management Process** | Adapts based on lessons learned and predictive indicators |
| **Integrated Program** | Continuous improvement, proactive, part of culture |
| **External Participation** | Active contributor to community, real-time sharing |

---

## 10. Organizational Profiles

### 10.1 What is a Profile?

A Profile represents the alignment of the Framework Core with organizational requirements, risk tolerance, and resources. Profiles help organizations:

- Describe current cybersecurity posture (Current Profile)
- Define target cybersecurity goals (Target Profile)
- Identify and prioritize opportunities for improvement (Gap Analysis)

### 10.2 Profile Types

| Type | Purpose |
|------|---------|
| **Current Profile** | Documents current state of cybersecurity activities |
| **Target Profile** | Defines desired future state |
| **Community Profile** | Sector or industry-specific baseline |

### 10.3 Creating a Profile

**Step 1: Scope**
- Define organizational boundaries
- Identify critical assets and systems
- Determine stakeholder requirements

**Step 2: Assess Current State**
- Evaluate each subcategory
- Rate current implementation
- Document evidence

**Step 3: Define Target State**
- Determine desired outcomes
- Consider risk tolerance
- Align with business objectives

**Step 4: Gap Analysis**
- Compare current to target
- Prioritize gaps
- Develop action plans

---

## 11. Using the CSF

### 11.1 Implementation Approach

```
┌─────────────────────────────────────────────────────┐
│ Step 1: PRIORITIZE AND SCOPE                        │
│ - Identify business objectives                      │
│ - Determine systems/assets in scope                 │
│ - Identify regulatory/contractual requirements      │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│ Step 2: ORIENT                                      │
│ - Identify related systems and assets               │
│ - Identify threats and vulnerabilities              │
│ - Determine risk assessment approach                │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│ Step 3: CREATE CURRENT PROFILE                      │
│ - Assess current state against CSF                  │
│ - Document achievements per subcategory             │
│ - Note gaps and weaknesses                          │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│ Step 4: CONDUCT RISK ASSESSMENT                     │
│ - Analyze operating environment                     │
│ - Determine likelihood and impact                   │
│ - Calculate risk levels                             │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│ Step 5: CREATE TARGET PROFILE                       │
│ - Define desired outcomes                           │
│ - Consider risk tolerance                           │
│ - Set realistic targets                             │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│ Step 6: DETERMINE, ANALYZE, PRIORITIZE GAPS         │
│ - Compare current to target                         │
│ - Prioritize based on risk                          │
│ - Consider resources and constraints                │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│ Step 7: IMPLEMENT ACTION PLAN                       │
│ - Develop remediation roadmap                       │
│ - Assign responsibilities                           │
│ - Monitor progress and adjust                       │
└─────────────────────────────────────────────────────┘
```

### 11.2 Key Success Factors

| Factor | Description |
|--------|-------------|
| **Executive Support** | Leadership commitment and resources |
| **Cross-Functional** | Involvement from all business areas |
| **Risk-Based** | Prioritize based on actual risk |
| **Continuous** | Ongoing improvement, not one-time |
| **Documented** | Clear records of decisions and rationale |

---

## 12. CSF Quick Reference

### 12.1 Function Summary

| Function | Categories | Focus Areas |
|----------|------------|-------------|
| **GOVERN** | 6 | Context, Strategy, Roles, Policy, Oversight, Supply Chain |
| **IDENTIFY** | 3 | Assets, Risk Assessment, Improvement |
| **PROTECT** | 5 | Access, Training, Data, Platform, Resilience |
| **DETECT** | 2 | Monitoring, Analysis |
| **RESPOND** | 4 | Management, Analysis, Communication, Mitigation |
| **RECOVER** | 2 | Recovery Plan, Communication |

### 12.2 Key Actions by Function

| Function | Key Actions |
|----------|-------------|
| **GOVERN** | Establish strategy, define roles, create policies, oversee program |
| **IDENTIFY** | Inventory assets, assess risks, plan improvements |
| **PROTECT** | Control access, train staff, protect data, secure platforms |
| **DETECT** | Monitor continuously, analyze events, declare incidents |
| **RESPOND** | Execute plans, analyze incidents, communicate, mitigate |
| **RECOVER** | Restore operations, communicate progress, improve |

---

## 13. Related Documents

- [CSF Assessment Template](./csf-assessment-template.md)
- [CSF Profile Template](./csf-profile-template.md)
- [NIST CSF to ISO 27001 Mapping](./nist-iso27001-mapping.md)
- [Implementation Tiers Guide](./implementation-tiers-guide.md)
- [CSF Implementation Guide](./csf-implementation-guide.md)

---

## 14. External Resources

| Resource | Link |
|----------|------|
| NIST CSF Official Website | [nist.gov/cyberframework](https://www.nist.gov/cyberframework) |
| CSF 2.0 Document | [NIST.CSWP.29](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf) |
| CSF 2.0 Reference Tool | [csf.tools](https://csf.tools) |
| NIST SP 800-53 | Security and Privacy Controls |

---

## 15. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to NIST CSF](./README.md) | [Back to Frameworks](../README.md)

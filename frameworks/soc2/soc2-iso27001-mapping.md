# SOC 2 to ISO 27001:2022 Mapping

A comprehensive mapping between SOC 2 Trust Service Criteria and ISO 27001:2022 controls.

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

This document provides a detailed mapping between SOC 2 Trust Service Criteria (TSC) and ISO 27001:2022 controls to:
- Enable organizations to leverage existing ISO 27001 controls for SOC 2 compliance
- Identify gaps when expanding from one framework to another
- Optimize evidence collection for dual compliance
- Streamline audit preparation

### 1.2 Mapping Legend

| Symbol | Meaning |
|--------|---------|
| ● | Strong alignment - control directly addresses criteria |
| ◐ | Partial alignment - control partially addresses criteria |
| ○ | Weak alignment - control tangentially related |

### 1.3 Coverage Summary

| SOC 2 Category | ISO 27001 Coverage |
|----------------|-------------------|
| CC1 - Control Environment | 85% |
| CC2 - Communication | 90% |
| CC3 - Risk Assessment | 95% |
| CC4 - Monitoring | 85% |
| CC5 - Control Activities | 90% |
| CC6 - Logical/Physical Access | 95% |
| CC7 - System Operations | 90% |
| CC8 - Change Management | 95% |
| CC9 - Risk Mitigation | 85% |
| Availability | 80% |
| Processing Integrity | 75% |
| Confidentiality | 90% |
| Privacy | 70% |

---

## 2. Common Criteria Mapping

### CC1 - Control Environment

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC1.1** | COSO Principle 1: Demonstrates commitment to integrity and ethical values | 5.1 (Policies), 5.4 (Management responsibilities), A.5.1 (Policies for information security) | ● |
| **CC1.2** | COSO Principle 2: Board exercises oversight responsibility | 5.1 (Leadership), A.5.1 (Policies), A.5.4 (Management responsibilities) | ◐ |
| **CC1.3** | COSO Principle 3: Management establishes structures, reporting lines, authorities | 5.3 (Roles and responsibilities), A.5.2 (Roles and responsibilities), A.5.3 (Segregation of duties) | ● |
| **CC1.4** | COSO Principle 4: Demonstrates commitment to competence | 7.2 (Competence), A.6.3 (Information security awareness) | ● |
| **CC1.5** | COSO Principle 5: Enforces accountability | 5.3 (Roles), 9.1 (Monitoring), A.5.2 (Roles) | ◐ |

**Implementation Notes:**
- ISO 27001 Clause 5 (Leadership) covers most CC1 requirements
- Board oversight may require additional documentation beyond ISO 27001
- HR policies and performance management supplement ISO controls

---

### CC2 - Communication and Information

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC2.1** | COSO Principle 13: Obtains or generates relevant, quality information | 7.5 (Documented information), A.5.1 (Policies), A.5.37 (Documented procedures) | ● |
| **CC2.2** | COSO Principle 14: Internally communicates information | 7.4 (Communication), A.6.3 (Awareness), A.5.1 (Policies) | ● |
| **CC2.3** | COSO Principle 15: Communicates with external parties | 7.4 (Communication), A.5.5 (Contact with authorities), A.5.6 (Contact with special interest groups) | ● |

**Implementation Notes:**
- ISO 27001 Clause 7.4 requires communication planning
- Security awareness training addresses internal communication
- External communication includes authorities, customers, and stakeholders

---

### CC3 - Risk Assessment

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC3.1** | COSO Principle 6: Specifies suitable objectives | 6.2 (Information security objectives), 4.1 (Context), 4.2 (Interested parties) | ● |
| **CC3.2** | COSO Principle 7: Identifies and analyzes risk | 6.1.2 (Risk assessment), 8.2 (Risk assessment), A.5.7 (Threat intelligence) | ● |
| **CC3.3** | COSO Principle 8: Assesses fraud risk | 6.1.2 (Risk assessment) - must include fraud scenarios | ◐ |
| **CC3.4** | COSO Principle 9: Identifies and analyzes significant change | 6.1.2 (Risk assessment), 8.1 (Planning), A.5.27 (Learning from incidents) | ● |

**Implementation Notes:**
- ISO 27001 risk assessment process directly supports CC3
- Fraud risk may need explicit inclusion in risk assessment scope
- Change management should trigger risk re-assessment

---

### CC4 - Monitoring Activities

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC4.1** | COSO Principle 16: Selects, develops, and performs ongoing/separate evaluations | 9.1 (Monitoring), 9.2 (Internal audit), 9.3 (Management review), A.8.16 (Monitoring activities) | ● |
| **CC4.2** | COSO Principle 17: Evaluates and communicates deficiencies | 9.2 (Internal audit), 10.1 (Nonconformity), 10.2 (Corrective action) | ● |

**Implementation Notes:**
- ISO 27001 internal audit program satisfies evaluation requirements
- Management review addresses deficiency communication
- Continuous monitoring may require additional technical controls

---

### CC5 - Control Activities

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC5.1** | COSO Principle 10: Selects and develops control activities | 6.1.3 (Risk treatment), 8.1 (Planning), A.5.1 (Policies) | ● |
| **CC5.2** | COSO Principle 11: Selects and develops technology controls | A.8.1-A.8.34 (Technology controls), 8.1 (Operational planning) | ● |
| **CC5.3** | COSO Principle 12: Deploys through policies and procedures | 7.5 (Documented information), A.5.1 (Policies), A.5.37 (Procedures) | ● |

**Implementation Notes:**
- Annex A technology controls provide extensive coverage
- Policy hierarchy should be documented
- Procedure documentation demonstrates deployment

---

### CC6 - Logical and Physical Access Controls

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC6.1** | Implements logical access security software, infrastructure, and architectures | A.5.15 (Access control), A.8.2 (Privileged access), A.8.3 (Access restriction), A.8.20 (Networks security), A.8.21 (Web services security), A.8.24 (Cryptography) | ● |
| **CC6.2** | Prior to granting access, registers and authorizes new users | A.5.16 (Identity management), A.5.17 (Authentication), A.5.18 (Access rights) | ● |
| **CC6.3** | Removes access to protected assets when appropriate | A.5.18 (Access rights), A.6.5 (Termination responsibilities) | ● |
| **CC6.4** | Restricts physical access | A.7.1 (Physical security perimeters), A.7.2 (Physical entry), A.7.3 (Securing offices), A.7.4 (Physical security monitoring) | ● |
| **CC6.5** | Disposes of assets securely | A.7.14 (Secure disposal), A.7.10 (Storage media) | ● |
| **CC6.6** | Protects against threats outside system boundaries | A.8.20 (Networks security), A.8.21 (Web services), A.8.22 (Network segregation), A.5.14 (Information transfer) | ● |
| **CC6.7** | Restricts transmission, movement, and removal of information | A.5.14 (Information transfer), A.8.12 (Data leakage prevention), A.7.9 (Off-premises security) | ● |
| **CC6.8** | Controls against malware, ransomware, and other threats | A.8.7 (Protection against malware), A.8.8 (Vulnerability management) | ● |

**Implementation Notes:**
- ISO 27001 provides comprehensive access control coverage
- Physical security controls in A.7 align directly with CC6.4
- Network and endpoint security controls support CC6.5-CC6.8

---

### CC7 - System Operations

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC7.1** | Detects and monitors security events and anomalies | A.8.15 (Logging), A.8.16 (Monitoring activities), A.5.7 (Threat intelligence) | ● |
| **CC7.2** | Monitors system components for anomalies | A.8.16 (Monitoring), A.8.15 (Logging), A.8.17 (Clock synchronization) | ● |
| **CC7.3** | Evaluates security events to determine impact | A.5.25 (Assessment of events), A.5.24 (Incident planning) | ● |
| **CC7.4** | Responds to identified security incidents | A.5.26 (Response to incidents), A.5.24 (Incident planning), A.5.5 (Contact with authorities) | ● |
| **CC7.5** | Recovers from identified security incidents | A.5.27 (Learning from incidents), A.5.29 (ICT readiness), A.5.30 (ICT readiness for continuity) | ● |

**Implementation Notes:**
- Incident response requirements align well
- SIEM/logging controls support detection capabilities
- Business continuity planning supports recovery

---

### CC8 - Change Management

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC8.1** | Authorizes, designs, develops, configures, documents, tests, approves, and implements changes | A.8.32 (Change management), A.8.9 (Configuration management), A.8.25 (Secure development lifecycle), A.8.29 (Security testing), A.8.31 (Separation of environments) | ● |

**Implementation Notes:**
- A.8.32 directly addresses change management
- Secure development lifecycle covers application changes
- Configuration management supports infrastructure changes

---

### CC9 - Risk Mitigation

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **CC9.1** | Identifies, selects, and develops risk mitigation activities for risks from business partners, vendors, and third parties | A.5.19 (Supplier relationships), A.5.20 (Addressing security in agreements), A.5.21 (ICT supply chain), A.5.22 (Monitoring suppliers), A.5.23 (Cloud services) | ● |
| **CC9.2** | Assesses and manages risks from vendors and business partners | A.5.19-A.5.23 (Supplier relationship controls), 8.1 (Operational planning) | ● |

**Implementation Notes:**
- ISO 27001 supplier controls directly support CC9
- Risk assessment should include third-party risks
- Ongoing monitoring of vendor compliance required

---

## 3. Availability Criteria Mapping

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **A1.1** | Maintains, monitors, and evaluates current processing capacity | A.8.6 (Capacity management), A.8.16 (Monitoring) | ● |
| **A1.2** | Authorizes, designs, develops, implements, operates, and monitors environmental protections | A.7.5 (Protecting against physical threats), A.7.8 (Equipment siting), A.7.11 (Supporting utilities), A.7.12 (Cabling security) | ● |
| **A1.3** | Tests recovery plan procedures | A.5.30 (ICT readiness for continuity), A.5.29 (ICT readiness during disruption) | ● |

**Implementation Notes:**
- Capacity management controls support A1.1
- Physical environmental controls address A1.2
- Business continuity testing addresses A1.3
- SLA management may require additional documentation

---

## 4. Processing Integrity Mapping

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **PI1.1** | Obtains or generates, uses, and communicates relevant quality information regarding processing objectives | A.8.33 (Test information), A.5.37 (Documented procedures) | ◐ |
| **PI1.2** | Implements policies and procedures over system processing | A.5.37 (Documented procedures), A.8.25 (Secure development) | ◐ |
| **PI1.3** | Implements policies and procedures for input, processing, and output | A.8.25 (Secure development), A.8.28 (Secure coding) | ◐ |
| **PI1.4** | Implements policies and procedures to address processing errors | A.8.25 (Secure development), A.5.26 (Incident response) | ◐ |
| **PI1.5** | Implements policies and procedures to retain information | A.5.33 (Protection of records), A.5.34 (Privacy and PII) | ◐ |

**Implementation Notes:**
- Processing integrity has partial ISO 27001 alignment
- Additional application-level controls typically needed
- Data quality controls may require supplementation

---

## 5. Confidentiality Mapping

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **C1.1** | Identifies and maintains confidential information | A.5.12 (Classification), A.5.13 (Labeling), A.5.33 (Records protection) | ● |
| **C1.2** | Disposes of confidential information | A.7.14 (Secure disposal), A.7.10 (Storage media), A.8.10 (Information deletion) | ● |

**Implementation Notes:**
- Classification controls directly support confidentiality
- Disposal procedures cover secure destruction
- Access restrictions inherit from CC6 mapping

---

## 6. Privacy Mapping

| TSC Criteria | Description | ISO 27001 Controls | Alignment |
|--------------|-------------|-------------------|-----------|
| **P1.1** | Privacy notice regarding collection, use, and retention | A.5.34 (Privacy and PII) | ◐ |
| **P2.1** | Communicates choices to data subjects | A.5.34 (Privacy and PII) | ◐ |
| **P3.1** | Collects personal information consistent with objectives | A.5.34 (Privacy and PII) | ◐ |
| **P3.2** | Collects personal information only for identified purposes | A.5.34 (Privacy and PII) | ◐ |
| **P4.1** | Uses personal information consistent with objectives | A.5.34 (Privacy and PII) | ◐ |
| **P4.2** | Retains personal information consistent with objectives | A.5.34 (Privacy and PII), A.5.33 (Records protection) | ◐ |
| **P4.3** | Disposes of personal information to meet objectives | A.8.10 (Information deletion), A.7.14 (Secure disposal) | ● |
| **P5.1** | Grants access to data subjects | A.5.34 (Privacy and PII) | ◐ |
| **P5.2** | Corrects or updates personal information | A.5.34 (Privacy and PII) | ◐ |
| **P6.1** | Discloses personal information with consent | A.5.34 (Privacy and PII), A.5.14 (Information transfer) | ◐ |
| **P6.2** | Creates and retains records of disclosures | A.5.33 (Records protection) | ◐ |
| **P6.3** | Provides notification of disclosures | A.5.34 (Privacy and PII) | ◐ |
| **P6.4** | Discloses personal information to authorized third parties | A.5.19 (Supplier relationships), A.5.14 (Information transfer) | ◐ |
| **P6.5** | Discloses personal information for legal purposes | A.5.5 (Contact with authorities), A.5.31 (Legal requirements) | ◐ |
| **P6.6** | Changes to privacy practices are communicated | A.5.34 (Privacy and PII), 7.4 (Communication) | ◐ |
| **P7.1** | Collects information about quality of personal information | A.5.34 (Privacy and PII) | ○ |
| **P8.1** | Communicates privacy incidents | A.5.26 (Incident response), A.5.34 (Privacy and PII) | ◐ |

**Implementation Notes:**
- Privacy criteria have limited ISO 27001 coverage
- A.5.34 provides foundation but not detailed requirements
- GDPR/privacy-specific controls typically required
- Privacy-specific policies and procedures needed

---

## 7. Detailed Control Mapping Matrix

### ISO 27001 Clause Controls → SOC 2 Mapping

| ISO 27001 Clause | SOC 2 Criteria |
|------------------|----------------|
| 4.1 Understanding the organization | CC3.1 |
| 4.2 Interested parties | CC3.1, CC2.3 |
| 4.3 Scope | CC1.3 |
| 4.4 ISMS | CC1.1, CC5.1 |
| 5.1 Leadership | CC1.1, CC1.2 |
| 5.2 Policy | CC1.1, CC5.3 |
| 5.3 Roles and responsibilities | CC1.3, CC1.5 |
| 6.1 Risk assessment | CC3.2, CC3.3, CC3.4 |
| 6.2 Objectives | CC3.1 |
| 6.3 Planning changes | CC3.4, CC8.1 |
| 7.1 Resources | CC1.4 |
| 7.2 Competence | CC1.4 |
| 7.3 Awareness | CC2.2 |
| 7.4 Communication | CC2.1, CC2.2, CC2.3 |
| 7.5 Documented information | CC2.1, CC5.3 |
| 8.1 Operational planning | CC5.1, CC5.2 |
| 8.2 Risk assessment | CC3.2 |
| 8.3 Risk treatment | CC5.1 |
| 9.1 Monitoring | CC4.1 |
| 9.2 Internal audit | CC4.1, CC4.2 |
| 9.3 Management review | CC4.1, CC4.2 |
| 10.1 Nonconformity | CC4.2 |
| 10.2 Continual improvement | CC4.2 |

### ISO 27001 Annex A Controls → SOC 2 Mapping

| ISO 27001 Control | SOC 2 Criteria |
|-------------------|----------------|
| A.5.1 Policies | CC1.1, CC2.1, CC5.3 |
| A.5.2 Roles and responsibilities | CC1.3, CC1.5 |
| A.5.3 Segregation of duties | CC1.3, CC5.2 |
| A.5.4 Management responsibilities | CC1.1, CC1.2 |
| A.5.5 Contact with authorities | CC2.3, CC7.4 |
| A.5.6 Contact with special interest groups | CC2.3 |
| A.5.7 Threat intelligence | CC3.2, CC7.1 |
| A.5.8 Project management security | CC5.1 |
| A.5.9 Asset inventory | CC6.1 |
| A.5.10 Acceptable use | CC5.3 |
| A.5.11 Return of assets | CC6.3 |
| A.5.12 Classification | C1.1, CC6.1 |
| A.5.13 Labeling | C1.1 |
| A.5.14 Information transfer | CC6.6, CC6.7 |
| A.5.15 Access control | CC6.1, CC6.2 |
| A.5.16 Identity management | CC6.2 |
| A.5.17 Authentication | CC6.1, CC6.2 |
| A.5.18 Access rights | CC6.2, CC6.3 |
| A.5.19 Supplier relationships | CC9.1, CC9.2 |
| A.5.20 Supplier agreements | CC9.1, CC9.2 |
| A.5.21 ICT supply chain | CC9.1 |
| A.5.22 Supplier monitoring | CC9.2 |
| A.5.23 Cloud services | CC9.1, CC9.2 |
| A.5.24 Incident planning | CC7.3, CC7.4 |
| A.5.25 Assessment of events | CC7.3 |
| A.5.26 Response to incidents | CC7.4 |
| A.5.27 Learning from incidents | CC7.5, CC3.4 |
| A.5.28 Evidence collection | CC7.4 |
| A.5.29 ICT readiness during disruption | A1.3, CC7.5 |
| A.5.30 ICT readiness for continuity | A1.3, CC7.5 |
| A.5.31 Legal requirements | CC3.1, P6.5 |
| A.5.32 Intellectual property | C1.1 |
| A.5.33 Protection of records | C1.1, P4.2, P6.2 |
| A.5.34 Privacy and PII | P1-P8 (all privacy) |
| A.5.35 Independent review | CC4.1 |
| A.5.36 Compliance with policies | CC4.1, CC5.3 |
| A.5.37 Documented procedures | CC5.3, PI1.2 |
| A.6.1 Screening | CC1.4 |
| A.6.2 Terms of employment | CC1.1, CC2.2 |
| A.6.3 Awareness | CC1.4, CC2.2 |
| A.6.4 Disciplinary process | CC1.5 |
| A.6.5 Termination responsibilities | CC6.3 |
| A.6.6 Confidentiality agreements | C1.1, CC1.1 |
| A.6.7 Remote working | CC6.1 |
| A.6.8 Event reporting | CC7.1, CC7.3 |
| A.7.1 Physical security perimeters | CC6.4 |
| A.7.2 Physical entry | CC6.4 |
| A.7.3 Securing offices | CC6.4 |
| A.7.4 Physical security monitoring | CC6.4, CC7.1 |
| A.7.5 Physical threats protection | A1.2 |
| A.7.6 Working in secure areas | CC6.4 |
| A.7.7 Clear desk | CC6.4, C1.1 |
| A.7.8 Equipment siting | A1.2 |
| A.7.9 Off-premises security | CC6.7 |
| A.7.10 Storage media | CC6.5, C1.2 |
| A.7.11 Supporting utilities | A1.2 |
| A.7.12 Cabling security | A1.2 |
| A.7.13 Equipment maintenance | A1.2 |
| A.7.14 Secure disposal | CC6.5, C1.2 |
| A.8.1 User endpoint devices | CC6.1 |
| A.8.2 Privileged access rights | CC6.1, CC6.2 |
| A.8.3 Information access restriction | CC6.1 |
| A.8.4 Access to source code | CC6.1 |
| A.8.5 Secure authentication | CC6.1, CC6.2 |
| A.8.6 Capacity management | A1.1 |
| A.8.7 Protection against malware | CC6.8 |
| A.8.8 Technical vulnerabilities | CC6.8, CC4.1 |
| A.8.9 Configuration management | CC8.1 |
| A.8.10 Information deletion | C1.2, P4.3 |
| A.8.11 Data masking | CC6.1, C1.1 |
| A.8.12 Data leakage prevention | CC6.7 |
| A.8.13 Information backup | A1.3, CC7.5 |
| A.8.14 Redundancy | A1.2, A1.3 |
| A.8.15 Logging | CC7.1, CC7.2 |
| A.8.16 Monitoring activities | CC4.1, CC7.1, CC7.2 |
| A.8.17 Clock synchronization | CC7.2 |
| A.8.18 Privileged utility programs | CC6.1 |
| A.8.19 Software installation | CC8.1 |
| A.8.20 Networks security | CC6.1, CC6.6 |
| A.8.21 Web services security | CC6.1, CC6.6 |
| A.8.22 Network segregation | CC6.6 |
| A.8.23 Web filtering | CC6.6, CC6.8 |
| A.8.24 Cryptography | CC6.1, CC6.7 |
| A.8.25 Secure development lifecycle | CC8.1 |
| A.8.26 Application security requirements | CC8.1 |
| A.8.27 Secure architecture | CC5.2, CC6.1 |
| A.8.28 Secure coding | CC8.1, PI1.3 |
| A.8.29 Security testing | CC8.1, CC4.1 |
| A.8.30 Outsourced development | CC9.1 |
| A.8.31 Separation of environments | CC8.1 |
| A.8.32 Change management | CC8.1 |
| A.8.33 Test information | PI1.1 |
| A.8.34 Audit testing protection | CC4.1 |

---

## 8. Gap Analysis Template

Use this template to identify gaps when mapping between frameworks:

| SOC 2 Criteria | Required Evidence | ISO 27001 Control | Gap Identified | Remediation Required |
|----------------|-------------------|-------------------|----------------|---------------------|
| CC1.1 | Code of conduct | A.5.1 | | |
| CC1.2 | Board oversight | Limited coverage | Need board charter | Create governance documentation |
| CC3.3 | Fraud risk assessment | 6.1.2 (partial) | Explicit fraud risk | Include fraud scenarios in RA |
| PI1.1-PI1.5 | Processing controls | Partial | Data quality controls | Implement application controls |
| P1.1-P8.1 | Privacy controls | A.5.34 (partial) | Comprehensive privacy | Implement privacy program |

---

## 9. Dual Compliance Strategy

### 9.1 Leveraging ISO 27001 for SOC 2

Organizations with ISO 27001 certification can leverage:

| ISO 27001 Asset | SOC 2 Application |
|-----------------|-------------------|
| ISMS policies | Forms basis of SOC 2 policy requirements |
| Risk assessment | Supports CC3 requirements with fraud additions |
| Statement of Applicability | Maps to Trust Service Criteria |
| Internal audit results | Evidence for CC4 monitoring requirements |
| Management review | Demonstrates governance oversight |
| Incident records | Supports CC7 incident response |
| Access control records | Supports CC6 logical access |
| Change records | Supports CC8 change management |

### 9.2 Additional SOC 2 Requirements

| Area | Additional Requirements |
|------|------------------------|
| Board oversight | Explicit board charter and meeting minutes |
| Fraud risk | Documented fraud risk assessment |
| System description | SOC 2-specific system description document |
| Subservice organizations | Carve-out or inclusive method documentation |
| Privacy | Comprehensive privacy program (if P criteria in scope) |
| Processing integrity | Application-level processing controls |
| Availability SLAs | Documented commitments and monitoring |

### 9.3 Evidence Collection Efficiency

| Evidence Type | Collect Once For |
|---------------|------------------|
| Security policies | ISO 27001 A.5.1, SOC 2 CC1, CC2, CC5 |
| Risk assessment | ISO 27001 6.1.2, SOC 2 CC3 |
| Access reviews | ISO 27001 A.5.18, SOC 2 CC6.3 |
| Incident records | ISO 27001 A.5.24-27, SOC 2 CC7.3-7.5 |
| Change tickets | ISO 27001 A.8.32, SOC 2 CC8.1 |
| Vendor assessments | ISO 27001 A.5.19-22, SOC 2 CC9 |
| Training records | ISO 27001 A.6.3, SOC 2 CC1.4, CC2.2 |
| Audit reports | ISO 27001 9.2, SOC 2 CC4.1 |

---

## 10. Related Documents

- [SOC 2 Guide](./soc2-guide.md)
- [Trust Service Criteria Reference](./trust-services-criteria.md)
- [SOC 2 Readiness Checklist](./soc2-readiness-checklist.md)
- [SOC 2 Evidence Guide](./soc2-evidence-guide.md)
- [SOC 2 Gap Assessment](./soc2-gap-assessment.md)
- [ISO 27001 Controls Guide](../iso-27001/annex-a-controls-guide.md)

---

## 11. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to SOC 2](./README.md) | [Back to Frameworks](../README.md)

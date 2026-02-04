# NIST CSF 2.0 to ISO 27001:2022 Mapping

A comprehensive mapping between NIST Cybersecurity Framework 2.0 and ISO 27001:2022 controls.

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

This document provides a mapping between NIST CSF 2.0 subcategories and ISO 27001:2022 controls to help organizations:

- Understand overlaps between frameworks
- Leverage existing ISO 27001 implementations for CSF
- Identify gaps when using both frameworks
- Create unified compliance programs

### 1.2 How to Use This Mapping

| If you have... | Use this mapping to... |
|----------------|------------------------|
| ISO 27001 certification | Understand CSF coverage from existing controls |
| CSF implementation | Identify ISO 27001 controls that align |
| Both requirements | Create unified control framework |
| Gap analysis needs | Find unmapped areas requiring attention |

---

## 2. Framework Comparison

### 2.1 Structural Comparison

| Aspect | NIST CSF 2.0 | ISO 27001:2022 |
|--------|--------------|----------------|
| **Structure** | Functions → Categories → Subcategories | Clauses + Annex A Controls |
| **Functions/Domains** | 6 | 4 themes (Organizational, People, Physical, Technical) |
| **Categories/Control Groups** | 22 | 93 controls |
| **Subcategories/Controls** | 106 | 93 |
| **Mandatory** | Voluntary | Certification available |
| **Risk Approach** | Tiers and Profiles | Risk assessment required |
| **Governance** | Explicit GOVERN function | Clauses 4-10 |

### 2.2 Key Differences

| Area | NIST CSF | ISO 27001 |
|------|----------|-----------|
| **Scope** | Cybersecurity focused | Information security (broader) |
| **Certification** | No formal certification | Third-party certification |
| **Prescriptiveness** | Outcome-based, flexible | More prescriptive controls |
| **Supply Chain** | Dedicated category (GV.SC) | Controls A.5.19-5.23 |
| **Governance** | Explicit function | Part of management system |

---

## 3. GOVERN Function Mapping

### GV.OC - Organizational Context

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| GV.OC-01 | Organizational mission understood | 4.1 Understanding the organization |
| GV.OC-02 | Internal/external stakeholders understood | 4.2 Interested parties |
| GV.OC-03 | Legal/regulatory requirements managed | A.5.31 Legal requirements, A.5.32 IP rights, A.5.33 Records protection, A.5.34 Privacy |
| GV.OC-04 | Critical objectives communicated | 4.1, 6.2 Objectives |
| GV.OC-05 | Dependencies understood | 4.1, A.5.19-5.23 Supplier relationships |

### GV.RM - Risk Management Strategy

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| GV.RM-01 | Risk management objectives established | 6.1.1 Risk assessment, 6.1.2 Risk treatment |
| GV.RM-02 | Risk appetite/tolerance established | 6.1.2 Risk treatment options |
| GV.RM-03 | Cybersecurity in enterprise risk management | 6.1 Actions to address risks |
| GV.RM-04 | Strategic direction for risk response | 6.1.3 Risk treatment plan |
| GV.RM-05 | Communication lines established | 7.4 Communication |
| GV.RM-06 | Standardized risk calculation method | 6.1.2 Risk assessment methodology |
| GV.RM-07 | Strategic opportunities characterized | 6.1 Actions to address opportunities |

### GV.RR - Roles, Responsibilities, and Authorities

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| GV.RR-01 | Leadership responsible, security culture | 5.1 Leadership commitment, A.5.4 Management responsibilities |
| GV.RR-02 | Roles and responsibilities established | 5.3 Roles and responsibilities, A.5.2 Information security roles |
| GV.RR-03 | Adequate resources allocated | 7.1 Resources |
| GV.RR-04 | Cybersecurity in HR practices | A.6.1-6.6 People controls |

### GV.PO - Policy

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| GV.PO-01 | Policy established based on context | 5.2 Policy, A.5.1 Information security policies |
| GV.PO-02 | Policy reviewed, updated, enforced | A.5.1 Policies, 7.5 Documented information |

### GV.OV - Oversight

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| GV.OV-01 | Strategy outcomes reviewed | 9.1 Monitoring and measurement, 9.3 Management review |
| GV.OV-02 | Strategy reviewed and adjusted | 9.3 Management review, 10.1 Continual improvement |
| GV.OV-03 | Performance evaluated and reviewed | 9.1 Monitoring, 9.2 Internal audit |

### GV.SC - Cybersecurity Supply Chain Risk Management

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| GV.SC-01 | Supply chain risk management program | A.5.19 Supplier relationships |
| GV.SC-02 | Supplier roles established | A.5.20 Addressing security in agreements |
| GV.SC-03 | Supply chain integrated into risk management | A.5.21 Managing security in ICT supply chain |
| GV.SC-04 | Suppliers known and prioritized | A.5.19, A.5.22 Monitoring of suppliers |
| GV.SC-05 | Requirements in contracts | A.5.20 Security in agreements |
| GV.SC-06 | Due diligence before relationships | A.5.19, A.5.21 Supply chain security |
| GV.SC-07 | Supplier risks assessed and monitored | A.5.22 Monitoring and review |
| GV.SC-08 | Suppliers in incident planning | A.5.23 Security for cloud services |
| GV.SC-09 | Supply chain practices integrated | A.5.21 ICT supply chain |
| GV.SC-10 | Provisions for relationship conclusion | A.5.20 Agreements |

---

## 4. IDENTIFY Function Mapping

### ID.AM - Asset Management

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| ID.AM-01 | Hardware inventory maintained | A.5.9 Inventory of assets |
| ID.AM-02 | Software/services inventory maintained | A.5.9 Inventory of assets |
| ID.AM-03 | Network/data flows documented | A.5.9, A.8.20 Network security |
| ID.AM-04 | Supplier services inventoried | A.5.9, A.5.19 Supplier relationships |
| ID.AM-05 | Assets prioritized by criticality | A.5.9, A.5.12 Classification |
| ID.AM-07 | Data inventory maintained | A.5.9, A.5.12 Classification, A.5.13 Labeling |
| ID.AM-08 | Lifecycle management | A.5.11 Return of assets, A.8.10 Information deletion |

### ID.RA - Risk Assessment

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| ID.RA-01 | Vulnerabilities identified | A.8.8 Vulnerability management |
| ID.RA-02 | Threat intelligence received | A.5.7 Threat intelligence |
| ID.RA-03 | Threats identified and recorded | 6.1.2 Risk assessment |
| ID.RA-04 | Impacts and likelihoods identified | 6.1.2 Risk assessment |
| ID.RA-05 | Inherent risk understood | 6.1.2 Risk assessment |
| ID.RA-06 | Risk responses prioritized | 6.1.3 Risk treatment |
| ID.RA-07 | Changes assessed for risk impact | A.8.32 Change management |
| ID.RA-08 | Vulnerability disclosure process | A.8.8 Vulnerability management |
| ID.RA-09 | Hardware/software integrity assessed | A.8.25-8.31 Secure development |
| ID.RA-10 | Critical suppliers assessed | A.5.19, A.5.21 Supplier security |

### ID.IM - Improvement

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| ID.IM-01 | Improvements from evaluations | 10.1 Continual improvement |
| ID.IM-02 | Improvements from security tests | A.8.8 Vulnerability management, 10.1 Improvement |
| ID.IM-03 | Improvements from operations | 10.1 Continual improvement |
| ID.IM-04 | Plans established and improved | A.5.24 Incident planning, 10.1 Improvement |

---

## 5. PROTECT Function Mapping

### PR.AA - Identity Management, Authentication, Access Control

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| PR.AA-01 | Identities and credentials managed | A.5.16 Identity management, A.5.17 Authentication |
| PR.AA-02 | Identities proofed and bound | A.5.16 Identity management |
| PR.AA-03 | Authentication implemented | A.5.17 Authentication information, A.8.5 Secure authentication |
| PR.AA-04 | Identity assertions protected | A.5.17, A.8.5 Secure authentication |
| PR.AA-05 | Access permissions managed | A.5.15 Access control, A.5.18 Access rights |
| PR.AA-06 | Physical access managed | A.7.1-7.4 Physical security |

### PR.AT - Awareness and Training

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| PR.AT-01 | Personnel provided awareness/training | A.6.3 Security awareness |
| PR.AT-02 | Specialized role training | A.6.3 Security awareness |

### PR.DS - Data Security

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| PR.DS-01 | Data-at-rest protected | A.8.24 Cryptography, A.8.10 Information deletion |
| PR.DS-02 | Data-in-transit protected | A.8.24 Cryptography, A.5.14 Information transfer |
| PR.DS-10 | Data-in-use protected | A.8.11 Data masking, A.8.12 Data leakage prevention |
| PR.DS-11 | Backups maintained and tested | A.8.13 Information backup |

### PR.PS - Platform Security

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| PR.PS-01 | Configuration management | A.8.9 Configuration management |
| PR.PS-02 | Software maintained | A.8.19 Software installation, A.8.8 Vulnerability management |
| PR.PS-03 | Hardware maintained | A.7.13 Equipment maintenance |
| PR.PS-04 | Log records generated | A.8.15 Logging, A.8.16 Monitoring |
| PR.PS-05 | Unauthorized software prevented | A.8.19 Software installation |
| PR.PS-06 | Secure development practices | A.8.25-8.31 Secure development lifecycle |

### PR.IR - Technology Infrastructure Resilience

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| PR.IR-01 | Networks protected from unauthorized access | A.8.20 Network security, A.8.21 Web filtering, A.8.22 Network segregation |
| PR.IR-02 | Assets protected from environmental threats | A.7.5 Physical environmental security, A.7.8-7.11 Equipment protection |
| PR.IR-03 | Resilience mechanisms implemented | A.8.14 Redundancy |
| PR.IR-04 | Adequate resource capacity | A.8.6 Capacity management |

---

## 6. DETECT Function Mapping

### DE.CM - Continuous Monitoring

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| DE.CM-01 | Networks monitored | A.8.16 Monitoring activities |
| DE.CM-02 | Physical environment monitored | A.7.4 Physical security monitoring |
| DE.CM-03 | Personnel activity monitored | A.8.15 Logging, A.8.16 Monitoring |
| DE.CM-06 | External services monitored | A.5.22 Monitoring suppliers |
| DE.CM-09 | Computing resources monitored | A.8.16 Monitoring activities |

### DE.AE - Adverse Event Analysis

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| DE.AE-02 | Events analyzed | A.8.16 Monitoring, A.5.25 Assessment of events |
| DE.AE-03 | Information correlated | A.8.16 Monitoring activities |
| DE.AE-04 | Impact and scope understood | A.5.25 Assessment of events |
| DE.AE-06 | Information provided to staff | A.5.25, A.5.26 Response to incidents |
| DE.AE-07 | Threat intelligence integrated | A.5.7 Threat intelligence |
| DE.AE-08 | Incidents declared | A.5.25 Assessment and decision |

---

## 7. RESPOND Function Mapping

### RS.MA - Incident Management

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| RS.MA-01 | Incident response plan executed | A.5.26 Response to incidents |
| RS.MA-02 | Reports triaged and validated | A.5.25 Assessment of events |
| RS.MA-03 | Incidents categorized/prioritized | A.5.25 Assessment and decision |
| RS.MA-04 | Incidents escalated as needed | A.5.26 Response to incidents |
| RS.MA-05 | Recovery criteria applied | A.5.26, A.5.29 Business continuity |

### RS.AN - Incident Analysis

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| RS.AN-03 | Analysis performed | A.5.27 Learning from incidents |
| RS.AN-06 | Investigation actions recorded | A.5.27, A.5.28 Evidence collection |
| RS.AN-07 | Data collected and preserved | A.5.28 Collection of evidence |
| RS.AN-08 | Magnitude estimated | A.5.25 Assessment of events |

### RS.CO - Incident Response Reporting and Communication

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| RS.CO-02 | Stakeholders notified | A.5.26 Response to incidents |
| RS.CO-03 | Information shared | 7.4 Communication |

### RS.MI - Incident Mitigation

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| RS.MI-01 | Incidents contained | A.5.26 Response to incidents |
| RS.MI-02 | Incidents eradicated | A.5.26 Response to incidents |

---

## 8. RECOVER Function Mapping

### RC.RP - Incident Recovery Plan Execution

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| RC.RP-01 | Recovery plan executed | A.5.29-5.30 Business continuity |
| RC.RP-02 | Recovery actions prioritized | A.5.29 ICT readiness |
| RC.RP-03 | Backup integrity verified | A.8.13 Information backup |
| RC.RP-04 | Critical functions considered | A.5.29, A.5.30 Continuity planning |
| RC.RP-05 | Integrity verified, operations restored | A.5.30, A.8.13 Backup |
| RC.RP-06 | Recovery end declared | A.5.27 Learning from incidents |

### RC.CO - Incident Recovery Communication

| CSF Subcategory | Description | ISO 27001:2022 Controls |
|-----------------|-------------|------------------------|
| RC.CO-03 | Progress communicated | 7.4 Communication |
| RC.CO-04 | Public updates shared | 7.4 Communication |

---

## 9. Coverage Summary

### 9.1 CSF Coverage by ISO 27001

| CSF Function | Subcategories | Fully Mapped | Partially Mapped | ISO 27001 Coverage |
|--------------|---------------|--------------|------------------|-------------------|
| GOVERN | 27 | 24 | 3 | 89% |
| IDENTIFY | 17 | 16 | 1 | 94% |
| PROTECT | 19 | 19 | 0 | 100% |
| DETECT | 11 | 10 | 1 | 91% |
| RESPOND | 11 | 11 | 0 | 100% |
| RECOVER | 8 | 7 | 1 | 88% |
| **TOTAL** | **93** | **87** | **6** | **94%** |

### 9.2 ISO 27001 Controls Most Relevant to CSF

| ISO 27001 Control | CSF Functions Covered |
|-------------------|----------------------|
| A.5.1 Information security policies | GV |
| A.5.7 Threat intelligence | ID, DE |
| A.5.9 Inventory of information | ID |
| A.5.15-5.18 Access control | PR |
| A.5.19-5.23 Supplier security | GV |
| A.5.24-5.28 Incident management | RS |
| A.5.29-5.30 Business continuity | RC |
| A.6.3 Security awareness | PR |
| A.8.8 Vulnerability management | ID, PR |
| A.8.15-8.16 Logging/monitoring | PR, DE |

---

## 10. Using Both Frameworks

### 10.1 Complementary Approach

| Scenario | Recommendation |
|----------|----------------|
| ISO 27001 certified, CSF required | Use this mapping to demonstrate CSF alignment |
| CSF implemented, ISO certification needed | Identify ISO-specific requirements not in CSF |
| Starting fresh | Implement ISO 27001 with CSF profile for measurement |
| Multi-framework compliance | Create unified control set using both frameworks |

### 10.2 Gap Areas

Areas where frameworks have different emphasis:

| Area | NIST CSF Focus | ISO 27001 Focus |
|------|----------------|-----------------|
| Governance | Dedicated GOVERN function | Part of management system clauses |
| Supply Chain | Detailed GV.SC category | Five specific controls |
| Profiles/Tiers | Maturity measurement | Not explicitly included |
| Certification | No formal certification | Third-party certification |
| Privacy | Referenced but limited | A.5.34 Privacy protection |

---

## 11. Related Documents

- [NIST CSF 2.0 Guide](./nist-csf-guide.md)
- [CSF Assessment Template](./csf-assessment-template.md)
- [ISO 27001 Controls Reference](../iso-27001/controls/README.md)
- [ISO 27001 Implementation Roadmap](../iso-27001/README.md)

---

## 12. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to NIST CSF](./README.md) | [Back to Frameworks](../README.md)

# International Data Transfers Guide

A guide to lawfully transferring personal data outside the European Economic Area (EEA) under GDPR Chapter V.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., DPO, Privacy Manager] |
| **Classification** | Internal |

---

## 1. Introduction

### 1.1 What is an International Transfer?

An international data transfer occurs when personal data is:
- Sent to a country outside the EEA
- Accessed from a country outside the EEA
- Stored in a country outside the EEA
- Processed by an organization in a country outside the EEA

### 1.2 The EEA

The European Economic Area includes:
- All 27 EU member states
- Iceland, Liechtenstein, Norway

**Note:** The UK is no longer in the EEA but has an adequacy decision (until June 2025, subject to review).

### 1.3 Why Restrictions Exist

GDPR aims to ensure personal data remains protected when it leaves the EEA. Countries outside the EEA may have:
- Weaker data protection laws
- Government surveillance programs
- Limited individual rights
- Inadequate enforcement

---

## 2. Transfer Mechanisms Overview

### 2.1 Available Mechanisms

| Mechanism | GDPR Article | When to Use |
|-----------|--------------|-------------|
| **Adequacy Decision** | 45 | Transfer to "adequate" countries |
| **Standard Contractual Clauses (SCCs)** | 46(2)(c) | Most common mechanism |
| **Binding Corporate Rules (BCRs)** | 46(2)(b) | Intra-group transfers (multinationals) |
| **Codes of Conduct** | 46(2)(e) | Sector-specific, with binding commitments |
| **Certification** | 46(2)(f) | With binding commitments |
| **Derogations** | 49 | Specific situations (limited use) |

### 2.2 Decision Flowchart

```
START: Need to transfer data outside EEA?
         │
         ▼
Is the destination country "adequate"? ──YES──▶ TRANSFER ALLOWED
         │                                       (under adequacy)
         NO
         │
         ▼
Can you use SCCs with the recipient? ────YES──▶ Conduct TIA
         │                                       │
         NO                                      ▼
         │                              Supplementary measures
         ▼                              needed?
Is it an intra-group transfer and ───────YES──▶ USE BCRs
you have approved BCRs?                         (if approved)
         │
         NO
         │
         ▼
Does a derogation apply? ────────────────YES──▶ Document and use
         │                                       derogation
         NO
         │
         ▼
     TRANSFER NOT PERMITTED
```

---

## 3. Adequacy Decisions (Article 45)

### 3.1 What is Adequacy?

The European Commission assesses whether a country provides "essentially equivalent" protection to the EU. If adequate, transfers can occur without additional safeguards.

### 3.2 Countries with Adequacy Decisions

*As of 2024:*

| Country | Decision Date | Notes |
|---------|---------------|-------|
| Andorra | 2010 | Full adequacy |
| Argentina | 2003 | Full adequacy |
| Canada | 2001 | Commercial organizations (PIPEDA) only |
| Faroe Islands | 2010 | Full adequacy |
| Guernsey | 2003 | Full adequacy |
| Israel | 2011 | Full adequacy |
| Isle of Man | 2004 | Full adequacy |
| Japan | 2019 | Full adequacy |
| Jersey | 2008 | Full adequacy |
| New Zealand | 2012 | Full adequacy |
| Republic of Korea | 2022 | Full adequacy |
| Switzerland | 2000 | Full adequacy |
| United Kingdom | 2021 | Until June 2025 (subject to review) |
| United States | 2023 | EU-US Data Privacy Framework (certified orgs only) |
| Uruguay | 2012 | Full adequacy |

### 3.3 EU-US Data Privacy Framework

**Important:** The US adequacy decision only covers transfers to organizations that:
- Have self-certified to the Data Privacy Framework
- Are listed on the DPF List (dataprivacyframework.gov)

**Before transferring to US:**
```
□ Check if recipient is certified on DPF List
□ Verify certification is current
□ Ensure transfer is within scope of certification
□ Document verification
```

---

## 4. Standard Contractual Clauses (SCCs)

### 4.1 What are SCCs?

Standard Contractual Clauses are pre-approved contract terms that provide safeguards for international transfers. They are legally binding on both parties.

### 4.2 Current SCCs (2021)

The European Commission adopted new SCCs on 4 June 2021. There are four modules:

| Module | Scenario |
|--------|----------|
| **Module 1** | Controller to Controller |
| **Module 2** | Controller to Processor |
| **Module 3** | Processor to Processor |
| **Module 4** | Processor to Controller |

### 4.3 Implementing SCCs

**Step 1: Select the correct module**

| You are... | Recipient is... | Module |
|------------|-----------------|--------|
| Controller | Controller | Module 1 |
| Controller | Processor | Module 2 |
| Processor | Sub-processor | Module 3 |
| Processor | Controller | Module 4 |

**Step 2: Complete the annexes**

| Annex | Content |
|-------|---------|
| **Annex I.A** | List of parties |
| **Annex I.B** | Description of transfer (purposes, data, subjects) |
| **Annex I.C** | Competent supervisory authority |
| **Annex II** | Technical and organizational measures |
| **Annex III** | List of sub-processors (Module 2/3) |

**Step 3: Conduct Transfer Impact Assessment (see Section 6)**

**Step 4: Implement supplementary measures if needed**

**Step 5: Execute the SCCs**

### 4.4 SCC Implementation Checklist

```
□ Correct module selected
□ All annexes completed accurately
□ Transfer Impact Assessment completed
□ Supplementary measures identified (if needed)
□ Supplementary measures implemented
□ SCCs signed by both parties
□ Copy retained for records
□ Privacy notice updated
□ RoPA updated
```

---

## 5. Binding Corporate Rules (BCRs)

### 5.1 What are BCRs?

Binding Corporate Rules are internal policies approved by supervisory authorities that allow multinational groups to transfer personal data within the group to countries outside the EEA.

### 5.2 Types of BCRs

| Type | For |
|------|-----|
| **Controller BCRs** | Group companies acting as controllers |
| **Processor BCRs** | Group companies providing processing services |

### 5.3 BCR Requirements

BCRs must include:
- Group structure and contact details
- Data transfers covered
- Legally binding nature
- Application of GDPR principles
- Data subject rights and enforcement
- Cooperation with authorities
- Training requirements
- Complaint handling
- Compliance monitoring

### 5.4 BCR Approval Process

1. Draft BCRs following WP29 guidance
2. Submit to lead supervisory authority
3. Cooperation procedure with other authorities
4. Formal approval decision
5. Implementation across group

**Note:** BCR approval can take 1-2 years and significant resources.

---

## 6. Transfer Impact Assessment (TIA)

### 6.1 When Required

A TIA is required when using:
- Standard Contractual Clauses
- Binding Corporate Rules
- Article 46 derogations in some cases

### 6.2 TIA Process

**Step 1: Map the transfer**

| Element | Details |
|---------|---------|
| Data exporter | [Your organization details] |
| Data importer | [Recipient details] |
| Destination country | [Country] |
| Data transferred | [Categories] |
| Purpose | [Why transfer occurs] |
| Transfer mechanism | [SCCs/BCRs/Other] |

**Step 2: Assess destination country laws**

| Assessment Area | Considerations |
|-----------------|----------------|
| **Surveillance laws** | Government access to data? |
| **Data protection laws** | Adequate protections? |
| **Rule of law** | Independent judiciary? Effective remedies? |
| **International commitments** | Human rights obligations? |
| **Practical application** | How are laws actually enforced? |

**Step 3: Assess the transfer mechanism**

| Question | Answer |
|----------|--------|
| Does the mechanism provide effective protection? | [Assessment] |
| Can the importer comply with the mechanism? | [Assessment] |
| Are there conflicting local laws? | [Assessment] |

**Step 4: Determine if supplementary measures needed**

| If... | Then... |
|-------|---------|
| Transfer mechanism is sufficient | Document and proceed |
| Supplementary measures can fill gaps | Implement and proceed |
| No measures can ensure protection | Transfer cannot occur |

### 6.3 TIA Template

---

#### Transfer Impact Assessment

**Transfer ID:** TIA-[YYYY]-[XXX]
**Date:** [DATE]
**Assessor:** [NAME]
**Approved by:** [NAME/ROLE]

---

##### Section 1: Transfer Details

| Field | Information |
|-------|-------------|
| **Data Exporter** | [Name, address, contact] |
| **Data Importer** | [Name, address, contact] |
| **Destination Country** | [Country] |
| **Transfer Mechanism** | [SCCs/BCRs/Other] |

**Data Being Transferred:**

| Data Category | Data Subjects | Volume | Frequency |
|---------------|---------------|--------|-----------|
| [CATEGORY] | [SUBJECTS] | [VOLUME] | [FREQUENCY] |

**Purpose of Transfer:**
[Describe why data needs to be transferred]

---

##### Section 2: Legal Framework Assessment

**2.1 Laws reviewed:**
- [ ] Data protection/privacy laws
- [ ] Electronic communications laws
- [ ] Surveillance/national security laws
- [ ] Government access laws
- [ ] Other relevant laws: [SPECIFY]

**2.2 Assessment of laws:**

| Factor | Assessment | Risk Level |
|--------|------------|------------|
| Government access | [Description] | [Low/Medium/High] |
| Judicial oversight | [Description] | [Low/Medium/High] |
| Individual remedies | [Description] | [Low/Medium/High] |
| Data protection authority | [Description] | [Low/Medium/High] |
| Human rights protections | [Description] | [Low/Medium/High] |

**2.3 Relevant laws identified:**

| Law/Regulation | Key Provisions | Impact on Transfer |
|----------------|----------------|-------------------|
| [LAW] | [PROVISIONS] | [IMPACT] |

---

##### Section 3: Practical Assessment

| Question | Answer |
|----------|--------|
| Has the importer received government access requests? | [Yes/No/Unknown] |
| Is the data type of interest to authorities? | [Assessment] |
| Is the data encrypted in transit and at rest? | [Yes/No] |
| Does the exporter have visibility of access requests? | [Yes/No] |

---

##### Section 4: Gap Analysis

| Protection Required | Provided by SCCs/BCRs | Gap? |
|---------------------|----------------------|------|
| [PROTECTION] | [Yes/Partial/No] | [Yes/No] |
| [PROTECTION] | [Yes/Partial/No] | [Yes/No] |

---

##### Section 5: Supplementary Measures

| Measure | Type | Gap Addressed |
|---------|------|---------------|
| [MEASURE] | [Technical/Contractual/Organizational] | [GAP] |
| [MEASURE] | [Technical/Contractual/Organizational] | [GAP] |

---

##### Section 6: Conclusion

- [ ] **Transfer may proceed** - Mechanism provides adequate protection
- [ ] **Transfer may proceed with supplementary measures** - Measures documented above
- [ ] **Transfer cannot proceed** - Insufficient protection cannot be remedied

**Reasoning:**
[Explain conclusion]

**Review Date:** [DATE]

---

##### Sign-off

| Role | Name | Date |
|------|------|------|
| Assessor | | |
| DPO/Privacy | | |

---

## 7. Supplementary Measures

### 7.1 Technical Measures

| Measure | Description | Effectiveness |
|---------|-------------|---------------|
| **Encryption** | Strong encryption with keys held by exporter | High - prevents access to plaintext |
| **Pseudonymization** | Data cannot be attributed without additional info | Medium - if key held by exporter |
| **Split processing** | Process sensitive elements in EEA only | High - for elements not transferred |
| **Zero-knowledge proof** | Verify without revealing data | High - where applicable |

### 7.2 Contractual Measures

| Measure | Description |
|---------|-------------|
| **Transparency obligations** | Require importer to notify of access requests |
| **Challenge commitments** | Importer commits to challenge unlawful requests |
| **Notification rights** | Require notification of legal developments |
| **Audit rights** | Right to audit importer's practices |
| **Liability clauses** | Strengthened liability provisions |

### 7.3 Organizational Measures

| Measure | Description |
|---------|-------------|
| **Policies** | Importer's internal policies limiting access |
| **Training** | Staff awareness of transfer requirements |
| **Access controls** | Strict need-to-know access |
| **Documentation** | Records of access and disclosures |
| **Compliance monitoring** | Regular review of importer compliance |

---

## 8. Derogations (Article 49)

### 8.1 When Derogations Apply

Derogations are exceptions for **occasional** transfers when no other mechanism is available.

| Derogation | Conditions | Limitations |
|------------|------------|-------------|
| **Explicit consent** | Informed of risks, specific consent | Must be truly voluntary |
| **Contract with data subject** | Necessary for contract performance | Individual must be party |
| **Contract in data subject's interest** | Contract with third party for their benefit | Must be necessary |
| **Public interest** | Important reasons of public interest | Must be recognized in law |
| **Legal claims** | Establish, exercise, or defend claims | Must be necessary |
| **Vital interests** | Protect life, individual unable to consent | Life-threatening situations |
| **Public register** | Data from legally public register | Subject to access conditions |
| **Compelling legitimate interests** | Not repetitive, limited data subjects | Last resort, notify authority |

### 8.2 Derogation Limitations

- **Occasional only:** Cannot be used for systematic transfers
- **Specific situations:** Must meet precise conditions
- **Document:** Must document justification
- **Notify:** Some require notification to supervisory authority

### 8.3 Derogation Documentation

| Field | Information |
|-------|-------------|
| Derogation relied upon | [Article 49 provision] |
| Justification | [Why derogation applies] |
| Why other mechanisms not possible | [Explanation] |
| Data transferred | [Description] |
| Frequency | [One-time/occasional] |
| Notification to authority | [If required] |

---

## 9. Transfer Register

### 9.1 Template

| Transfer ID | Destination | Recipient | Purpose | Mechanism | TIA Date | Review Date |
|-------------|-------------|-----------|---------|-----------|----------|-------------|
| [ID] | [COUNTRY] | [NAME] | [PURPOSE] | [MECHANISM] | [DATE] | [DATE] |

---

## 10. Compliance Checklist

### 10.1 Before Transferring

```
□ Identify all international transfers
□ Determine appropriate transfer mechanism
□ Complete Transfer Impact Assessment
□ Implement supplementary measures (if needed)
□ Execute appropriate agreements (SCCs, etc.)
□ Update privacy notice
□ Update RoPA
□ Document in transfer register
```

### 10.2 Ongoing

```
□ Monitor for changes in destination country laws
□ Review TIAs periodically (at least annually)
□ Monitor for regulatory guidance
□ Update mechanisms as needed
□ Re-assess if transfer circumstances change
```

---

## 11. Related Documents

- [GDPR Requirements Guide](./gdpr-requirements-guide.md)
- [Records of Processing Activities](./ropa-template.md)
- [Data Processing Agreement Template](../../templates/data-processing-agreement.md)
- [Privacy Notice Template](./privacy-notice-template.md)
- [Data Protection Policy](../../policies/data-protection-policy.md)

---

## 12. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to GDPR](./README.md) | [Back to Frameworks](../README.md)

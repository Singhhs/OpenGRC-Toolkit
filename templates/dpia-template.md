# Data Protection Impact Assessment (DPIA) Template

A template for conducting Data Protection Impact Assessments as required by GDPR Article 35 and other data protection regulations.

---

## Data Protection Impact Assessment

### Document Control

| Field | Information |
|-------|-------------|
| **Project/Processing Name** | [NAME] |
| **DPIA Reference** | DPIA-[YYYY]-[XXX] |
| **Version** | [VERSION] |
| **Date** | [DATE] |
| **Author** | [NAME, ROLE] |
| **DPO Review** | [NAME, DATE] |
| **Business Owner** | [NAME, ROLE] |
| **Status** | [Draft / Under Review / Approved / Requires Action] |

---

## 1. DPIA Screening

### 1.1 Is a DPIA Required?

A DPIA is **mandatory** when processing is likely to result in high risk to individuals. Check if any apply:

**Automatic Triggers (DPIA Required):**
- [ ] Systematic and extensive profiling with significant effects
- [ ] Large-scale processing of special category data
- [ ] Systematic monitoring of publicly accessible areas
- [ ] Use of new technologies with high risk potential
- [ ] Automated decision-making with legal or significant effects
- [ ] Large-scale processing of children's data
- [ ] Processing that prevents individuals from exercising rights
- [ ] Combining datasets from different sources
- [ ] Processing of biometric data for identification

**Risk Factors (Consider DPIA if 2+ apply):**
- [ ] Evaluation or scoring of individuals
- [ ] Automated decision-making
- [ ] Systematic monitoring
- [ ] Sensitive data or data of vulnerable individuals
- [ ] Large-scale processing
- [ ] Matching or combining datasets
- [ ] Data concerning vulnerable data subjects
- [ ] Innovative use of technology
- [ ] Data transfer outside EEA
- [ ] Processing that prevents individuals from accessing services

**Screening Decision:**
- [ ] DPIA Required - Proceed with assessment
- [ ] DPIA Not Required - Document reasoning: _______________
- [ ] DPIA Conducted Voluntarily

---

## 2. Project Description

### 2.1 Processing Overview

**Project/System Name:** [NAME]

**Brief Description:**
[Describe the project, system, or processing activity in 2-3 paragraphs]

**Business Need:**
[Why is this processing necessary? What problem does it solve?]

**Project Timeline:**
| Milestone | Date |
|-----------|------|
| Project Start | [DATE] |
| Go-Live Date | [DATE] |
| Review Date | [DATE] |

### 2.2 Processing Details

**What personal data will be processed?**

| Data Category | Specific Data Elements | Source |
|---------------|------------------------|--------|
| Identity Data | [e.g., name, DOB, ID number] | [Source] |
| Contact Data | [e.g., email, phone, address] | [Source] |
| Financial Data | [e.g., bank details, salary] | [Source] |
| Technical Data | [e.g., IP, device ID, cookies] | [Source] |
| Special Category | [e.g., health, biometric] | [Source] |
| Other | [Specify] | [Source] |

**Who are the data subjects?**
- [ ] Employees
- [ ] Customers
- [ ] Prospects
- [ ] Website visitors
- [ ] Children (under 18)
- [ ] Vulnerable individuals
- [ ] Other: [SPECIFY]

**Estimated number of data subjects:** [NUMBER]

**Estimated volume of records:** [NUMBER]

### 2.3 Processing Operations

**How will data be processed?**

| Operation | Description |
|-----------|-------------|
| Collection | [How data will be collected] |
| Storage | [Where and how data will be stored] |
| Use | [How data will be used] |
| Sharing | [Who data will be shared with] |
| Retention | [How long data will be kept] |
| Deletion | [How data will be deleted] |

**Technologies/Systems involved:**
- [System 1]
- [System 2]
- [System 3]

### 2.4 Data Flows

**Data Flow Diagram:**
[Insert or describe data flow diagram]

```
[Data Subject] --> [Collection Point] --> [Processing System] --> [Storage]
                                                |
                                                v
                                          [Third Party]
```

**Third-Party Recipients:**

| Recipient | Purpose | Location | Safeguards |
|-----------|---------|----------|------------|
| [Name] | [Purpose] | [Country] | [e.g., DPA, SCCs] |
| [Name] | [Purpose] | [Country] | [e.g., DPA, SCCs] |

---

## 3. Lawful Basis Assessment

### 3.1 Legal Basis for Processing

**Primary lawful basis:** [Select one]
- [ ] Consent (Article 6(1)(a))
- [ ] Contract (Article 6(1)(b))
- [ ] Legal obligation (Article 6(1)(c))
- [ ] Vital interests (Article 6(1)(d))
- [ ] Public task (Article 6(1)(e))
- [ ] Legitimate interests (Article 6(1)(f))

**Justification:**
[Explain why this lawful basis applies]

### 3.2 Special Category Data (If Applicable)

**Condition for processing special category data:** [Select one]
- [ ] Explicit consent
- [ ] Employment/social security law
- [ ] Vital interests
- [ ] Not-for-profit bodies
- [ ] Made public by data subject
- [ ] Legal claims
- [ ] Substantial public interest
- [ ] Health or social care
- [ ] Public health
- [ ] Archiving/research/statistics

**Justification:**
[Explain why this condition applies]

### 3.3 Legitimate Interests Assessment (If Applicable)

**What is the legitimate interest?**
[Describe the interest being pursued]

**Is processing necessary for this interest?**
[Explain why processing is necessary]

**Balancing test - Impact on individuals:**
[Weigh the interest against impact on data subjects]

**Conclusion:**
[Does the legitimate interest override individual rights?]

---

## 4. Necessity and Proportionality

### 4.1 Necessity Assessment

| Question | Response |
|----------|----------|
| Is all the data necessary? | [Yes/No - Justify] |
| Could the purpose be achieved with less data? | [Yes/No - Explain] |
| Could the purpose be achieved without personal data? | [Yes/No - Explain] |
| Is the processing proportionate to the aim? | [Yes/No - Justify] |

### 4.2 Data Minimization

**Data minimization measures:**
- [Measure 1]
- [Measure 2]

**Data that could be removed/reduced:**
- [Item 1]
- [Item 2]

### 4.3 Retention

**Retention period:** [PERIOD]

**Justification for retention period:**
[Explain why this period is necessary]

**Deletion/anonymization process:**
[Describe how data will be deleted or anonymized]

---

## 5. Risk Assessment

### 5.1 Risk Identification

Identify risks to individuals' rights and freedoms:

| Risk ID | Risk Description | Likelihood | Severity | Risk Level |
|---------|------------------|------------|----------|------------|
| R1 | [Description] | [L/M/H] | [L/M/H] | [L/M/H] |
| R2 | [Description] | [L/M/H] | [L/M/H] | [L/M/H] |
| R3 | [Description] | [L/M/H] | [L/M/H] | [L/M/H] |
| R4 | [Description] | [L/M/H] | [L/M/H] | [L/M/H] |
| R5 | [Description] | [L/M/H] | [L/M/H] | [L/M/H] |

**Risk Categories to Consider:**
- Unauthorized access or disclosure
- Data loss or destruction
- Inaccurate data causing harm
- Excessive data collection
- Lack of transparency
- Function creep
- Inability to exercise rights
- Discrimination
- Financial loss
- Reputational damage
- Physical harm
- Psychological distress

### 5.2 Risk Matrix

| | Low Severity | Medium Severity | High Severity |
|---|---|---|---|
| **High Likelihood** | Medium | High | Critical |
| **Medium Likelihood** | Low | Medium | High |
| **Low Likelihood** | Low | Low | Medium |

### 5.3 Risk Mitigation

| Risk ID | Mitigation Measure | Owner | Status | Residual Risk |
|---------|-------------------|-------|--------|---------------|
| R1 | [Measure] | [Name] | [Status] | [L/M/H] |
| R2 | [Measure] | [Name] | [Status] | [L/M/H] |
| R3 | [Measure] | [Name] | [Status] | [L/M/H] |
| R4 | [Measure] | [Name] | [Status] | [L/M/H] |
| R5 | [Measure] | [Name] | [Status] | [L/M/H] |

---

## 6. Security Measures

### 6.1 Technical Measures

| Measure | Implemented? | Details |
|---------|--------------|---------|
| Encryption at rest | [Yes/No/Planned] | [Details] |
| Encryption in transit | [Yes/No/Planned] | [Details] |
| Access controls | [Yes/No/Planned] | [Details] |
| Authentication | [Yes/No/Planned] | [Details] |
| Logging and monitoring | [Yes/No/Planned] | [Details] |
| Backup and recovery | [Yes/No/Planned] | [Details] |
| Pseudonymization | [Yes/No/Planned] | [Details] |
| Anonymization | [Yes/No/Planned] | [Details] |

### 6.2 Organizational Measures

| Measure | Implemented? | Details |
|---------|--------------|---------|
| Data protection policies | [Yes/No/Planned] | [Details] |
| Staff training | [Yes/No/Planned] | [Details] |
| Access management process | [Yes/No/Planned] | [Details] |
| Incident response procedure | [Yes/No/Planned] | [Details] |
| Third-party contracts | [Yes/No/Planned] | [Details] |
| Regular audits | [Yes/No/Planned] | [Details] |

---

## 7. Data Subject Rights

### 7.1 Rights Facilitation

| Right | How Facilitated | Contact Point |
|-------|-----------------|---------------|
| Right to be informed | [Description] | [Contact] |
| Right of access | [Description] | [Contact] |
| Right to rectification | [Description] | [Contact] |
| Right to erasure | [Description] | [Contact] |
| Right to restrict processing | [Description] | [Contact] |
| Right to data portability | [Description] | [Contact] |
| Right to object | [Description] | [Contact] |
| Rights related to automated decisions | [Description] | [Contact] |

### 7.2 Privacy Notice

- [ ] Privacy notice updated to include this processing
- [ ] Privacy notice accessible to data subjects
- [ ] Just-in-time notices provided where appropriate

---

## 8. Consultation

### 8.1 Internal Consultation

| Stakeholder | Date | Feedback | Action Taken |
|-------------|------|----------|--------------|
| DPO | [Date] | [Summary] | [Action] |
| IT Security | [Date] | [Summary] | [Action] |
| Legal | [Date] | [Summary] | [Action] |
| [Other] | [Date] | [Summary] | [Action] |

### 8.2 Data Subject Consultation

**Were data subjects consulted?** [Yes/No]

**If yes:**
- Method: [Survey/Focus group/Other]
- Date: [DATE]
- Summary of feedback: [SUMMARY]
- How feedback was incorporated: [DESCRIPTION]

**If no, why not:**
[Explain why consultation was not conducted]

### 8.3 Supervisory Authority Consultation

**Is prior consultation with the supervisory authority required?**
- [ ] No - residual risks are acceptable
- [ ] Yes - high residual risks require consultation

**If yes:**
- Authority: [NAME]
- Date of consultation: [DATE]
- Outcome: [SUMMARY]

---

## 9. DPIA Outcome

### 9.1 Summary of Findings

**Overall Risk Level:** [Low / Medium / High / Critical]

**Key Risks Identified:**
1. [Risk 1]
2. [Risk 2]
3. [Risk 3]

**Key Mitigations Implemented:**
1. [Mitigation 1]
2. [Mitigation 2]
3. [Mitigation 3]

### 9.2 Decision

- [ ] **Approved** - Processing may proceed
- [ ] **Approved with conditions** - Processing may proceed once conditions met
- [ ] **Not approved** - Risks too high, processing cannot proceed
- [ ] **Requires supervisory authority consultation** - Prior consultation needed

**Conditions (if applicable):**
1. [Condition 1]
2. [Condition 2]

### 9.3 Review Schedule

**Next review date:** [DATE]

**Review triggers:**
- Changes to processing scope
- New data categories
- New recipients
- Security incidents
- Regulatory changes
- [Other triggers]

---

## 10. Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Owner | | | |
| Data Protection Officer | | | |
| IT Security | | | |
| Business Sponsor | | | |

---

## Appendices

### Appendix A: Data Flow Diagram
[Detailed data flow diagram]

### Appendix B: Privacy Notice
[Link or copy of relevant privacy notice]

### Appendix C: Third-Party Contracts
[List of relevant DPAs and contracts]

### Appendix D: Security Documentation
[Reference to security assessments]

---

[Back to Templates](./README.md) | [Back to Home](../README.md)

# GDPR Requirements Guide

A comprehensive guide to the General Data Protection Regulation (EU) 2016/679 requirements for organizations.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., DPO, Privacy Manager] |
| **Classification** | Internal |

---

## 1. Introduction to GDPR

### 1.1 What is GDPR?

The General Data Protection Regulation (GDPR) is a comprehensive data protection law that came into effect on **25 May 2018**. It governs how organizations collect, process, store, and share personal data of individuals in the European Union (EU) and European Economic Area (EEA).

### 1.2 Who Must Comply?

GDPR applies to:

| Organization Type | When GDPR Applies |
|-------------------|-------------------|
| **EU-based organizations** | All processing of personal data |
| **Non-EU organizations** | When offering goods/services to EU residents |
| **Non-EU organizations** | When monitoring behavior of EU residents |
| **Processors** | When processing personal data on behalf of controllers |

### 1.3 Key Terminology

| Term | Definition |
|------|------------|
| **Personal Data** | Any information relating to an identified or identifiable natural person |
| **Data Subject** | The individual whose personal data is processed |
| **Controller** | Organization that determines purposes and means of processing |
| **Processor** | Organization that processes data on behalf of the controller |
| **Processing** | Any operation performed on personal data |
| **Special Category Data** | Sensitive data requiring additional protection |
| **Consent** | Freely given, specific, informed, and unambiguous agreement |
| **Pseudonymization** | Processing so data can't be attributed without additional information |

---

## 2. Core Principles (Article 5)

All processing must comply with these seven principles:

### 2.1 Lawfulness, Fairness, and Transparency

| Requirement | Implementation |
|-------------|----------------|
| **Lawfulness** | Have a valid legal basis for each processing activity |
| **Fairness** | Process data in ways individuals would reasonably expect |
| **Transparency** | Be open about how data is used via privacy notices |

### 2.2 Purpose Limitation

| Requirement | Implementation |
|-------------|----------------|
| **Specified** | Clearly define purposes at collection time |
| **Explicit** | Document purposes clearly |
| **Legitimate** | Purposes must be lawful |
| **No further processing** | Don't use for incompatible purposes |

**Compatible purposes include:**
- Archiving in the public interest
- Scientific or historical research
- Statistical purposes

### 2.3 Data Minimization

| Requirement | Implementation |
|-------------|----------------|
| **Adequate** | Sufficient to fulfill the purpose |
| **Relevant** | Rationally linked to the purpose |
| **Limited** | Only collect what's necessary |

**Questions to ask:**
- Do we need this data element?
- Can we achieve the purpose with less data?
- Can we use anonymized data instead?

### 2.4 Accuracy

| Requirement | Implementation |
|-------------|----------------|
| **Accurate** | Ensure data is correct |
| **Up to date** | Update data when necessary |
| **Rectification** | Correct or delete inaccurate data promptly |

### 2.5 Storage Limitation

| Requirement | Implementation |
|-------------|----------------|
| **Time-limited** | Keep only as long as necessary |
| **Retention schedules** | Document how long data is kept and why |
| **Regular review** | Periodically review and delete |

**Exception:** Data may be kept longer for archiving, research, or statistics with appropriate safeguards.

### 2.6 Integrity and Confidentiality (Security)

| Requirement | Implementation |
|-------------|----------------|
| **Appropriate security** | Technical and organizational measures |
| **Protect against** | Unauthorized/unlawful processing |
| **Protect against** | Accidental loss, destruction, damage |

### 2.7 Accountability

| Requirement | Implementation |
|-------------|----------------|
| **Demonstrate compliance** | Maintain documentation |
| **Responsibility** | Controller is responsible for compliance |
| **Evidence** | Be able to prove compliance if challenged |

---

## 3. Lawful Bases for Processing (Article 6)

You must have at least one lawful basis for every processing activity:

### 3.1 The Six Lawful Bases

| Lawful Basis | Article | When to Use |
|--------------|---------|-------------|
| **Consent** | 6(1)(a) | Individual has given clear consent |
| **Contract** | 6(1)(b) | Necessary to fulfill a contract |
| **Legal Obligation** | 6(1)(c) | Required by law |
| **Vital Interests** | 6(1)(d) | Protect someone's life |
| **Public Task** | 6(1)(e) | Official function or public interest |
| **Legitimate Interests** | 6(1)(f) | Your interests (balanced against individual's rights) |

### 3.2 Consent Requirements

For consent to be valid:

```
□ Freely given - genuine choice, no imbalance of power
□ Specific - separate consent for different purposes
□ Informed - know what they're consenting to
□ Unambiguous - clear affirmative action
□ Demonstrable - you can prove consent was given
□ Withdrawable - easy to withdraw as it was to give
```

**Consent is NOT appropriate when:**
- There's a significant power imbalance (e.g., employer-employee)
- The processing is necessary anyway
- You can't offer a genuine choice

### 3.3 Contract Basis

Processing is necessary to:
- Fulfill a contract with the individual
- Take steps at the individual's request before entering a contract

**Note:** Cannot use this for processing that's useful but not necessary for the contract.

### 3.4 Legal Obligation

- Must be a clear legal requirement
- Document the specific law requiring processing
- Cannot use for discretionary processing

### 3.5 Vital Interests

- Life-or-death situations
- Usually used when individual cannot give consent
- Rarely applicable in commercial contexts

### 3.6 Public Task

For public authorities or organizations exercising official authority:
- Must be laid down by law
- Common for government, healthcare, education

### 3.7 Legitimate Interests

Three-part test required:

```
1. PURPOSE TEST
   □ What is the legitimate interest?
   □ Is it your interest, a third party's, or wider public interest?
   □ Is it lawful and clearly articulated?

2. NECESSITY TEST
   □ Is processing necessary for that interest?
   □ Is there a less intrusive way to achieve the same result?
   □ Is the processing proportionate?

3. BALANCING TEST
   □ What is the impact on individuals?
   □ Would they expect this processing?
   □ Are any of them vulnerable (e.g., children)?
   □ Do your interests override their rights?
```

**Document your assessment** - this is your Legitimate Interests Assessment (LIA).

---

## 4. Special Category Data (Article 9)

### 4.1 What is Special Category Data?

| Category | Examples |
|----------|----------|
| **Racial or ethnic origin** | Nationality, ethnicity |
| **Political opinions** | Party membership, political views |
| **Religious/philosophical beliefs** | Religion, atheism, ethical beliefs |
| **Trade union membership** | Union membership status |
| **Genetic data** | DNA, genetic testing results |
| **Biometric data** | Fingerprints, facial recognition (for identification) |
| **Health data** | Medical records, disabilities, mental health |
| **Sex life or sexual orientation** | Sexual preferences, relationships |

### 4.2 Additional Conditions Required

You need BOTH a lawful basis (Article 6) AND an Article 9 condition:

| Condition | When Applicable |
|-----------|-----------------|
| **Explicit consent** | Freely given, specific consent for sensitive data |
| **Employment/social security** | Processing necessary for employment law obligations |
| **Vital interests** | Protect life when consent not possible |
| **Not-for-profit** | Processing by organizations with political/religious aims |
| **Made public** | Individual has made the data public |
| **Legal claims** | Establishing, exercising, or defending legal claims |
| **Substantial public interest** | Specific conditions in national law |
| **Health/social care** | Medical diagnosis, treatment, health system management |
| **Public health** | Cross-border health threats, quality assurance |
| **Archiving/research** | With appropriate safeguards |

### 4.3 Criminal Conviction Data (Article 10)

- Requires additional authorization under national law
- Usually only processed by official authorities
- Similar restrictions to special category data

---

## 5. Data Subject Rights (Articles 12-22)

### 5.1 Overview of Rights

| Right | Article | Response Time |
|-------|---------|---------------|
| Right to be informed | 13-14 | At collection |
| Right of access | 15 | 1 month |
| Right to rectification | 16 | 1 month |
| Right to erasure | 17 | 1 month |
| Right to restrict processing | 18 | 1 month |
| Right to data portability | 20 | 1 month |
| Right to object | 21 | Immediately |
| Rights related to automated decisions | 22 | Varies |

### 5.2 Right to Be Informed

**At collection (direct):**
- Identity and contact details of controller
- Contact details of DPO (if applicable)
- Purposes and lawful basis
- Legitimate interests (if applicable)
- Recipients or categories of recipients
- International transfers and safeguards
- Retention period
- Data subject rights
- Right to withdraw consent (if applicable)
- Right to complain to supervisory authority
- Whether provision is mandatory and consequences of not providing
- Existence of automated decision-making

**If not obtained from individual:**
- Source of data
- Categories of data
- Must inform within 1 month (or at first communication/disclosure)

### 5.3 Right of Access (Subject Access Request)

Individuals can obtain:
- Confirmation of processing
- Copy of their personal data
- Supplementary information (similar to privacy notice)

**Exemptions may apply:**
- Legal professional privilege
- Crime prevention/detection
- Third-party information

### 5.4 Right to Rectification

- Correct inaccurate data
- Complete incomplete data
- Must notify recipients where possible

### 5.5 Right to Erasure ("Right to be Forgotten")

**Applies when:**
- Data no longer necessary
- Consent withdrawn
- Successful objection
- Unlawful processing
- Legal obligation to erase
- Child's data collected for online services

**Does NOT apply when needed for:**
- Freedom of expression
- Legal obligations
- Public health
- Archiving/research/statistics
- Legal claims

### 5.6 Right to Restrict Processing

**Applies when:**
- Accuracy contested (during verification)
- Processing is unlawful but individual prefers restriction to erasure
- Controller no longer needs data but individual needs it for legal claims
- Objection pending verification

**During restriction:**
- Can only store data
- Further processing only with consent, legal claims, protecting others, or public interest

### 5.7 Right to Data Portability

**Requirements:**
- Data provided by individual
- Processing based on consent or contract
- Processing is automated

**Must provide:**
- Data in structured, commonly used, machine-readable format
- Direct transfer to another controller if technically feasible

### 5.8 Right to Object

**Immediate and absolute for:**
- Direct marketing (must stop immediately)

**Requires balancing for:**
- Processing based on legitimate interests
- Processing based on public task

**Must demonstrate:**
- Compelling legitimate grounds that override individual's interests
- Or processing is for legal claims

### 5.9 Rights Related to Automated Decision-Making

**Applies to:**
- Solely automated decisions
- With legal or similarly significant effects

**Individual can:**
- Request human intervention
- Express their point of view
- Contest the decision

**Exceptions:**
- Necessary for contract
- Authorized by law
- Based on explicit consent

---

## 6. Controller Obligations

### 6.1 Privacy by Design and Default (Article 25)

**By Design:**
```
□ Consider data protection from the start of any project
□ Implement appropriate technical measures
□ Implement appropriate organizational measures
□ Integrate safeguards into processing
```

**By Default:**
```
□ Only process data necessary for each purpose
□ Don't collect more than needed
□ Don't retain longer than needed
□ Don't share more widely than needed
□ Default settings should be privacy-protective
```

### 6.2 Security of Processing (Article 32)

Implement appropriate measures considering:
- State of the art
- Cost of implementation
- Nature, scope, context of processing
- Risk and severity to individuals

**Measures to consider:**
- Pseudonymization and encryption
- Confidentiality, integrity, availability, resilience
- Ability to restore access after incident
- Regular testing and evaluation

### 6.3 Records of Processing (Article 30)

**Mandatory if:**
- 250+ employees, OR
- Processing is not occasional, OR
- Processing includes special category/criminal data, OR
- Processing is likely to result in risk to individuals

**Controller record must include:**
| Field | Required |
|-------|----------|
| Controller name and contact details | Yes |
| DPO contact details | If applicable |
| Purposes of processing | Yes |
| Categories of data subjects | Yes |
| Categories of personal data | Yes |
| Categories of recipients | Yes |
| International transfers | Yes |
| Retention periods | Yes |
| Security measures (description) | Yes |

### 6.4 Data Protection Impact Assessment (Article 35)

**Required when:**
- Systematic and extensive profiling with significant effects
- Large-scale processing of special category data
- Systematic monitoring of public areas
- Any processing likely to result in high risk

**DPIA must include:**
- Systematic description of processing
- Assessment of necessity and proportionality
- Assessment of risks to individuals
- Measures to address risks

### 6.5 Data Protection Officer (Articles 37-39)

**Mandatory when:**
- Public authority or body
- Core activities require systematic monitoring at scale
- Core activities involve special category data at scale

**DPO must:**
- Be involved in all data protection matters
- Report to highest management level
- Be independent
- Have adequate resources
- Maintain expert knowledge

**DPO tasks:**
- Inform and advise on obligations
- Monitor compliance
- Advise on DPIAs
- Cooperate with supervisory authority
- Act as contact point

---

## 7. Data Breach Notification (Articles 33-34)

### 7.1 Notification to Supervisory Authority (Article 33)

**When required:**
- Personal data breach occurs
- Risk to rights and freedoms of individuals

**Timeline:**
- Within 72 hours of becoming aware
- If delayed, must justify delay

**Content of notification:**
```
□ Nature of breach
□ Categories and approximate number of individuals affected
□ Categories and approximate number of records affected
□ DPO or other contact point
□ Likely consequences
□ Measures taken or proposed
```

### 7.2 Notification to Individuals (Article 34)

**When required:**
- High risk to rights and freedoms

**Not required if:**
- Data was encrypted/unintelligible
- Measures taken to prevent risk materializing
- Individual notification would require disproportionate effort (use public communication)

**Content:**
- Clear and plain language
- Nature of breach
- DPO contact
- Likely consequences
- Measures taken

---

## 8. International Transfers (Articles 44-49)

### 8.1 Transfer Rules

Personal data can only be transferred outside EEA if:

| Mechanism | Description |
|-----------|-------------|
| **Adequacy Decision** | Country deemed adequate by EU Commission |
| **Standard Contractual Clauses (SCCs)** | EU-approved contract terms |
| **Binding Corporate Rules (BCRs)** | Approved internal policies for multinationals |
| **Derogations** | Specific situations (consent, contract, legal claims, etc.) |

### 8.2 Adequate Countries

Countries with adequacy decisions (as of 2024):
- Andorra, Argentina, Canada (commercial), Faroe Islands
- Guernsey, Israel, Isle of Man, Japan, Jersey
- New Zealand, Republic of Korea, Switzerland
- United Kingdom, United States (Data Privacy Framework)
- Uruguay

### 8.3 Standard Contractual Clauses

- Must use EU Commission-approved clauses
- New SCCs adopted June 2021
- Must conduct Transfer Impact Assessment (TIA)
- May need supplementary measures

### 8.4 Transfer Impact Assessment

Assess:
- Circumstances of transfer
- Laws of destination country
- Whether SCCs can be complied with
- Supplementary measures needed

---

## 9. Enforcement and Penalties

### 9.1 Supervisory Authority Powers (Article 58)

| Power Type | Examples |
|------------|----------|
| **Investigative** | Investigations, audits, access to premises |
| **Corrective** | Warnings, reprimands, orders to comply, bans, fines |
| **Authorization** | Approve BCRs, clauses, certifications |

### 9.2 Administrative Fines (Article 83)

**Lower tier (up to €10M or 2% global turnover):**
- Controller/processor obligations
- Certification body obligations
- Monitoring body obligations

**Higher tier (up to €20M or 4% global turnover):**
- Processing principles
- Lawful basis/consent
- Data subject rights
- International transfers
- Non-compliance with orders

### 9.3 Factors Affecting Fines

| Factor | Consideration |
|--------|---------------|
| Nature, gravity, duration | How serious and how long? |
| Intentional or negligent | Was it deliberate? |
| Mitigation actions | What did you do to reduce harm? |
| Technical/organizational measures | Were security measures appropriate? |
| Previous infringements | History of non-compliance? |
| Cooperation | Did you work with the authority? |
| Data categories | Was special category data involved? |
| How authority learned | Did you self-report? |
| Previous corrective measures | Have you been sanctioned before? |
| Adherence to codes/certifications | Following approved frameworks? |
| Aggravating/mitigating factors | Financial benefit, other circumstances? |

---

## 10. Implementation Checklist

### 10.1 Governance

```
□ Appoint DPO (if required) or privacy lead
□ Assign data protection responsibilities
□ Establish privacy governance structure
□ Allocate adequate resources
□ Report to senior management/board
```

### 10.2 Documentation

```
□ Create/update privacy notices
□ Maintain records of processing activities (RoPA)
□ Document lawful basis for each processing activity
□ Create data retention schedule
□ Document consent mechanisms and records
□ Develop DPIA process and templates
□ Create data breach procedure
□ Document international transfer mechanisms
```

### 10.3 Policies and Procedures

```
□ Data protection/privacy policy
□ Data subject request procedure
□ Data breach response procedure
□ Data retention procedure
□ Privacy impact assessment procedure
□ International transfer procedure
□ Consent management procedure
```

### 10.4 Contracts

```
□ Review and update processor agreements
□ Implement SCCs for international transfers
□ Update customer/supplier contracts
□ Include data protection in new contracts
```

### 10.5 Technical Measures

```
□ Encryption at rest and in transit
□ Access controls and authentication
□ Pseudonymization where appropriate
□ Security monitoring and logging
□ Backup and recovery
□ Data deletion capabilities
□ Subject access request fulfillment system
```

### 10.6 Training and Awareness

```
□ GDPR awareness training for all staff
□ Role-specific training (HR, marketing, IT)
□ DPO/privacy team specialist training
□ Regular refresher training
□ New starter induction
```

---

## 11. GDPR and ISO 27001 Mapping

| GDPR Requirement | ISO 27001 Control |
|------------------|-------------------|
| Article 5 - Principles | Multiple controls supporting security |
| Article 25 - Privacy by Design | A.8.25-8.31 Secure development |
| Article 30 - Records | A.5.9-5.11 Asset management |
| Article 32 - Security | A.8.1-8.34 Technical controls |
| Article 33-34 - Breach notification | A.5.24-5.28 Incident management |
| Article 35 - DPIA | Risk assessment process |
| Article 37-39 - DPO | Organizational roles |

---

## 12. Related Documents

- [Records of Processing Activities Template](./ropa-template.md)
- [Privacy Notice Template](./privacy-notice-template.md)
- [Lawful Basis Assessment Guide](./lawful-basis-guide.md)
- [International Transfers Guide](./international-transfers-guide.md)
- [GDPR Breach Notification Procedure](./breach-notification-procedure.md)
- [Data Subject Request Procedure](../../procedures/data-subject-request-procedure.md)
- [DPIA Template](../../templates/dpia-template.md)
- [Data Processing Agreement Template](../../templates/data-processing-agreement.md)
- [Data Protection Policy](../../policies/data-protection-policy.md)

---

## 13. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to GDPR](./README.md) | [Back to Frameworks](../README.md)

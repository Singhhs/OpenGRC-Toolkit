# Lawful Basis Assessment Guide

A practical guide for determining and documenting the lawful basis for processing personal data under GDPR Article 6.

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

### 1.1 Purpose

This guide helps organizations:
- Understand the six lawful bases under GDPR Article 6
- Choose the most appropriate lawful basis for processing activities
- Document lawful basis decisions
- Conduct Legitimate Interests Assessments (LIAs)

### 1.2 Key Principle

**Every processing activity requires a valid lawful basis BEFORE processing begins.**

You cannot change your lawful basis retrospectively unless you have a valid alternative basis that would have applied from the start.

---

## 2. Overview of Lawful Bases

### 2.1 The Six Lawful Bases (Article 6)

| Basis | Article | Summary | Common Use Cases |
|-------|---------|---------|------------------|
| **Consent** | 6(1)(a) | Individual has given clear consent | Marketing, newsletters, non-essential cookies |
| **Contract** | 6(1)(b) | Necessary for a contract | Order fulfillment, service delivery |
| **Legal Obligation** | 6(1)(c) | Required by law | Tax records, employment law compliance |
| **Vital Interests** | 6(1)(d) | Protect someone's life | Medical emergencies (rare) |
| **Public Task** | 6(1)(e) | Official function | Government, public authorities |
| **Legitimate Interests** | 6(1)(f) | Your interests (balanced) | Fraud prevention, B2B marketing, security |

### 2.2 Decision Flowchart

```
START: What processing do you need to do?
         │
         ▼
Is it required by law? ─────────────────YES──▶ LEGAL OBLIGATION
         │
         NO
         │
         ▼
Is it for a public authority function? ──YES──▶ PUBLIC TASK
         │
         NO
         │
         ▼
Is it to protect someone's life? ────────YES──▶ VITAL INTERESTS
         │
         NO
         │
         ▼
Is it necessary to fulfill a contract ───YES──▶ CONTRACT
with the individual?
         │
         NO
         │
         ▼
Do you have genuine, freely given ───────YES──▶ CONSENT
consent?
         │
         NO
         │
         ▼
Do you have a legitimate interest ───────YES──▶ LEGITIMATE INTERESTS
that outweighs individual rights?              (Conduct LIA)
         │
         NO
         │
         ▼
     CANNOT PROCESS
```

---

## 3. Consent (Article 6(1)(a))

### 3.1 When to Use Consent

**Appropriate for:**
- Marketing communications
- Non-essential cookies
- Processing not necessary for the service
- Special category data (often)
- Sharing with unrelated third parties

**Not appropriate when:**
- There's a power imbalance (employer-employee)
- Processing is mandatory for the service
- You can't offer genuine choice
- Refusing would have negative consequences

### 3.2 Valid Consent Requirements

| Requirement | What It Means | Implementation |
|-------------|---------------|----------------|
| **Freely given** | Genuine choice, no coercion | Don't bundle consent, no penalties for refusal |
| **Specific** | Clear about what's agreed | Separate consents for different purposes |
| **Informed** | Know what they're agreeing to | Clear explanation before consent |
| **Unambiguous** | Clear affirmative action | Checkboxes (not pre-ticked), signatures |
| **Demonstrable** | You can prove it | Records of when, how, what consented to |
| **Withdrawable** | Easy to withdraw | As easy to withdraw as to give |

### 3.3 Consent Checklist

```
□ Is consent genuinely optional?
□ Is there an alternative for those who don't consent?
□ Is there no significant imbalance of power?
□ Is consent separate from terms and conditions?
□ Is the request in clear, plain language?
□ Does it specify all purposes?
□ Does it identify all third parties?
□ Can consent be withdrawn easily?
□ Are you recording evidence of consent?
```

### 3.4 Consent Record Template

| Field | Information |
|-------|-------------|
| **Individual** | [Name/ID] |
| **What consented to** | [Specific processing] |
| **Date/time** | [When consent given] |
| **Method** | [How consent was collected] |
| **Evidence** | [Link to record/screenshot] |
| **Information provided** | [What they were told] |
| **Consent version** | [Version of consent text] |

---

## 4. Contract (Article 6(1)(b))

### 4.1 When to Use Contract

**Two scenarios:**
1. Processing necessary to **perform a contract** with the individual
2. Processing necessary to **take steps** at individual's request **before entering** a contract

### 4.2 Contract Basis Checklist

```
□ Does a contract exist (or are pre-contract steps being taken)?
□ Is the processing genuinely necessary for the contract?
□ Could the contract be performed without this processing?
□ Is the data subject a party to the contract?
□ Is this processing expected by the individual?
```

### 4.3 What Contract Does NOT Cover

- Processing that's merely useful (not necessary)
- Processing for other purposes (marketing, profiling)
- Processing for your benefit rather than contract performance
- Contracts where the individual isn't a party

### 4.4 Contract Basis Documentation

| Processing Activity | Contract | Why Necessary |
|--------------------|----------|---------------|
| [ACTIVITY] | [Contract reference] | [Explanation] |

---

## 5. Legal Obligation (Article 6(1)(c))

### 5.1 When to Use Legal Obligation

Processing is **required by law** (not merely permitted):
- Tax reporting requirements
- Employment law obligations
- Anti-money laundering checks
- Health and safety records
- Court orders

### 5.2 Legal Obligation Checklist

```
□ Is there a specific law requiring this processing?
□ Is it mandatory (not just permitted)?
□ Have you documented the specific legal requirement?
□ Is the processing limited to what the law requires?
```

### 5.3 Legal Obligation Documentation

| Processing Activity | Legal Requirement | Legislation |
|--------------------|-------------------|-------------|
| Tax records retention | Keep records 6 years | [Tax Act reference] |
| Right to work checks | Verify employment eligibility | [Immigration Act reference] |
| [ACTIVITY] | [REQUIREMENT] | [LEGISLATION] |

---

## 6. Vital Interests (Article 6(1)(d))

### 6.1 When to Use Vital Interests

**Very limited application:**
- Life or death situations
- Medical emergencies
- When individual cannot give consent
- Serious health threats

### 6.2 Important Limitations

- Cannot use if another lawful basis applies
- "Vital" means essential for life, not just important
- Rarely applicable in commercial contexts
- Often superseded by legal obligation (emergency services)

---

## 7. Public Task (Article 6(1)(e))

### 7.1 When to Use Public Task

For **public authorities** or organizations with **official functions**:
- Government departments
- Law enforcement
- Healthcare (public sector)
- Education (public sector)
- Regulators

### 7.2 Public Task Requirements

```
□ Is there a legal basis for the public task?
□ Is the processing necessary for that task?
□ Is the individual's right to object accommodated?
```

---

## 8. Legitimate Interests (Article 6(1)(f))

### 8.1 When to Use Legitimate Interests

The most flexible basis, BUT requires a **balancing test**.

**Common legitimate interests:**
- Fraud prevention and security
- Network and information security
- B2B marketing
- Internal administration
- Preventing crime
- Enforcing legal claims

### 8.2 Three-Part Test

Every legitimate interests assessment must cover:

```
1. PURPOSE TEST
   - What is your legitimate interest?
   - Is it valid and clearly articulated?
   - Is it your interest, a third party's, or society's?

2. NECESSITY TEST
   - Is the processing necessary for that interest?
   - Is there a less intrusive way to achieve it?
   - Is it proportionate?

3. BALANCING TEST
   - What impact does the processing have on individuals?
   - Would they expect this processing?
   - Are there particular risks (children, sensitive data)?
   - Do your interests override their rights and freedoms?
```

### 8.3 Legitimate Interests Assessment (LIA) Template

---

#### Legitimate Interests Assessment

**Processing Activity:** [NAME]
**Date:** [DATE]
**Assessor:** [NAME/ROLE]
**Approved by:** [NAME/ROLE]

---

##### Part 1: Purpose Test

**1.1 What is the legitimate interest?**

[Describe the interest you are pursuing]

**1.2 Whose interest is it?**
- [ ] Our organization's interest
- [ ] Third party's interest (specify: ___________)
- [ ] Wider public/societal interest

**1.3 Why is this interest legitimate?**

[Explain why it is a valid interest worth pursuing]

**1.4 What are the benefits of the processing?**

| Beneficiary | Benefit |
|-------------|---------|
| Organization | [BENEFIT] |
| Individuals | [BENEFIT] |
| Third parties | [BENEFIT] |
| Society | [BENEFIT] |

---

##### Part 2: Necessity Test

**2.1 What processing is involved?**

| Data Element | Source | Recipients | Retention |
|--------------|--------|------------|-----------|
| [DATA] | [SOURCE] | [RECIPIENTS] | [PERIOD] |

**2.2 Is this processing necessary for the legitimate interest?**

[Explain why the processing is necessary - not just useful]

**2.3 Could you achieve the same purpose with less data or less intrusive processing?**

| Alternative Considered | Why Not Suitable |
|------------------------|------------------|
| [ALTERNATIVE] | [REASON] |
| [ALTERNATIVE] | [REASON] |

**2.4 Is the processing proportionate?**

[Explain why the extent of processing is proportionate to the benefit]

---

##### Part 3: Balancing Test

**3.1 What is the nature of the data?**

| Factor | Assessment |
|--------|------------|
| Is it special category data? | [Yes/No] |
| Is it about criminal convictions? | [Yes/No] |
| Is it sensitive in context? | [Yes/No - explain] |
| Is it private or publicly available? | [Assessment] |

**3.2 What is the impact on individuals?**

| Impact Area | Assessment | Severity |
|-------------|------------|----------|
| Physical safety | [Impact] | [Low/Medium/High] |
| Financial | [Impact] | [Low/Medium/High] |
| Emotional | [Impact] | [Low/Medium/High] |
| Reputational | [Impact] | [Low/Medium/High] |
| Privacy | [Impact] | [Low/Medium/High] |
| Autonomy/rights | [Impact] | [Low/Medium/High] |

**3.3 Reasonable expectations**

| Question | Answer |
|----------|--------|
| Would individuals expect this processing? | [Yes/No - explain] |
| What is the relationship with individuals? | [Describe] |
| How was the data collected? | [Describe] |
| Was there a privacy notice at collection? | [Yes/No] |

**3.4 Vulnerable individuals**

| Question | Answer |
|----------|--------|
| Does processing affect children? | [Yes/No] |
| Does it affect vulnerable adults? | [Yes/No] |
| Are there power imbalances? | [Yes/No] |

**3.5 Safeguards and mitigations**

| Safeguard | How It Helps |
|-----------|--------------|
| [SAFEGUARD] | [BENEFIT] |
| [SAFEGUARD] | [BENEFIT] |
| [SAFEGUARD] | [BENEFIT] |

**3.6 Can individuals object or opt out?**

[Explain how individuals can exercise their right to object]

---

##### Part 4: Conclusion

**4.1 Balancing Conclusion**

| Factor | Weight |
|--------|--------|
| Strength of legitimate interest | [Strong/Medium/Weak] |
| Impact on individuals | [High/Medium/Low] |
| Reasonable expectations | [Expected/Unexpected] |
| Safeguards in place | [Strong/Medium/Weak] |

**4.2 Decision**

- [ ] **Legitimate interests applies** - Processing may proceed
- [ ] **Legitimate interests applies with conditions** - Implement additional safeguards
- [ ] **Legitimate interests does NOT apply** - Find alternative basis or do not process

**4.3 Reasoning**

[Summarize why the balancing test is passed or failed]

**4.4 Required actions before processing**

| Action | Owner | Deadline |
|--------|-------|----------|
| [ACTION] | [NAME] | [DATE] |

---

##### Sign-off

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Assessor | | | |
| DPO/Privacy | | | |
| Business Owner | | | |

---

## 9. Special Category Data Conditions (Article 9)

When processing special category data, you need BOTH:
1. A lawful basis (Article 6), AND
2. An Article 9 condition

### 9.1 Article 9 Conditions

| Condition | When Applicable |
|-----------|-----------------|
| **Explicit consent** | Clear, affirmative agreement specifically for sensitive data |
| **Employment/social security** | Necessary for employment obligations |
| **Vital interests** | Protect life when consent not possible |
| **Not-for-profit activities** | Political, philosophical, religious organizations |
| **Made public** | Individual has made the data public |
| **Legal claims** | Establish, exercise, or defend claims |
| **Substantial public interest** | Specific schedule under national law |
| **Health/social care** | Medical diagnosis, treatment, health system management |
| **Public health** | Cross-border threats, quality assurance |
| **Archiving/research** | With appropriate safeguards |

---

## 10. Documentation Requirements

### 10.1 What to Document

For each processing activity, document:

| Element | Documentation |
|---------|---------------|
| Lawful basis | Which basis applies |
| Justification | Why that basis was chosen |
| Evidence | Supporting documentation |
| Review date | When to reassess |

### 10.2 Lawful Basis Register

| Processing Activity | Lawful Basis | Justification | LIA Ref (if LI) | Review Date |
|--------------------|--------------|---------------|-----------------|-------------|
| [ACTIVITY] | [BASIS] | [JUSTIFICATION] | [REF] | [DATE] |
| [ACTIVITY] | [BASIS] | [JUSTIFICATION] | [REF] | [DATE] |

---

## 11. Related Documents

- [GDPR Requirements Guide](./gdpr-requirements-guide.md)
- [Records of Processing Activities Template](./ropa-template.md)
- [Privacy Notice Template](./privacy-notice-template.md)
- [DPIA Template](../../templates/dpia-template.md)
- [Data Protection Policy](../../policies/data-protection-policy.md)

---

## 12. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to GDPR](./README.md) | [Back to Frameworks](../README.md)

# GDPR Breach Notification Procedure

A procedure for notifying personal data breaches under GDPR Articles 33-34.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Owner** | [ROLE - e.g., DPO, Privacy Manager] |
| **Approver** | [ROLE - e.g., CISO, Legal Director] |
| **Review Frequency** | Annual |
| **Classification** | Internal |

---

## 1. Purpose

This procedure defines the process for identifying, assessing, documenting, and notifying personal data breaches in compliance with GDPR Articles 33-34 at [ORGANIZATION NAME].

---

## 2. Scope

This procedure applies to:
- All personal data breaches involving data of EU/EEA residents
- All employees, contractors, and third parties
- All systems and processes handling personal data
- Both controller and processor activities

---

## 3. Key Definitions

| Term | Definition |
|------|------------|
| **Personal Data Breach** | A breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorized disclosure of, or access to, personal data |
| **Controller** | Organization that determines purposes and means of processing |
| **Processor** | Organization that processes data on behalf of the controller |
| **Supervisory Authority** | The data protection regulator (e.g., ICO, CNIL, BfDI) |
| **High Risk** | Breach likely to result in significant harm to individuals |

---

## 4. Types of Breaches

### 4.1 Breach Categories

| Category | Description | Examples |
|----------|-------------|----------|
| **Confidentiality** | Unauthorized disclosure or access | Data sent to wrong recipient, hacking, unauthorized viewing |
| **Integrity** | Unauthorized alteration | Data corruption, unauthorized modification |
| **Availability** | Loss of access or destruction | Ransomware, accidental deletion, loss of encryption key |

### 4.2 Common Breach Scenarios

| Scenario | Type |
|----------|------|
| Email sent to wrong recipient | Confidentiality |
| Lost or stolen device | Confidentiality |
| Ransomware attack | Availability + Confidentiality |
| Database breach/hacking | Confidentiality |
| Accidental deletion | Availability |
| Verbal disclosure | Confidentiality |
| Paper documents lost | Confidentiality |
| System misconfiguration exposing data | Confidentiality |
| Phishing attack with data access | Confidentiality |
| Insider unauthorized access | Confidentiality |

---

## 5. Notification Requirements

### 5.1 Notification to Supervisory Authority (Article 33)

| Requirement | Detail |
|-------------|--------|
| **When** | Unless unlikely to result in risk to individuals |
| **Deadline** | Within 72 hours of becoming aware |
| **Who notifies** | Controller (processor must notify controller without undue delay) |

### 5.2 Notification to Individuals (Article 34)

| Requirement | Detail |
|-------------|--------|
| **When** | When breach likely to result in HIGH RISK to rights and freedoms |
| **Deadline** | Without undue delay |
| **Who notifies** | Controller |

### 5.3 Notification NOT Required to Individuals If:

- Data was encrypted/unintelligible to unauthorized persons
- Subsequent measures ensure high risk won't materialize
- Individual notification would require disproportionate effort (use public communication instead)

---

## 6. Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| **All Staff** | Report potential breaches immediately |
| **DPO/Privacy Manager** | Assess breaches, coordinate notification, maintain register |
| **IT/Security Team** | Technical investigation and containment |
| **Incident Commander** | Coordinate response for significant breaches |
| **Legal** | Legal advice, regulatory liaison |
| **Communications** | External communications if needed |
| **Executive Management** | Approve notifications, strategic decisions |

---

## 7. Procedure

### Phase 1: Detection and Reporting

**Step 1: Identify Potential Breach**

Any employee who suspects a breach must:

```
□ Stop the breach if possible (without destroying evidence)
□ Note key details:
  - What happened
  - When discovered
  - What data may be affected
  - Who may be affected
□ Report IMMEDIATELY to:
  - [DPO/Privacy contact]
  - [Security/IT contact]
  - [Breach hotline/email]
```

**Breach Reporting Channels:**
- Email: [breach@organization.com]
- Phone: [PHONE NUMBER]
- Internal portal: [URL]
- In person: [Location/contact]

**Step 2: Log the Incident**

Create breach record immediately:

| Field | Information |
|-------|-------------|
| Breach ID | BR-[YYYY]-[XXX] |
| Date/time discovered | [DATETIME] |
| How discovered | [METHOD] |
| Reported by | [NAME] |
| Initial description | [DESCRIPTION] |

---

### Phase 2: Assessment

**Step 3: Conduct Initial Assessment**

*Complete within 24 hours of discovery*

```
□ What happened?
  - Type of breach (confidentiality/integrity/availability)
  - How did it occur?
  - Is it ongoing?

□ What data is affected?
  - Categories of data
  - Volume of records
  - Special category data?
  - Financial data?

□ Who is affected?
  - Categories of data subjects
  - Approximate numbers
  - Geographic locations
  - Vulnerable individuals?

□ What is the potential impact?
  - Immediate harm
  - Potential future harm
  - Severity of harm
```

**Step 4: Determine Risk Level**

Use this matrix to assess risk:

| Factor | Questions |
|--------|-----------|
| **Data type** | Is it special category? Financial? Identity? |
| **Volume** | How many individuals affected? |
| **Identifiability** | Can individuals be identified? |
| **Context** | What additional harm could occur? |
| **Exposure** | Who has accessed the data? |
| **Controls** | Was data encrypted? Password protected? |
| **Ease of harm** | Can the data be easily misused? |
| **Individuals** | Are vulnerable people affected? |

**Risk Assessment Matrix:**

| Severity of Harm | Likelihood of Harm | Risk Level |
|------------------|-------------------|------------|
| High | High/Likely | **High Risk** |
| High | Medium | **High Risk** |
| High | Low/Unlikely | **Medium Risk** |
| Medium | High | **High Risk** |
| Medium | Medium | **Medium Risk** |
| Medium | Low | **Low Risk** |
| Low | Any | **Low Risk** |

**Step 5: Determine Notification Requirements**

| Risk Level | Authority Notification | Individual Notification |
|------------|----------------------|------------------------|
| **High Risk** | Required (within 72 hours) | Required (without undue delay) |
| **Medium Risk** | Required (within 72 hours) | Consider case-by-case |
| **Low Risk** | Required (within 72 hours) unless unlikely to result in risk | Not required |
| **No Risk** | Not required | Not required |

**All breaches must be documented, even if not notified.**

---

### Phase 3: Containment

**Step 6: Contain the Breach**

```
□ Immediate containment actions:
  - Isolate affected systems
  - Revoke compromised credentials
  - Block unauthorized access
  - Recover lost data if possible

□ Evidence preservation:
  - Preserve logs
  - Document system state
  - Secure forensic copies if needed

□ Short-term fixes:
  - Temporary access restrictions
  - Monitoring for further compromise
  - Communication to affected teams
```

---

### Phase 4: Notification

**Step 7: Notify Supervisory Authority (if required)**

*Within 72 hours of becoming aware*

**Content of notification (Article 33(3)):**

| Element | Information Required |
|---------|---------------------|
| Nature of breach | Description, categories of data, categories of subjects, approximate numbers |
| Contact point | DPO or other contact name and details |
| Likely consequences | Potential impact on individuals |
| Measures taken | Actions to address breach and mitigate effects |

**Authority Contact Details:**

| Authority | Country | Contact |
|-----------|---------|---------|
| [LEAD AUTHORITY] | [COUNTRY] | [CONTACT/URL] |
| ICO | UK | ico.org.uk |
| CNIL | France | cnil.fr |
| BfDI | Germany | bfdi.bund.de |
| [ADD RELEVANT AUTHORITIES] | | |

**If notification cannot be made within 72 hours:**
- Provide information in phases
- Explain reasons for delay
- Each phase should be made without further undue delay

**Step 8: Notify Affected Individuals (if required)**

*If high risk to rights and freedoms*

**Content of notification to individuals (Article 34(2)):**

```
□ Clear, plain language
□ Nature of the breach
□ Name and contact details of DPO/contact
□ Likely consequences
□ Measures taken to address breach
□ Measures taken to mitigate possible adverse effects
□ Recommendations for individuals to protect themselves
```

**Communication channels:**
- Direct email (preferred)
- Direct letter
- Phone call (for high-sensitivity situations)
- Public communication (only if individual contact disproportionate)

---

### Phase 5: Investigation and Remediation

**Step 9: Investigate Root Cause**

```
□ Full investigation:
  - Timeline of events
  - How breach occurred
  - Systems and processes involved
  - People involved
  - Control failures

□ Root cause analysis:
  - Technical failures
  - Process failures
  - Human errors
  - External factors

□ Document findings:
  - Investigation report
  - Contributing factors
  - Recommendations
```

**Step 10: Implement Remediation**

```
□ Address root cause:
  - Technical fixes
  - Process improvements
  - Training needs
  - Policy updates

□ Prevent recurrence:
  - Additional controls
  - Monitoring improvements
  - Testing and verification
```

---

### Phase 6: Documentation and Review

**Step 11: Complete Breach Documentation**

Maintain records of ALL breaches (Article 33(5)), including:

| Element | Documentation |
|---------|---------------|
| Facts | What happened, when, how |
| Effects | Impact on individuals and organization |
| Actions taken | Containment, notification, remediation |
| Decisions | Risk assessment, notification decisions |
| Evidence | Supporting documentation |

**Step 12: Post-Incident Review**

```
□ Conduct review meeting
□ Identify lessons learned
□ Update procedures if needed
□ Improve detection capabilities
□ Test improvements
□ Report to management/board
```

---

## 8. Processor Obligations

### 8.1 If We Are a Processor

When acting as a processor, we must:
- Notify the controller **without undue delay** upon becoming aware
- Provide sufficient information to enable controller notification
- Assist controller with breach management
- Document our processing of the breach

### 8.2 Our Processors

Our processors must notify us:
- Without undue delay
- With all information needed for our assessment
- Per our Data Processing Agreement

---

## 9. Templates

### 9.1 Supervisory Authority Notification Template

```
PERSONAL DATA BREACH NOTIFICATION

Date: [DATE]
Our Reference: BR-[YYYY]-[XXX]

To: [SUPERVISORY AUTHORITY]

1. CONTROLLER DETAILS
Organization: [NAME]
Address: [ADDRESS]
Contact: [DPO NAME], [EMAIL], [PHONE]

2. NATURE OF BREACH
Date/time breach occurred: [DATE/TIME]
Date/time breach discovered: [DATE/TIME]
Description: [DESCRIPTION]

Categories of data: [CATEGORIES]
Approximate number of records: [NUMBER]
Categories of data subjects: [CATEGORIES]
Approximate number affected: [NUMBER]

3. LIKELY CONSEQUENCES
[DESCRIPTION OF POTENTIAL IMPACT]

4. MEASURES TAKEN
Containment: [ACTIONS]
Mitigation: [ACTIONS]
Notification to individuals: [YES/NO - DETAILS]

5. ADDITIONAL INFORMATION
[ANY OTHER RELEVANT DETAILS]

6. CONTACT
For queries: [NAME], [ROLE]
Email: [EMAIL]
Phone: [PHONE]

Signature: _______________________
Name: [NAME]
Role: [ROLE]
Date: [DATE]
```

### 9.2 Individual Notification Template

```
Subject: Important Notice About Your Personal Data

Dear [NAME],

We are writing to inform you of a personal data incident that may affect you.

WHAT HAPPENED
[Clear description of the breach in plain language]

WHAT DATA WAS INVOLVED
[Categories of data affected]

WHAT WE ARE DOING
[Actions taken to address the breach]
[Measures to prevent future incidents]

WHAT YOU CAN DO
We recommend you:
- [Recommendation 1 - e.g., change passwords]
- [Recommendation 2 - e.g., monitor accounts]
- [Recommendation 3 - e.g., be alert to phishing]

CONTACT US
If you have questions:
- Email: [EMAIL]
- Phone: [PHONE]
- Our Data Protection Officer: [DPO CONTACT]

We sincerely apologize for this incident and any concern it may cause.

Yours sincerely,

[NAME]
[TITLE]
[ORGANIZATION]
```

---

## 10. Breach Register

Maintain a register of all breaches:

| BR ID | Date Discovered | Description | Data/Subjects | Risk Level | SA Notified | Individuals Notified | Status |
|-------|-----------------|-------------|---------------|------------|-------------|---------------------|--------|
| [ID] | [DATE] | [DESC] | [DETAILS] | [LEVEL] | [Y/N/DATE] | [Y/N/DATE] | [STATUS] |

---

## 11. Key Timelines

| Action | Deadline |
|--------|----------|
| Report suspected breach internally | Immediately |
| Initial assessment | 24 hours |
| Notify supervisory authority | 72 hours from awareness |
| Notify individuals (if high risk) | Without undue delay |
| Complete investigation | [X] weeks |
| Post-incident review | [X] weeks |

---

## 12. Escalation

| Situation | Escalate To | Contact |
|-----------|-------------|---------|
| Any suspected breach | DPO/Privacy Team | [CONTACT] |
| High-risk breach | Executive Management | [CONTACT] |
| Potential regulatory action | Legal | [CONTACT] |
| Media attention | Communications | [CONTACT] |
| Criminal activity | Legal + Law Enforcement | [CONTACT] |

---

## 13. Related Documents

- [Incident Response Procedure](../../procedures/incident-response-procedure.md)
- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Data Breach Playbook](../../crisis-management/playbooks/data-breach-playbook.md)
- [GDPR Requirements Guide](./gdpr-requirements-guide.md)
- [Data Protection Policy](../../policies/data-protection-policy.md)

---

## 14. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to GDPR](./README.md) | [Back to Frameworks](../README.md)

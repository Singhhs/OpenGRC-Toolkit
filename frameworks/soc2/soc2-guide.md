# SOC 2 Compliance Guide

A comprehensive guide to understanding and achieving SOC 2 compliance.

---

## Document Control

| Field | Information |
|-------|-------------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., CISO, Compliance Manager] |
| **Classification** | Internal |

---

## 1. Introduction

### 1.1 What is SOC 2?

SOC 2 (Service Organization Control 2) is an auditing framework developed by the American Institute of Certified Public Accountants (AICPA). It defines criteria for managing customer data based on five Trust Service Criteria (TSC).

SOC 2 reports provide assurance to customers and stakeholders that a service organization has appropriate controls in place.

### 1.2 Who Needs SOC 2?

SOC 2 is relevant for:
- SaaS providers
- Cloud service providers
- Data centers and hosting providers
- Managed service providers (MSPs)
- Any organization that stores, processes, or transmits customer data

### 1.3 Benefits of SOC 2

| Benefit | Description |
|---------|-------------|
| **Customer Trust** | Demonstrates commitment to security |
| **Competitive Advantage** | Often required to win enterprise deals |
| **Risk Reduction** | Identifies and addresses control gaps |
| **Operational Improvement** | Formalizes security processes |
| **Regulatory Support** | Helps meet compliance requirements |

---

## 2. SOC 2 Report Types

### 2.1 Type I vs Type II

| Aspect | Type I | Type II |
|--------|--------|---------|
| **Scope** | Design of controls | Design AND operating effectiveness |
| **Timeframe** | Point in time (specific date) | Period of time (typically 6-12 months) |
| **Evidence** | Control descriptions | Control descriptions + testing results |
| **Value** | Lower - design only | Higher - proves controls work |
| **Timeline** | Faster to achieve | Requires observation period |
| **Cost** | Lower | Higher |

### 2.2 When to Choose Each Type

| Scenario | Recommended Type |
|----------|------------------|
| First SOC 2 audit | Type I (then Type II) |
| New controls recently implemented | Type I |
| Established controls, need full assurance | Type II |
| Customer requirement specifies Type II | Type II |
| Quick market requirement | Type I |

### 2.3 Report Components

A SOC 2 report includes:

| Section | Content |
|---------|---------|
| **Section I** | Auditor's opinion |
| **Section II** | Management assertion |
| **Section III** | System description |
| **Section IV** | Trust service criteria, controls, and tests (Type II) |
| **Section V** | Other information (optional) |

---

## 3. Trust Service Criteria Overview

### 3.1 The Five Categories

| Category | Required? | Description |
|----------|-----------|-------------|
| **Security** | Always | Protection against unauthorized access (Common Criteria) |
| **Availability** | Optional | System availability for operation and use |
| **Processing Integrity** | Optional | System processing is complete, valid, accurate, timely |
| **Confidentiality** | Optional | Information designated confidential is protected |
| **Privacy** | Optional | Personal information is handled appropriately |

### 3.2 Selecting Categories

**Security (Common Criteria) is always required.**

Select additional categories based on:

| Factor | Consideration |
|--------|---------------|
| **Service type** | What does your service do? |
| **Customer data** | What data do you handle? |
| **Customer requirements** | What do customers ask for? |
| **Contractual obligations** | What have you committed to? |
| **Risk profile** | What are your key risks? |

**Common combinations:**
- SaaS: Security + Availability + Confidentiality
- Data processors: Security + Confidentiality + Privacy
- Infrastructure: Security + Availability
- Healthcare: Security + Availability + Confidentiality + Privacy

---

## 4. Common Criteria (Security)

The Common Criteria (CC) apply to all SOC 2 engagements and form the foundation of security controls.

### 4.1 CC1 - Control Environment

*The foundation for all other controls*

| Criteria | Description |
|----------|-------------|
| CC1.1 | COSO Principle 1: Demonstrates commitment to integrity and ethical values |
| CC1.2 | COSO Principle 2: Board exercises oversight responsibility |
| CC1.3 | COSO Principle 3: Management establishes structures, reporting lines, authorities |
| CC1.4 | COSO Principle 4: Demonstrates commitment to competence |
| CC1.5 | COSO Principle 5: Enforces accountability |

**Key Controls:**
- Code of conduct/ethics policy
- Background checks
- Organizational structure
- Job descriptions and responsibilities
- Board/management oversight
- Performance evaluations

### 4.2 CC2 - Communication and Information

*How information flows within the organization*

| Criteria | Description |
|----------|-------------|
| CC2.1 | COSO Principle 13: Uses relevant quality information |
| CC2.2 | COSO Principle 14: Communicates internally |
| CC2.3 | COSO Principle 15: Communicates externally |

**Key Controls:**
- Security policies communicated to employees
- Security awareness training
- Incident reporting mechanisms
- External communication of security commitments
- Customer notifications

### 4.3 CC3 - Risk Assessment

*Identifying and assessing risks*

| Criteria | Description |
|----------|-------------|
| CC3.1 | COSO Principle 6: Specifies suitable objectives |
| CC3.2 | COSO Principle 7: Identifies and analyzes risk |
| CC3.3 | COSO Principle 8: Assesses fraud risk |
| CC3.4 | COSO Principle 9: Identifies and analyzes significant change |

**Key Controls:**
- Risk assessment process
- Risk register
- Fraud risk assessment
- Change impact assessment
- Risk treatment plans

### 4.4 CC4 - Monitoring Activities

*Ongoing evaluation of controls*

| Criteria | Description |
|----------|-------------|
| CC4.1 | COSO Principle 16: Selects, develops, performs ongoing/separate evaluations |
| CC4.2 | COSO Principle 17: Evaluates and communicates deficiencies |

**Key Controls:**
- Internal audits
- Control monitoring
- Vulnerability assessments
- Penetration testing
- Management review meetings
- Exception tracking and remediation

### 4.5 CC5 - Control Activities

*Actions to address risks*

| Criteria | Description |
|----------|-------------|
| CC5.1 | COSO Principle 10: Selects and develops control activities |
| CC5.2 | COSO Principle 11: Selects and develops technology controls |
| CC5.3 | COSO Principle 12: Deploys through policies and procedures |

**Key Controls:**
- Security policies and procedures
- Technology controls implementation
- Segregation of duties
- Control documentation

### 4.6 CC6 - Logical and Physical Access Controls

*Restricting access to authorized users*

| Criteria | Description |
|----------|-------------|
| CC6.1 | Logical access security software, infrastructure, architectures |
| CC6.2 | Prior to issuing credentials, registration and authorization |
| CC6.3 | Process to remove access when no longer required |
| CC6.4 | Restricts physical access to facilities and protected information |
| CC6.5 | Protects against security events to meet objectives |
| CC6.6 | Implements boundary protection |
| CC6.7 | Restricts transmission, movement, removal of information |
| CC6.8 | Prevents or detects unauthorized or malicious software |

**Key Controls:**
- Identity and access management
- Authentication (MFA)
- Access provisioning and deprovisioning
- Physical security
- Network security (firewalls, segmentation)
- Endpoint protection
- Data loss prevention
- Encryption

### 4.7 CC7 - System Operations

*Managing system operations*

| Criteria | Description |
|----------|-------------|
| CC7.1 | Uses detection and monitoring procedures |
| CC7.2 | Monitors system components for anomalies |
| CC7.3 | Evaluates security events |
| CC7.4 | Responds to identified security incidents |
| CC7.5 | Identifies, develops, and implements activities to recover |

**Key Controls:**
- Security monitoring (SIEM)
- Intrusion detection
- Log management
- Incident response procedures
- Disaster recovery
- Business continuity

### 4.8 CC8 - Change Management

*Managing changes to systems*

| Criteria | Description |
|----------|-------------|
| CC8.1 | Authorizes, designs, develops, configures, tests, and implements changes |

**Key Controls:**
- Change management policy
- Change approval process
- Testing procedures
- Segregation of environments
- Version control
- Deployment procedures

### 4.9 CC9 - Risk Mitigation

*Managing vendor and business risks*

| Criteria | Description |
|----------|-------------|
| CC9.1 | Identifies, selects, and develops risk mitigation activities |
| CC9.2 | Assesses and manages vendor and partner risks |

**Key Controls:**
- Business continuity planning
- Insurance
- Vendor management program
- Third-party risk assessments
- Vendor contracts

---

## 5. Additional Trust Service Criteria

### 5.1 Availability (A Series)

| Criteria | Description |
|----------|-------------|
| A1.1 | Maintains, monitors, and evaluates current processing capacity and availability |
| A1.2 | Authorizes, designs, develops, implements, operates, maintains, and monitors environmental protections |
| A1.3 | Tests recovery plan procedures supporting system recovery |

**Key Controls:**
- Capacity planning
- Performance monitoring
- Environmental controls (power, cooling)
- Redundancy and failover
- Backup and recovery
- DR testing

### 5.2 Processing Integrity (PI Series)

| Criteria | Description |
|----------|-------------|
| PI1.1 | Obtains or generates, uses, and communicates relevant, quality information |
| PI1.2 | Implements policies and procedures over system inputs |
| PI1.3 | Implements policies and procedures over system processing |
| PI1.4 | Implements policies and procedures to make output complete, accurate, and timely |
| PI1.5 | Implements policies and procedures to store inputs, items in processing, and outputs |

**Key Controls:**
- Input validation
- Processing controls
- Output reconciliation
- Error handling
- Data quality checks
- Audit trails

### 5.3 Confidentiality (C Series)

| Criteria | Description |
|----------|-------------|
| C1.1 | Identifies and maintains confidential information |
| C1.2 | Disposes of confidential information |

**Key Controls:**
- Data classification
- Confidentiality agreements (NDAs)
- Data encryption
- Data retention and disposal
- Access restrictions for confidential data

### 5.4 Privacy (P Series)

| Criteria | Description |
|----------|-------------|
| P1.1 | Notice: Provides notice about privacy practices |
| P2.1 | Choice and consent: Describes choices and obtains consent |
| P3.1 | Collection: Collects personal information consistent with objectives |
| P3.2 | Collection: For new purposes, assesses compatibility |
| P4.1 | Use, retention, and disposal: Limits use of personal information |
| P4.2 | Use, retention, and disposal: Retains only as needed |
| P4.3 | Use, retention, and disposal: Disposes of personal information |
| P5.1 | Access: Grants identified individuals ability to access their data |
| P5.2 | Access: Corrects, amends, or appends personal information |
| P6.1 | Disclosure and notification: Discloses to third parties with consent |
| P6.2 | Disclosure and notification: Creates and retains record of disclosures |
| P6.3 | Disclosure and notification: Creates and retains record of detected unauthorized disclosures |
| P6.4 | Disclosure and notification: Obtains privacy commitments from vendors |
| P6.5 | Disclosure and notification: Notifies of unauthorized access |
| P6.6 | Disclosure and notification: Provides notification of changes |
| P6.7 | Disclosure and notification: Provides information about personal information held |
| P7.1 | Quality: Collects and maintains accurate, complete personal information |
| P8.1 | Monitoring and enforcement: Monitors compliance with privacy commitments |

**Key Controls:**
- Privacy policy
- Consent mechanisms
- Data subject rights procedures
- Data minimization
- Privacy impact assessments
- Breach notification procedures
- Vendor privacy requirements

---

## 6. SOC 2 Audit Process

### 6.1 Audit Timeline

```
┌─────────────────────────────────────────────────────────────┐
│ PREPARATION PHASE (3-6 months before audit)                 │
│ • Gap assessment                                            │
│ • Control implementation                                    │
│ • Evidence collection                                       │
│ • Pre-audit readiness check                                 │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│ ENGAGEMENT PHASE                                            │
│ • Select auditor                                            │
│ • Define scope and criteria                                 │
│ • Sign engagement letter                                    │
│ • Establish timeline                                        │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│ OBSERVATION PERIOD (Type II only - 6-12 months)             │
│ • Controls operating                                        │
│ • Evidence being generated                                  │
│ • Auditor may request interim evidence                      │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│ AUDIT PHASE (2-4 weeks)                                     │
│ • Document requests                                         │
│ • Walkthroughs                                              │
│ • Testing (Type II)                                         │
│ • Interviews                                                │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│ REPORT PHASE (2-4 weeks)                                    │
│ • Draft report review                                       │
│ • Management response to exceptions                         │
│ • Final report issued                                       │
└─────────────────────────────────────────────────────────────┘
```

### 6.2 Typical Timeline

| Phase | Duration |
|-------|----------|
| Gap assessment | 2-4 weeks |
| Remediation | 2-6 months |
| Pre-audit preparation | 2-4 weeks |
| Type I audit | 2-4 weeks |
| Observation period (Type II) | 6-12 months |
| Type II audit | 2-4 weeks |
| Report finalization | 2-4 weeks |

### 6.3 Auditor Selection

| Factor | Consideration |
|--------|---------------|
| **Experience** | Industry expertise, similar clients |
| **Reputation** | Known and respected by your customers |
| **Approach** | Collaborative vs. adversarial |
| **Cost** | Competitive but not cheapest |
| **Timeline** | Can meet your schedule |
| **Communication** | Responsive and clear |

---

## 7. Control Implementation

### 7.1 Control Categories

| Category | Examples |
|----------|----------|
| **Administrative** | Policies, procedures, training |
| **Technical** | Firewalls, encryption, access controls |
| **Physical** | Locks, cameras, badge readers |

### 7.2 Control Attributes

For each control, document:

| Attribute | Description |
|-----------|-------------|
| **Control ID** | Unique identifier |
| **Description** | What the control does |
| **Criteria** | Which TSC it addresses |
| **Owner** | Who is responsible |
| **Frequency** | How often it operates |
| **Evidence** | What proves it works |

### 7.3 Common Control Gaps

| Area | Common Gaps |
|------|-------------|
| **Access Management** | No formal provisioning/deprovisioning, missing access reviews |
| **Change Management** | Informal process, missing approvals, no segregation |
| **Incident Response** | No documented plan, untested procedures |
| **Risk Assessment** | No formal process, outdated assessments |
| **Vendor Management** | No due diligence, missing contracts |
| **Training** | No security awareness, no records |

---

## 8. Evidence Collection

### 8.1 Evidence Types

| Type | Examples |
|------|----------|
| **Policies/Procedures** | Written documentation |
| **Screenshots** | System configurations |
| **Reports** | System-generated reports |
| **Logs** | Audit trails, access logs |
| **Records** | Completed forms, approvals |
| **Observations** | Auditor walkthroughs |
| **Inquiries** | Interview responses |

### 8.2 Evidence Requirements

Evidence should be:
- **Relevant** - Addresses the specific criterion
- **Reliable** - From trusted source
- **Sufficient** - Enough to support conclusion
- **Timely** - Within the audit period (Type II)

### 8.3 Evidence by Control Area

| Control Area | Typical Evidence |
|--------------|------------------|
| **Access Control** | User lists, access reviews, termination tickets |
| **Change Management** | Change tickets, approvals, test results |
| **Monitoring** | SIEM reports, alert samples, review records |
| **Incident Response** | Incident tickets, post-mortems |
| **Backup** | Backup logs, restoration test results |
| **Training** | Completion records, training materials |

---

## 9. Maintaining Compliance

### 9.1 Continuous Compliance

| Activity | Frequency |
|----------|-----------|
| Control monitoring | Continuous |
| Access reviews | Quarterly |
| Risk assessment | Annually |
| Policy review | Annually |
| Training | Annually + new hires |
| Penetration testing | Annually |
| DR testing | Annually |

### 9.2 Annual Audit Cycle

```
Year 1: Type I → Type II (6-month observation)
Year 2: Type II renewal
Year 3: Type II renewal
...continue annually
```

### 9.3 Handling Exceptions

| Situation | Response |
|-----------|----------|
| Control failure identified | Document, remediate, assess impact |
| Gap during audit | Management response in report |
| Significant deficiency | May affect opinion, prioritize fix |
| Customer questions | Provide context and remediation plan |

---

## 10. SOC 2 and Other Frameworks

### 10.1 SOC 2 vs ISO 27001

| Aspect | SOC 2 | ISO 27001 |
|--------|-------|-----------|
| **Type** | Attestation report | Certification |
| **Auditor** | CPA firm | Certification body |
| **Scope** | Flexible (choose criteria) | Comprehensive ISMS |
| **Validity** | Annual renewal | 3-year certificate |
| **Geography** | Primarily North America | International |
| **Output** | Detailed report | Certificate |

### 10.2 Leveraging Multiple Frameworks

| Framework | Alignment with SOC 2 |
|-----------|---------------------|
| **ISO 27001** | Strong overlap with Common Criteria |
| **NIST CSF** | Maps to all trust service criteria |
| **GDPR** | Aligns with Privacy criteria |
| **HIPAA** | Security and Privacy criteria overlap |
| **PCI DSS** | Security controls overlap |

---

## 11. Related Documents

- [Trust Service Criteria Reference](./trust-services-criteria.md)
- [SOC 2 Readiness Checklist](./soc2-readiness-checklist.md)
- [SOC 2 Evidence Guide](./soc2-evidence-guide.md)
- [SOC 2 to ISO 27001 Mapping](./soc2-iso27001-mapping.md)
- [SOC 2 Gap Assessment](./soc2-gap-assessment.md)

---

## 12. External Resources

| Resource | Link |
|----------|------|
| AICPA SOC Suite | [aicpa.org/soc](https://www.aicpa.org/soc) |
| Trust Service Criteria | AICPA TSP Section 100 |
| SOC 2 Guide | AICPA SOC 2 Guide |

---

## 13. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to SOC 2](./README.md) | [Back to Frameworks](../README.md)

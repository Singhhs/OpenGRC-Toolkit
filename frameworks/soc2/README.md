# SOC 2 Resources

**Status: Active (80%)**

SOC 2 (Service Organization Control 2) is an auditing procedure developed by the AICPA that ensures service providers securely manage data to protect the interests of organizations and the privacy of their clients.

---

## Quick Navigation

| Document | Description |
|----------|-------------|
| [SOC 2 Guide](./soc2-guide.md) | Comprehensive SOC 2 overview, Type I vs II, audit process |
| [Trust Service Criteria](./trust-services-criteria.md) | Complete TSC reference with points of focus |
| [Readiness Checklist](./soc2-readiness-checklist.md) | Pre-audit readiness assessment checklist |
| [Evidence Guide](./soc2-evidence-guide.md) | Evidence collection guide for audits |
| [Gap Assessment](./soc2-gap-assessment.md) | Gap assessment template for SOC 2 readiness |
| [ISO 27001 Mapping](./soc2-iso27001-mapping.md) | Mapping between SOC 2 and ISO 27001:2022 |

---

## What is SOC 2?

SOC 2 is an attestation report that provides assurance over controls at a service organization relevant to the Trust Service Criteria. Unlike certifications, SOC 2 results in an auditor's opinion on the design and operating effectiveness of controls.

### Report Types

| Type | Description | Use Case |
|------|-------------|----------|
| **Type I** | Point-in-time assessment of control design | Initial SOC 2, quick turnaround needed |
| **Type II** | Assessment of design and operating effectiveness over a period (3-12 months) | Ongoing assurance, customer requirement |

---

## Trust Service Criteria

SOC 2 audits evaluate controls against one or more Trust Service Criteria:

| Category | Required | Description |
|----------|----------|-------------|
| **Security (Common Criteria)** | Yes | Protection against unauthorized access |
| **Availability** | Optional | System availability for operation and use |
| **Processing Integrity** | Optional | System processing is complete, valid, accurate, timely |
| **Confidentiality** | Optional | Information designated as confidential is protected |
| **Privacy** | Optional | Personal information is collected, used, retained, disclosed appropriately |

### Common Criteria Categories (CC1-CC9)

Security is the foundational criterion, organized into nine categories:

| Category | Focus Area | Key Controls |
|----------|------------|--------------|
| **CC1** | Control Environment | Governance, ethics, organizational structure |
| **CC2** | Communication and Information | Internal/external communication, quality information |
| **CC3** | Risk Assessment | Risk identification, fraud risk, change impact |
| **CC4** | Monitoring Activities | Ongoing/separate evaluations, deficiency communication |
| **CC5** | Control Activities | Control selection, technology controls, policies |
| **CC6** | Logical and Physical Access | Access management, authentication, physical security |
| **CC7** | System Operations | Security monitoring, incident response, recovery |
| **CC8** | Change Management | Change control, testing, approval, deployment |
| **CC9** | Risk Mitigation | Vendor management, third-party risk |

---

## SOC 2 Documents

### Core Guides

| Document | Description |
|----------|-------------|
| [SOC 2 Guide](./soc2-guide.md) | Complete overview of SOC 2 framework, audit types, process, and timeline |
| [Trust Service Criteria](./trust-services-criteria.md) | Detailed reference for all TSC with points of focus for each criterion |

### Assessment & Planning

| Document | Description |
|----------|-------------|
| [Readiness Checklist](./soc2-readiness-checklist.md) | Comprehensive checklist covering all control domains for pre-audit assessment |
| [Gap Assessment](./soc2-gap-assessment.md) | Detailed gap assessment template for evaluating SOC 2 readiness |
| [Evidence Guide](./soc2-evidence-guide.md) | Guide for collecting and organizing evidence by control area |

### Cross-Framework Resources

| Document | Description |
|----------|-------------|
| [ISO 27001 Mapping](./soc2-iso27001-mapping.md) | Detailed mapping between SOC 2 criteria and ISO 27001:2022 controls |

---

## Getting Started with SOC 2

### Step 1: Define Scope
1. Identify system boundaries and services in scope
2. Select Trust Service Criteria (Security + optional criteria)
3. Identify subservice organizations (carve-out vs inclusive)

### Step 2: Assess Readiness
1. Complete the [Readiness Checklist](./soc2-readiness-checklist.md)
2. Perform [Gap Assessment](./soc2-gap-assessment.md)
3. Develop remediation plan for gaps

### Step 3: Implement Controls
1. Address gaps identified in assessment
2. Document policies, procedures, and controls
3. Implement monitoring and evidence collection

### Step 4: Engage Auditor
1. Select CPA firm with SOC 2 experience
2. Determine report type (Type I or Type II)
3. Establish audit period for Type II

### Step 5: Prepare Evidence
1. Use [Evidence Guide](./soc2-evidence-guide.md) to organize evidence
2. Collect samples for audit period
3. Document populations for sampling

---

## SOC 2 vs Other Frameworks

| Aspect | SOC 2 | ISO 27001 | NIST CSF |
|--------|-------|-----------|----------|
| **Type** | Attestation report | Certification | Framework |
| **Auditor** | CPA firm | Accredited CB | Self-assessment or third-party |
| **Validity** | Point-in-time or period | 3-year cycle | Ongoing |
| **Focus** | Service organizations | Any organization | Any organization |
| **Geographic** | Primarily North America | International | Primarily US |
| **Flexibility** | Choose TSC categories | Full ISMS required | Flexible implementation |
| **Output** | Auditor opinion report | Certificate | Profile/assessment |

### When to Choose SOC 2

SOC 2 is typically appropriate when:
- You are a SaaS or service provider
- Customers require attestation reports
- Primary market is North America
- Need to demonstrate security controls to clients
- Want flexibility in scope (choose criteria)

---

## Leveraging Existing Frameworks

### From ISO 27001

Organizations with ISO 27001 certification have significant overlap:
- ~85-90% of Common Criteria covered by ISO controls
- Risk assessment process directly applicable
- Many evidence artifacts can be reused

See [SOC 2 to ISO 27001 Mapping](./soc2-iso27001-mapping.md) for detailed alignment.

### From NIST CSF

Organizations implementing NIST CSF can leverage:
- Risk management approach aligns with CC3
- Detection and response aligns with CC7
- Access control aligns with CC6

---

## Audit Timeline

### Type I (3-4 months)
| Phase | Duration | Activities |
|-------|----------|------------|
| Readiness | 4-8 weeks | Gap assessment, remediation |
| Audit | 2-4 weeks | Evidence collection, testing |
| Report | 2-3 weeks | Draft, review, final report |

### Type II (6-12 months)
| Phase | Duration | Activities |
|-------|----------|------------|
| Readiness | 4-8 weeks | Gap assessment, remediation |
| Observation | 3-12 months | Control operation, evidence collection |
| Audit | 3-4 weeks | Testing, sampling, interviews |
| Report | 2-4 weeks | Draft, review, final report |

---

## Common Challenges

| Challenge | Solution |
|-----------|----------|
| Scope creep | Define clear system boundaries upfront |
| Evidence gaps | Start collecting evidence early; use automated tools |
| Policy inconsistency | Align policies with actual practices |
| Vendor management | Document subservice organizations and monitoring |
| Control gaps | Prioritize remediation based on risk |
| Resource constraints | Phase implementation, start with Type I |

---

## Resources in This Section

### Documents (6)

1. **[SOC 2 Guide](./soc2-guide.md)** - Comprehensive framework overview
2. **[Trust Service Criteria](./trust-services-criteria.md)** - Complete TSC reference
3. **[Readiness Checklist](./soc2-readiness-checklist.md)** - Pre-audit assessment
4. **[Evidence Guide](./soc2-evidence-guide.md)** - Evidence collection guidance
5. **[Gap Assessment](./soc2-gap-assessment.md)** - Detailed gap analysis template
6. **[ISO 27001 Mapping](./soc2-iso27001-mapping.md)** - Cross-framework mapping

---

## Related Framework Resources

| Framework | Relationship | Documentation |
|-----------|--------------|---------------|
| [ISO 27001](../iso-27001/README.md) | Strong overlap with Common Criteria | [View](../iso-27001/README.md) |
| [NIST CSF](../nist-csf/README.md) | Complementary risk framework | [View](../nist-csf/README.md) |
| [GDPR](../gdpr/README.md) | Supports Privacy criteria | [View](../gdpr/README.md) |

---

## Contributing

Help improve SOC 2 resources:
- Add additional policy templates aligned to SOC 2
- Create supplementary guides (system description, Type II tips)
- Share lessons learned from audits (anonymized)

See [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines.

---

[Back to Frameworks](../README.md) | [Back to Home](../../README.md)

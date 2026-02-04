# NIST Cybersecurity Framework (CSF) 2.0

**Status: Active**

Comprehensive resources for implementing the NIST Cybersecurity Framework 2.0.

---

## Quick Start

| Step | Resource |
|------|----------|
| 1. Understand the Framework | [NIST CSF 2.0 Guide](./nist-csf-guide.md) |
| 2. Assess Current State | [CSF Assessment Template](./csf-assessment-template.md) |
| 3. Understand Maturity Levels | [Implementation Tiers Guide](./implementation-tiers-guide.md) |
| 4. Create Profiles | [CSF Profile Template](./csf-profile-template.md) |
| 5. Map to ISO 27001 | [NIST-ISO 27001 Mapping](./nist-iso27001-mapping.md) |
| 6. Implement | [CSF Implementation Guide](./csf-implementation-guide.md) |

---

## Available Resources

### Guides

| Document | Description |
|----------|-------------|
| [NIST CSF 2.0 Guide](./nist-csf-guide.md) | Comprehensive guide to all 6 functions, 22 categories, and 106 subcategories |
| [Implementation Tiers Guide](./implementation-tiers-guide.md) | Understanding and using the 4 implementation tiers |
| [CSF Implementation Guide](./csf-implementation-guide.md) | Step-by-step implementation roadmap |

### Templates

| Document | Description |
|----------|-------------|
| [CSF Assessment Template](./csf-assessment-template.md) | Self-assessment against all CSF subcategories |
| [CSF Profile Template](./csf-profile-template.md) | Current and target profile documentation |

### Mappings

| Document | Description |
|----------|-------------|
| [NIST CSF to ISO 27001 Mapping](./nist-iso27001-mapping.md) | Detailed control mapping between frameworks |

---

## CSF 2.0 Overview

### What's New in CSF 2.0

| Change | Description |
|--------|-------------|
| **GOVERN Function** | New sixth function focusing on governance and risk strategy |
| **Broader Scope** | Expanded beyond critical infrastructure to all organizations |
| **Supply Chain** | Enhanced emphasis on supply chain risk management |
| **Implementation Examples** | New practical implementation guidance |
| **Profiles** | Improved guidance for organizational profiles |

### The Six Functions

| Function | ID | Purpose | Categories |
|----------|-----|---------|------------|
| **GOVERN** | GV | Establish risk management strategy and oversight | 6 |
| **IDENTIFY** | ID | Understand assets, risks, and improvements | 3 |
| **PROTECT** | PR | Implement safeguards | 5 |
| **DETECT** | DE | Identify cybersecurity events | 2 |
| **RESPOND** | RS | Take action on incidents | 4 |
| **RECOVER** | RC | Restore capabilities | 2 |

### Framework Structure

```
CSF CORE
├── GOVERN (GV)
│   ├── Organizational Context (GV.OC)
│   ├── Risk Management Strategy (GV.RM)
│   ├── Roles, Responsibilities (GV.RR)
│   ├── Policy (GV.PO)
│   ├── Oversight (GV.OV)
│   └── Supply Chain Risk Management (GV.SC)
├── IDENTIFY (ID)
│   ├── Asset Management (ID.AM)
│   ├── Risk Assessment (ID.RA)
│   └── Improvement (ID.IM)
├── PROTECT (PR)
│   ├── Identity Management & Access Control (PR.AA)
│   ├── Awareness and Training (PR.AT)
│   ├── Data Security (PR.DS)
│   ├── Platform Security (PR.PS)
│   └── Technology Infrastructure Resilience (PR.IR)
├── DETECT (DE)
│   ├── Continuous Monitoring (DE.CM)
│   └── Adverse Event Analysis (DE.AE)
├── RESPOND (RS)
│   ├── Incident Management (RS.MA)
│   ├── Incident Analysis (RS.AN)
│   ├── Incident Response Reporting (RS.CO)
│   └── Incident Mitigation (RS.MI)
└── RECOVER (RC)
    ├── Incident Recovery Plan Execution (RC.RP)
    └── Incident Recovery Communication (RC.CO)
```

---

## Implementation Tiers

| Tier | Name | Description |
|------|------|-------------|
| **Tier 1** | Partial | Ad hoc, reactive, limited awareness |
| **Tier 2** | Risk Informed | Risk-aware but not organization-wide |
| **Tier 3** | Repeatable | Formal, consistent, organization-wide |
| **Tier 4** | Adaptive | Continuous improvement, predictive |

See the [Implementation Tiers Guide](./implementation-tiers-guide.md) for detailed guidance.

---

## Using the CSF

### Implementation Steps

1. **Prioritize and Scope** - Define objectives and scope
2. **Orient** - Identify assets, threats, and requirements
3. **Create Current Profile** - Assess current state
4. **Conduct Risk Assessment** - Analyze risks
5. **Create Target Profile** - Define desired state
6. **Determine Gaps** - Compare current to target
7. **Implement Action Plan** - Execute improvements

### When to Use CSF

| Scenario | CSF Value |
|----------|-----------|
| Building security program | Comprehensive framework |
| Risk-based approach needed | Risk management focus |
| Board/executive communication | Common language |
| Multiple framework requirements | Maps to other frameworks |
| Measuring improvement | Profiles and tiers |
| Supply chain security | Dedicated GV.SC category |

---

## CSF and Other Frameworks

### CSF to ISO 27001 Coverage

| CSF Function | ISO 27001 Coverage |
|--------------|-------------------|
| GOVERN | Clauses 4-10, A.5.1-5.4 |
| IDENTIFY | A.5.9-5.14, 6.1 |
| PROTECT | A.5.15-5.18, A.6, A.7, A.8 |
| DETECT | A.8.15-8.16 |
| RESPOND | A.5.24-5.28 |
| RECOVER | A.5.29-5.30 |

See the [detailed mapping](./nist-iso27001-mapping.md) for subcategory-level alignment.

### Complementary Frameworks

| Framework | Relationship |
|-----------|--------------|
| **ISO 27001** | CSF outcomes, ISO controls |
| **CIS Controls** | Specific implementation guidance |
| **NIST 800-53** | Detailed control catalog |
| **COBIT** | Governance alignment |

---

## Resources by Role

### For CISOs and Security Leaders
- [NIST CSF 2.0 Guide](./nist-csf-guide.md) - Full framework understanding
- [Implementation Tiers Guide](./implementation-tiers-guide.md) - Maturity measurement
- [CSF Profile Template](./csf-profile-template.md) - Strategic planning

### For Security Practitioners
- [CSF Assessment Template](./csf-assessment-template.md) - Hands-on assessment
- [CSF Implementation Guide](./csf-implementation-guide.md) - Implementation steps
- [NIST-ISO 27001 Mapping](./nist-iso27001-mapping.md) - Control alignment

### For Risk Managers
- [NIST CSF 2.0 Guide](./nist-csf-guide.md) - Risk management integration
- [CSF Profile Template](./csf-profile-template.md) - Risk-based profiles
- [Implementation Tiers Guide](./implementation-tiers-guide.md) - Risk maturity

### For Auditors and Assessors
- [CSF Assessment Template](./csf-assessment-template.md) - Assessment methodology
- [NIST-ISO 27001 Mapping](./nist-iso27001-mapping.md) - Cross-framework evidence

---

## External Resources

| Resource | Link |
|----------|------|
| NIST CSF Official Website | [nist.gov/cyberframework](https://www.nist.gov/cyberframework) |
| CSF 2.0 Document | [NIST.CSWP.29](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf) |
| CSF 2.0 Reference Tool | [csf.tools](https://csf.tools) |
| NIST SP 800-53 | Security and Privacy Controls |
| NIST SP 800-37 | Risk Management Framework |

---

## Contributing

We welcome contributions to expand this section:
- Industry-specific profiles
- Implementation case studies
- Additional mappings
- Tool integrations

See [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines.

---

## Document History

| Version | Date | Changes |
|---------|------|---------|
| 2.0 | [DATE] | Major expansion - guides, templates, mappings added |
| 1.0 | [DATE] | Initial placeholder |

---

[Back to Frameworks](../README.md) | [Back to Home](../../README.md)

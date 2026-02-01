# Risk Assessment

This section provides templates, methodologies, and tools for conducting information security risk assessments.

## Contents

- [Templates](./templates/README.md) - Risk register, assessment forms, treatment plans
- [Methodologies](./methodologies/README.md) - Risk assessment approaches and frameworks

## Quick Links

| Resource | Purpose |
|----------|---------|
| [Risk Register Template](./templates/risk-register-template.md) | Track identified risks |
| [Risk Assessment Template](./templates/risk-assessment-template.md) | Document assessment findings |
| [Risk Treatment Plan](./templates/risk-treatment-plan-template.md) | Plan risk responses |
| [Asset Inventory Template](./templates/asset-inventory-template.md) | Catalog information assets |
| [Risk Assessment Methodology](./methodologies/risk-assessment-methodology.md) | How to conduct assessments |

## Risk Assessment Process Overview

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   1. Context    │────▶│  2. Identify    │────▶│   3. Analyze    │
│  Establishment  │     │     Risks       │     │     Risks       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
                                                        │
                                                        ▼
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  6. Monitor &   │◀────│   5. Implement  │◀────│   4. Evaluate   │
│     Review      │     │   Treatment     │     │   & Treat       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

## Risk Assessment Types

| Type | When | Scope |
|------|------|-------|
| **Enterprise Risk Assessment** | Annually, major changes | Entire organization |
| **System Risk Assessment** | New systems, changes | Specific system |
| **Vendor Risk Assessment** | New vendors, renewals | Third-party relationship |
| **Project Risk Assessment** | New projects | Project scope |
| **Targeted Assessment** | Specific concerns | Narrow scope |

## Risk Criteria

### Impact Scale

| Level | Rating | Financial Impact | Operational Impact | Reputational Impact |
|-------|--------|------------------|-------------------|---------------------|
| **Critical** | 5 | > $[X]M | Business-critical failure | Major media coverage |
| **High** | 4 | $[X]K - $[X]M | Significant disruption | Regional media |
| **Medium** | 3 | $[X]K - $[X]K | Moderate disruption | Customer complaints |
| **Low** | 2 | < $[X]K | Minor inconvenience | Isolated incidents |
| **Negligible** | 1 | Minimal | No operational impact | No external impact |

### Likelihood Scale

| Level | Rating | Frequency | Probability |
|-------|--------|-----------|-------------|
| **Almost Certain** | 5 | Multiple times per year | > 90% |
| **Likely** | 4 | Once per year | 50-90% |
| **Possible** | 3 | Once in 2-3 years | 25-50% |
| **Unlikely** | 2 | Once in 5 years | 5-25% |
| **Rare** | 1 | Less than once in 5 years | < 5% |

### Risk Matrix

|  | Negligible (1) | Low (2) | Medium (3) | High (4) | Critical (5) |
|--|----------------|---------|------------|----------|--------------|
| **Almost Certain (5)** | Medium | Medium | High | Critical | Critical |
| **Likely (4)** | Low | Medium | High | High | Critical |
| **Possible (3)** | Low | Medium | Medium | High | High |
| **Unlikely (2)** | Low | Low | Medium | Medium | High |
| **Rare (1)** | Low | Low | Low | Medium | Medium |

### Risk Response by Level

| Risk Level | Response | Approval |
|------------|----------|----------|
| **Critical** | Immediate action required | Executive/Board |
| **High** | Treatment plan required | Senior Management |
| **Medium** | Treatment plan or acceptance | Management |
| **Low** | Monitor or accept | Risk Owner |

## Treatment Options

| Option | Description | When to Use |
|--------|-------------|-------------|
| **Avoid** | Eliminate the risk source | Unacceptable risk, viable alternative exists |
| **Mitigate** | Reduce likelihood or impact | Cost-effective controls available |
| **Transfer** | Share risk with third party | Insurance, outsourcing appropriate |
| **Accept** | Acknowledge and monitor | Low risk or no viable treatment |

## Framework Alignment

| Framework | Risk Assessment Requirement |
|-----------|----------------------------|
| ISO 27001 | Clause 6.1.2, 8.2 |
| NIST CSF | ID.RA, ID.RM |
| SOC 2 | CC3.1-CC3.4 |
| GDPR | Article 35 (DPIA) |

## Related Documents

- [Information Security Policy](../policies/information-security-policy.md)
- [ISO 27001 Framework](../frameworks/iso-27001/README.md)
- [Risk Assessment Procedure](../procedures/risk-assessment-procedure.md)

---

[Back to Home](../README.md)

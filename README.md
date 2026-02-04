# OpenGRC Toolkit

**A free, open, and collaborative toolbox for information security professionals.**

OpenGRC Toolkit provides ready-to-use templates, policies, procedures, and tools for information security managers, consultants, crisis teams, and independent security professionals. Whether you're implementing ISO 27001, preparing for SOC 2, or building an incident response capability from scratch—start here.

---

## Project Status

| Metric | Count |
|--------|-------|
| **Total Documents** | **123** |
| Policies | 21 |
| Procedures | 19 (12 general + 6 ISO + 1 GDPR) |
| Checklists | 10 |
| Playbooks | 13 |
| Templates | 11 general + 10 crisis |
| Risk Assessment | 6 |
| ISO 27001 Controls | 93 |
| GDPR Resources | 7 |
| NIST CSF Resources | 6 |

**Current Focus:** Framework expansion - **ISO 27001, GDPR, and NIST CSF now active!**

---

## Quick Navigation

| Category | Description | Status |
|----------|-------------|--------|
| [Frameworks](./frameworks/README.md) | Framework-specific guides and mappings | ISO 27001 + GDPR + NIST CSF active |
| [Policies](./policies/README.md) | Ready-to-customize security policy templates | **21 policies (complete)** |
| [Procedures](./procedures/README.md) | Step-by-step operational procedures | **19 procedures** |
| [Risk Assessment](./risk-assessment/README.md) | Risk assessment templates and methodologies | Available |
| [Checklists](./checklists/README.md) | Audit and implementation checklists | **10 checklists** |
| [Crisis Management](./crisis-management/README.md) | Incident response playbooks and crisis templates | **13 playbooks** |
| [Templates](./templates/README.md) | General-purpose document templates | **21 templates** |
| [Tools](./tools/README.md) | Scripts and utilities for security operations | Planned |

---

## What's Available

### Policies (21) - Complete ISO 27001 Coverage

#### Core ISMS Policies (Critical)
| Policy | ISO 27001 Mapping |
|--------|-------------------|
| [Information Security Policy](./policies/information-security-policy.md) | 5.2, A.5.1 |
| [Access Control Policy](./policies/access-control-policy.md) | A.5.15-A.5.18 |
| [Acceptable Use Policy](./policies/acceptable-use-policy.md) | A.5.10 |
| [Data Classification Policy](./policies/data-classification-policy.md) | A.5.12-A.5.13 |
| [Password Policy](./policies/password-policy.md) | A.5.17 |

#### Operational Policies (Critical)
| Policy | ISO 27001 Mapping |
|--------|-------------------|
| [Incident Response Policy](./policies/incident-response-policy.md) | A.5.24-A.5.28 |
| [Business Continuity Policy](./policies/business-continuity-policy.md) | A.5.29-A.5.30 |
| [Backup Policy](./policies/backup-policy.md) | A.8.13 |
| [Change Management Policy](./policies/change-management-policy.md) | A.8.32 |
| [Vulnerability Management Policy](./policies/vulnerability-management-policy.md) | A.8.8 |

#### People & Physical Policies
| Policy | ISO 27001 Mapping |
|--------|-------------------|
| [Human Resources Security Policy](./policies/human-resources-security-policy.md) | A.6.1-A.6.6 |
| [Remote Work Policy](./policies/remote-work-policy.md) | A.6.7 |
| [Mobile Device Policy](./policies/mobile-device-policy.md) | A.8.1 |
| [Physical Security Policy](./policies/physical-security-policy.md) | A.7.1-A.7.14 |

#### Asset & Data Policies
| Policy | ISO 27001 Mapping |
|--------|-------------------|
| [Asset Management Policy](./policies/asset-management-policy.md) | A.5.9-A.5.11 |
| [Data Protection Policy](./policies/data-protection-policy.md) | A.5.34 |
| [Information Transfer Policy](./policies/information-transfer-policy.md) | A.5.14 |

#### Technical Policies
| Policy | ISO 27001 Mapping |
|--------|-------------------|
| [Supplier Security Policy](./policies/supplier-security-policy.md) | A.5.19-A.5.23 |
| [Cryptography Policy](./policies/cryptography-policy.md) | A.8.24 |
| [Secure Development Policy](./policies/secure-development-policy.md) | A.8.25-A.8.31 |
| [Logging and Monitoring Policy](./policies/logging-monitoring-policy.md) | A.8.15-A.8.16 |
| [Network Security Policy](./policies/network-security-policy.md) | A.8.20-A.8.22 |

### Procedures (19)

**General Procedures (12):**
- [Incident Response Procedure](./procedures/incident-response-procedure.md)
- [User Access Request Procedure](./procedures/user-access-request-procedure.md)
- [Access Review Procedure](./procedures/access-review-procedure.md)
- [User Offboarding Procedure](./procedures/user-offboarding-procedure.md)
- [Change Management Procedure](./procedures/change-management-procedure.md)
- [Backup and Recovery Procedure](./procedures/backup-procedure.md)
- [Internal Audit Procedure](./procedures/internal-audit-procedure.md)
- [Patch Management Procedure](./procedures/patch-management-procedure.md) *(new)*
- [Vendor Security Assessment Procedure](./procedures/vendor-security-assessment-procedure.md) *(new)*
- [Disaster Recovery Procedure](./procedures/disaster-recovery-procedure.md) *(new)*
- [Data Subject Request Procedure](./procedures/data-subject-request-procedure.md) *(new)*
- [Security Awareness Procedure](./procedures/security-awareness-procedure.md) *(new)*

**ISO 27001 Specific Procedures (6):**
- [Management Review Procedure](./frameworks/iso-27001/procedures/management-review-procedure.md)
- [Corrective Action Procedure](./frameworks/iso-27001/procedures/corrective-action-procedure.md)
- [Risk Treatment Procedure](./frameworks/iso-27001/procedures/risk-treatment-procedure.md)
- [Document Control Procedure](./frameworks/iso-27001/procedures/document-control-procedure.md)
- [Risk Assessment Procedure](./frameworks/iso-27001/procedures/risk-assessment-procedure.md)

**GDPR Specific Procedure:**
- [GDPR Breach Notification Procedure](./frameworks/gdpr/breach-notification-procedure.md)

### Checklists (10)
- [ISO 27001 Implementation Checklist](./checklists/iso27001-implementation-checklist.md)
- [ISO 27001 Internal Audit Checklist](./checklists/iso27001-audit-checklist.md)
- [Pre-Certification Readiness Checklist](./checklists/pre-certification-checklist.md) *(new)*
- [Vendor Security Assessment Checklist](./checklists/vendor-security-checklist.md) *(new)*
- [Cloud Security Checklist](./checklists/cloud-security-checklist.md) *(new)*
- [Server Hardening Checklist](./checklists/server-hardening-checklist.md) *(new)*
- [Network Security Checklist](./checklists/network-security-checklist.md) *(new)*
- [Security Baseline Checklist](./checklists/security-baseline-checklist.md)
- [New Employee Onboarding Checklist](./checklists/new-employee-checklist.md)
- [Offboarding Checklist](./checklists/offboarding-checklist.md)

### Crisis Management
**Playbooks (13):**

Core Playbooks:
- [Ransomware Playbook](./crisis-management/playbooks/ransomware-playbook.md)
- [Data Breach Playbook](./crisis-management/playbooks/data-breach-playbook.md)
- [Phishing Playbook](./crisis-management/playbooks/phishing-playbook.md)
- [Malware Playbook](./crisis-management/playbooks/malware-playbook.md)
- [Account Compromise Playbook](./crisis-management/playbooks/account-compromise-playbook.md)

Infrastructure & Third-Party:
- [DDoS Attack Playbook](./crisis-management/playbooks/ddos-playbook.md)
- [Third-Party Breach Playbook](./crisis-management/playbooks/third-party-breach-playbook.md)
- [Website Defacement Playbook](./crisis-management/playbooks/website-defacement-playbook.md)
- [Cloud Security Incident Playbook](./crisis-management/playbooks/cloud-security-incident-playbook.md)

Physical & Human:
- [Lost/Stolen Device Playbook](./crisis-management/playbooks/lost-device-playbook.md)
- [Insider Threat Playbook](./crisis-management/playbooks/insider-threat-playbook.md)
- [Social Engineering Playbook](./crisis-management/playbooks/social-engineering-playbook.md)
- [Physical Security Playbook](./crisis-management/playbooks/physical-security-playbook.md)

**Templates:**
- [Incident Report Template](./crisis-management/templates/incident-report-template.md)

### Risk Assessment
- [Risk Assessment Methodology](./risk-assessment/methodologies/risk-assessment-methodology.md)
- [Risk Register Template](./risk-assessment/templates/risk-register-template.md)
- [Risk Assessment Report Template](./risk-assessment/templates/risk-assessment-template.md)
- [Asset Inventory Template](./risk-assessment/templates/asset-inventory-template.md)

### ISO 27001 Specific
- [Statement of Applicability Template](./frameworks/iso-27001/statement-of-applicability.md)
- [All 93 Annex A Controls Reference](./frameworks/iso-27001/controls/README.md)
- [Implementation Roadmap](./frameworks/iso-27001/README.md)

### GDPR Resources
- [GDPR Requirements Guide](./frameworks/gdpr/gdpr-requirements-guide.md)
- [Records of Processing Activities (RoPA)](./frameworks/gdpr/ropa-template.md)
- [Privacy Notice Template](./frameworks/gdpr/privacy-notice-template.md)
- [Cookie Policy Template](./frameworks/gdpr/cookie-policy-template.md)
- [Lawful Basis Assessment Guide](./frameworks/gdpr/lawful-basis-guide.md)
- [International Transfers Guide](./frameworks/gdpr/international-transfers-guide.md)
- [GDPR Breach Notification Procedure](./frameworks/gdpr/breach-notification-procedure.md)

### NIST CSF 2.0 Resources
- [NIST CSF 2.0 Guide](./frameworks/nist-csf/nist-csf-guide.md)
- [CSF Assessment Template](./frameworks/nist-csf/csf-assessment-template.md)
- [CSF Profile Template](./frameworks/nist-csf/csf-profile-template.md)
- [Implementation Tiers Guide](./frameworks/nist-csf/implementation-tiers-guide.md)
- [CSF Implementation Guide](./frameworks/nist-csf/csf-implementation-guide.md)
- [NIST CSF to ISO 27001 Mapping](./frameworks/nist-csf/nist-iso27001-mapping.md)

### Templates
- [Vendor Security Questionnaire](./templates/vendor-security-questionnaire.md)
- [Access Request Form](./templates/access-request-form.md)
- [Exception Request Form](./templates/exception-request-form.md)
- [Management Review Agenda](./templates/management-review-agenda.md)
- [Business Impact Analysis](./templates/business-impact-analysis.md)
- [Non-Disclosure Agreement (NDA)](./templates/nda-template.md)

---

## What's Missing (Roadmap)

### High Priority - Complete ISO 27001 Implementation

#### Procedures Still Needed
- [x] ~~Patch Management Procedure~~ ✓ Complete
- [x] ~~Vendor Security Assessment Procedure~~ ✓ Complete
- [x] ~~Management Review Procedure~~ ✓ Complete (ISO-specific)
- [x] ~~Corrective Action Procedure~~ ✓ Complete (ISO-specific)
- [x] ~~Document Control Procedure~~ ✓ Complete (ISO-specific)
- [x] ~~Security Awareness Training Procedure~~ ✓ Complete
- [x] ~~Risk Treatment Procedure~~ ✓ Complete (ISO-specific)
- [x] ~~Disaster Recovery Procedure~~ ✓ Complete
- [x] ~~Data Subject Request Procedure (GDPR)~~ ✓ Complete

#### Checklists Still Needed
- [x] ~~Pre-Certification Readiness Checklist~~ ✓ Complete
- [x] ~~Vendor Security Assessment Checklist~~ ✓ Complete
- [x] ~~Cloud Security Checklist~~ ✓ Complete
- [x] ~~Server Hardening Checklist~~ ✓ Complete
- [x] ~~Network Security Checklist~~ ✓ Complete

#### Playbooks Still Needed
- [x] ~~DDoS Attack Playbook~~ ✓ Complete
- [x] ~~Malware Infection Playbook~~ ✓ Complete
- [x] ~~Account Compromise Playbook~~ ✓ Complete
- [x] ~~Third-Party Breach Playbook~~ ✓ Complete
- [x] ~~Website Defacement Playbook~~ ✓ Complete
- [x] ~~Cloud Security Incident Playbook~~ ✓ Complete

#### Templates Still Needed
- [x] ~~Data Processing Agreement (DPA) Template~~ ✓ Complete
- [x] ~~Security Metrics Report Template~~ ✓ Complete
- [x] ~~Internal Audit Report Template~~ ✓ Complete
- [x] ~~Corrective Action Request Form~~ ✓ Complete
- [x] ~~Threat Catalog~~ ✓ Complete
- [x] ~~DPIA Template~~ ✓ Complete
- [x] ~~Communication Templates~~ ✓ Complete (10 crisis templates added)

### Medium Priority - Framework Expansion

#### NIST CSF 2.0
- [x] ~~Framework overview and implementation guide~~ ✓ Complete
- [x] ~~Function/Category/Subcategory mapping~~ ✓ Complete
- [x] ~~NIST CSF to ISO 27001 control mapping~~ ✓ Complete
- [x] ~~Self-assessment template~~ ✓ Complete
- [x] ~~Implementation tiers guide~~ ✓ Complete
- [x] ~~Profile template~~ ✓ Complete

#### SOC 2
- [ ] Trust Service Criteria overview
- [ ] Common Criteria (CC) control mapping
- [ ] SOC 2 readiness checklist
- [ ] Evidence collection guide

#### GDPR
- [x] ~~GDPR requirements overview~~ ✓ Complete
- [x] ~~Records of Processing Activities (RoPA) template~~ ✓ Complete
- [x] ~~Data Subject Rights procedures~~ ✓ Complete
- [x] ~~DPIA methodology~~ ✓ Complete
- [x] ~~Privacy policy templates~~ ✓ Complete
- [x] ~~Breach notification templates~~ ✓ Complete
- [x] ~~Lawful basis guide~~ ✓ Complete
- [x] ~~International transfers guide~~ ✓ Complete
- [x] ~~Cookie policy template~~ ✓ Complete

### Lower Priority - Enhancements

#### Tools and Automation
- [ ] Risk calculator spreadsheet
- [ ] Control mapping matrix (ISO/NIST/SOC2)
- [ ] Asset inventory CSV template
- [ ] Policy acknowledgment tracker

#### Additional Resources
- [ ] Security awareness training materials
- [ ] Executive presentation templates
- [ ] Board reporting templates
- [ ] Compliance dashboard examples

---

## Framework Coverage

| Framework | Status | Progress | Documentation |
|-----------|--------|----------|---------------|
| ISO 27001:2022 | **Active** | **98%** | [View](./frameworks/iso-27001/README.md) |
| GDPR | **Active** | **80%** | [View](./frameworks/gdpr/README.md) |
| NIST CSF 2.0 | **Active** | **75%** | [View](./frameworks/nist-csf/README.md) |
| SOC 2 | Planned | 5% | [View](./frameworks/soc2/README.md) |
| PCI DSS | Not Started | 0% | - |
| HIPAA | Not Started | 0% | - |
| CIS Controls | Not Started | 0% | - |

---

## Getting Started

### For Consultants
1. Browse the [Frameworks](./frameworks/README.md) section for your target compliance framework
2. Use the [Policies](./policies/README.md) as starting templates for client engagements
3. Customize the [Risk Assessment](./risk-assessment/README.md) templates for your methodology

### For Security Managers
1. Start with the [Information Security Policy](./policies/information-security-policy.md) as your foundation
2. Implement [Procedures](./procedures/README.md) to operationalize your policies
3. Use [Checklists](./checklists/README.md) for ongoing compliance monitoring

### For Crisis Teams
1. Review the [Crisis Management](./crisis-management/README.md) section
2. Adapt the [Incident Response Playbooks](./crisis-management/playbooks/README.md)
3. Prepare your [Communication Templates](./crisis-management/templates/README.md)

### For Privacy/DPO Teams
1. Start with the [GDPR Requirements Guide](./frameworks/gdpr/gdpr-requirements-guide.md)
2. Create your [Records of Processing Activities](./frameworks/gdpr/ropa-template.md)
3. Implement the [Data Subject Request Procedure](./procedures/data-subject-request-procedure.md)
4. Use the [DPIA Template](./templates/dpia-template.md) for high-risk processing

---

## How to Use This Repository

### 1. Clone or Download
```bash
git clone https://github.com/YOUR-USERNAME/OpenGRC-Toolkit.git
```

### 2. Customize Templates
All documents contain placeholder text marked with:
- `[ORGANIZATION NAME]` - Replace with client/company name
- `[DATE]` - Replace with effective date
- `[ROLE/TITLE]` - Replace with responsible party
- `<!-- CUSTOMIZE: ... -->` - Notes for customization

### 3. Implement and Track
Use the checklists to track implementation progress and ensure completeness.

---

## Document Naming Conventions

| Type | Format | Example |
|------|--------|---------|
| Policies | `[topic]-policy.md` | `access-control-policy.md` |
| Procedures | `[topic]-procedure.md` | `incident-response-procedure.md` |
| Templates | `[type]-template.md` | `risk-register-template.md` |
| Checklists | `[topic]-checklist.md` | `iso27001-audit-checklist.md` |
| Playbooks | `[topic]-playbook.md` | `ransomware-playbook.md` |

---

## Contributing

We welcome contributions from the security community. See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

### Priority Contributions Needed
1. **NIST CSF 2.0 content** - Framework documentation and control mappings
2. **SOC 2 content** - Trust Service Criteria documentation
3. **Additional Playbooks** - Cryptojacking, IoT/OT Compromise
4. **Translations** - Non-English versions of documents

### Ways to Contribute
- Submit new templates or policies
- Improve existing documentation
- Add framework mappings
- Report issues or suggest enhancements
- Translate documents to other languages
- Share real-world lessons learned (anonymized)

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material
- **Adapt** — remix, transform, and build upon the material for any purpose

Under the following terms:
- **Attribution** — You must give appropriate credit and indicate if changes were made

---

## Disclaimer

These templates are provided as starting points and general guidance. They should be customized to fit your organization's specific context, risk appetite, and regulatory requirements. This toolkit does not constitute legal or professional advice. Always consult with qualified professionals for your specific situation.

---

## Support This Project

If you find this toolkit useful:
- Star this repository
- Share it with colleagues
- Contribute improvements
- Report issues

---

## Changelog

| Date | Changes |
|------|---------|
| 2024-XX-XX | **NIST CSF 2.0 Framework**: 6 new resources (guide, assessment, profile, tiers, implementation, ISO mapping) |
| 2024-XX-XX | **GDPR Framework**: 7 new resources (requirements guide, RoPA, privacy notice, lawful basis guide, international transfers, cookie policy, breach notification) |
| 2024-XX-XX | Playbooks expanded: 13 incident response playbooks (added Website Defacement, Cloud Security) |
| 2024-XX-XX | Templates expanded: 21 templates (11 general + 10 crisis communication) |
| 2024-XX-XX | Policy set completed: 21 policies with full ISO 27001 coverage |
| 2024-XX-XX | Initial release with 57 documents |

---

*Built by the community, for the community.*

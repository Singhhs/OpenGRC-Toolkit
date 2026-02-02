# Asset Inventory Template

**Organization:** [ORGANIZATION NAME]
**Version:** [VERSION]
**Last Updated:** [DATE]
**Owner:** [ROLE]

---

## Purpose

This document provides a template for maintaining an inventory of information assets as required by ISO 27001 (A.5.9) and other security frameworks.

---

## Asset Categories

| Category | Description | Examples |
|----------|-------------|----------|
| **Hardware** | Physical computing equipment | Servers, workstations, network devices |
| **Software** | Applications and systems | Operating systems, business applications |
| **Data/Information** | Digital and physical information | Databases, files, records |
| **Services** | IT and business services | Cloud services, hosting, communications |
| **People** | Key roles with critical knowledge | System administrators, key personnel |
| **Intangible** | Non-physical assets | Reputation, intellectual property |

---

## Hardware Assets

| Asset ID | Asset Name | Type | Location | Owner | Custodian | Classification | Criticality | Serial/Tag | Status |
|----------|------------|------|----------|-------|-----------|----------------|-------------|------------|--------|
| HW-001 | | Server/Workstation/Network | | | | Confidential/Internal | Critical/High/Medium/Low | | Active/Retired |
| HW-002 | | | | | | | | | |
| HW-003 | | | | | | | | | |

### Hardware Details Template

| Field | Description |
|-------|-------------|
| **Asset ID** | Unique identifier (HW-XXX) |
| **Asset Name** | Descriptive name |
| **Type** | Server, Workstation, Laptop, Network Device, Mobile, Storage, etc. |
| **Make/Model** | Manufacturer and model |
| **Serial Number** | Manufacturer serial number |
| **Asset Tag** | Internal asset tag number |
| **Location** | Physical location (building, room, rack) |
| **IP Address** | If applicable |
| **Owner** | Business owner responsible for asset |
| **Custodian** | Person/team with physical control |
| **Classification** | Data classification level |
| **Criticality** | Business criticality (Critical/High/Medium/Low) |
| **Purchase Date** | Date acquired |
| **Warranty Expiry** | Warranty end date |
| **End of Life** | Expected retirement date |
| **Status** | Active, Maintenance, Retired, Disposed |
| **Notes** | Additional information |

---

## Software Assets

| Asset ID | Software Name | Type | Version | License Type | License Count | Owner | Installed On | Classification | Criticality |
|----------|---------------|------|---------|--------------|---------------|-------|--------------|----------------|-------------|
| SW-001 | | OS/Application/Database | | Perpetual/Subscription | | | | | |
| SW-002 | | | | | | | | | |
| SW-003 | | | | | | | | | |

### Software Details Template

| Field | Description |
|-------|-------------|
| **Asset ID** | Unique identifier (SW-XXX) |
| **Software Name** | Application/system name |
| **Type** | Operating System, Application, Database, Security, Utility |
| **Vendor** | Software vendor |
| **Version** | Current version |
| **License Type** | Perpetual, Subscription, Open Source, OEM |
| **License Key** | License reference (stored securely) |
| **License Count** | Number of licenses |
| **License Expiry** | Expiration date |
| **Owner** | Business owner |
| **Installed On** | Hardware assets where installed |
| **Classification** | Data classification |
| **Criticality** | Business criticality |
| **Support Contract** | Support agreement reference |
| **Support Expiry** | Support end date |
| **Notes** | Additional information |

---

## Data/Information Assets

| Asset ID | Data Name | Type | Format | Location | Owner | Custodian | Classification | Retention | Backup |
|----------|-----------|------|--------|----------|-------|-----------|----------------|-----------|--------|
| DA-001 | | Database/File/Record | | | | | | | Yes/No |
| DA-002 | | | | | | | | | |
| DA-003 | | | | | | | | | |

### Data Asset Details Template

| Field | Description |
|-------|-------------|
| **Asset ID** | Unique identifier (DA-XXX) |
| **Data Name** | Descriptive name |
| **Description** | What the data contains |
| **Type** | Database, File Share, Document, Record, Email |
| **Format** | Electronic, Paper, Both |
| **Location** | Where data is stored (server, cloud, physical) |
| **Owner** | Data owner (business accountability) |
| **Custodian** | Data custodian (technical custody) |
| **Classification** | Restricted/Confidential/Internal/Public |
| **Contains PII** | Yes/No |
| **Contains Financial** | Yes/No |
| **Regulatory Requirements** | GDPR, HIPAA, PCI, etc. |
| **Retention Period** | How long to retain |
| **Backup** | Is data backed up (Yes/No) |
| **Backup Frequency** | How often backed up |
| **Encryption** | Encrypted at rest (Yes/No) |
| **Access Control** | How access is controlled |
| **Notes** | Additional information |

---

## Service Assets

| Asset ID | Service Name | Type | Provider | Owner | Classification | Criticality | Contract Ref | SLA | Expiry |
|----------|--------------|------|----------|-------|----------------|-------------|--------------|-----|--------|
| SV-001 | | Cloud/Hosting/Communication | | | | | | | |
| SV-002 | | | | | | | | | |
| SV-003 | | | | | | | | | |

### Service Details Template

| Field | Description |
|-------|-------------|
| **Asset ID** | Unique identifier (SV-XXX) |
| **Service Name** | Name of service |
| **Type** | Cloud SaaS, Cloud IaaS, Hosting, Communication, Outsourced |
| **Description** | What the service provides |
| **Provider** | Service provider/vendor |
| **Owner** | Internal business owner |
| **Classification** | Data classification handled |
| **Criticality** | Business criticality |
| **Contract Reference** | Contract identifier |
| **Contract Expiry** | Contract end date |
| **SLA** | Service level agreement details |
| **Data Location** | Where provider stores data |
| **Security Certifications** | Provider certifications (ISO 27001, SOC 2) |
| **Last Assessment** | Last security assessment date |
| **Notes** | Additional information |

---

## People Assets (Key Roles)

| Asset ID | Role | Department | Key Knowledge/Skills | Backup Person | Criticality |
|----------|------|------------|---------------------|---------------|-------------|
| PE-001 | | | | | |
| PE-002 | | | | | |

---

## Asset Classification Guidelines

### Criticality Levels

| Level | Definition | RTO Guidance |
|-------|------------|--------------|
| **Critical** | Failure causes immediate, severe business impact | < 4 hours |
| **High** | Failure causes significant business disruption | < 24 hours |
| **Medium** | Failure causes moderate business impact | < 72 hours |
| **Low** | Failure causes minimal business impact | > 72 hours |

### Data Classification Levels

| Level | Definition | Handling |
|-------|------------|----------|
| **Restricted** | Highly sensitive, legal/regulatory protection required | Strictest controls, need-to-know, encrypted |
| **Confidential** | Sensitive business information | Access controls, encrypted in transit |
| **Internal** | General business information | Employee access, not public |
| **Public** | Approved for public release | No restrictions |

---

## Asset Lifecycle

| Stage | Activities |
|-------|------------|
| **Acquisition** | Register in inventory, assign owner, classify |
| **Deployment** | Configure security controls, document location |
| **Operation** | Regular review, update records, maintain |
| **Retirement** | Plan decommission, secure disposal, update inventory |
| **Disposal** | Secure destruction, certificate, remove from inventory |

---

## Review Schedule

| Review Type | Frequency | Responsibility |
|-------------|-----------|----------------|
| Full inventory review | Annually | Asset Manager / IT |
| New asset registration | Within 5 days of acquisition | Asset Owner |
| Disposal verification | At disposal | IT / Security |
| Critical asset review | Quarterly | IT / Business Owners |

---

## Related Documents

- [Data Classification Policy](../../policies/data-classification-policy.md)
- [Risk Assessment Methodology](../methodologies/risk-assessment-methodology.md)
- [Acceptable Use Policy](../../policies/acceptable-use-policy.md)

---

[Back to Templates](./README.md) | [Back to Risk Assessment](../README.md)

# Asset Management Policy

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Next Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Director / CISO] |
| **Approved By** | [ROLE - e.g., CIO] |
| **Classification** | Internal |

---

## 1. Purpose

This policy establishes requirements for identifying, classifying, and managing information assets throughout their lifecycle at [ORGANIZATION NAME] to ensure appropriate protection.

## 2. Scope

This policy applies to:
- All information assets owned or managed by [ORGANIZATION NAME]
- All employees, contractors, and third parties who use company assets
- All locations where assets are used or stored

## 3. Definitions

| Term | Definition |
|------|------------|
| **Information Asset** | Anything of value to the organization including hardware, software, data, services, and people with critical knowledge |
| **Asset Owner** | Person accountable for the asset's protection and appropriate use |
| **Asset Custodian** | Person responsible for day-to-day management and protection |
| **Asset Register** | Inventory of all information assets |

## 4. Asset Categories

| Category | Description | Examples |
|----------|-------------|----------|
| **Hardware** | Physical IT equipment | Servers, workstations, laptops, network devices, mobile devices |
| **Software** | Applications and systems | Operating systems, applications, databases, development tools |
| **Data/Information** | Electronic and physical information | Databases, files, documents, records |
| **Services** | IT and business services | Cloud services, hosting, communications |
| **People** | Personnel with critical knowledge | Key personnel, specialized skills |
| **Intangible** | Non-physical assets | Reputation, intellectual property, brand |

## 5. Policy Statements

### 5.1 Asset Inventory

#### 5.1.1 Inventory Requirements

All information assets shall be:
- Identified and recorded in the asset register
- Assigned a unique identifier
- Classified according to value and sensitivity
- Assigned an owner

#### 5.1.2 Asset Register Contents

The asset register shall include:

| Field | Description |
|-------|-------------|
| Asset ID | Unique identifier |
| Name/Description | Clear description |
| Category | Hardware, software, data, etc. |
| Owner | Accountable person/role |
| Custodian | Responsible for day-to-day management |
| Location | Physical or logical location |
| Classification | Security classification |
| Criticality | Business criticality rating |
| Value | Financial or strategic value |
| Status | Active, retired, disposed |

#### 5.1.3 Inventory Maintenance

- Asset register reviewed at least annually
- Updates made within [5] business days of changes
- Automated discovery tools used where possible
- Regular reconciliation with physical assets

### 5.2 Asset Ownership

#### 5.2.1 Owner Responsibilities

Asset owners shall:
- Ensure appropriate classification
- Define access requirements
- Approve access requests
- Review access periodically
- Ensure adequate protection
- Manage asset lifecycle
- Participate in risk assessments

#### 5.2.2 Custodian Responsibilities

Asset custodians shall:
- Implement security controls
- Maintain asset according to requirements
- Report security concerns
- Support owner in protection duties

#### 5.2.3 User Responsibilities

Asset users shall:
- Use assets only for authorized purposes
- Comply with acceptable use policy
- Protect assets in their possession
- Report loss, theft, or damage
- Return assets when required

### 5.3 Asset Classification

#### 5.3.1 Classification Scheme

All assets shall be classified based on the data they contain or process:

| Classification | Description | Examples |
|----------------|-------------|----------|
| **Restricted** | Highest sensitivity, significant harm if disclosed | Trade secrets, credentials, regulated personal data |
| **Confidential** | Sensitive business information | Financial data, contracts, employee data |
| **Internal** | For internal use only | Policies, procedures, internal communications |
| **Public** | Approved for public release | Marketing materials, public website content |

#### 5.3.2 Criticality Rating

Assets shall be rated for business criticality:

| Rating | RTO | Description |
|--------|-----|-------------|
| **Critical** | < 4 hours | Essential for operations, severe impact if unavailable |
| **High** | < 24 hours | Important functions, significant impact |
| **Medium** | < 72 hours | Supporting functions, moderate impact |
| **Low** | > 72 hours | Non-essential, minimal impact |

### 5.4 Acceptable Use

#### 5.4.1 General Requirements

- Assets used only for authorized business purposes
- Limited personal use permitted per [Acceptable Use Policy](./acceptable-use-policy.md)
- Assets not to be modified without authorization
- Security controls not to be disabled or bypassed

#### 5.4.2 Prohibited Activities

- Unauthorized copying or distribution
- Installation of unauthorized software
- Connection of unauthorized devices
- Removal of assets without approval
- Use for illegal activities

### 5.5 Asset Lifecycle

#### 5.5.1 Acquisition

Before acquiring assets:
- Business need justified
- Security requirements defined
- Vendor security assessed (if applicable)
- Budget approved
- Procurement follows policy

#### 5.5.2 Deployment

Before deployment:
- Asset registered in inventory
- Owner and custodian assigned
- Security configuration applied
- Access controls implemented
- Asset labeled/tagged

#### 5.5.3 Operation

During operation:
- Asset maintained per requirements
- Security updates applied
- Access reviewed periodically
- Changes controlled
- Monitoring active

#### 5.5.4 Return of Assets

When assets change hands:
- Assets returned upon role change or termination
- Data properly transferred or removed
- Asset register updated
- Condition documented

#### 5.5.5 Retirement and Disposal

When retiring assets:
- Planned decommission process
- Data securely removed
- Licenses reclaimed
- Environmentally responsible disposal
- Asset register updated
- Disposal documented

### 5.6 Asset Security

#### 5.6.1 Physical Security

- Assets physically secured per classification
- Portable assets protected from theft
- Secure storage when not in use
- Access restricted to authorized personnel

#### 5.6.2 Logical Security

- Access controls appropriate to classification
- Encryption for sensitive data
- Security software installed
- Regular updates and patches

#### 5.6.3 Media Handling

- Removable media controlled
- Encryption required for sensitive data
- Secure disposal when no longer needed
- Transport procedures for sensitive media

### 5.7 Asset Disposal

#### 5.7.1 Disposal Requirements

Before disposal:
- Data securely erased or destroyed
- Destruction verified
- Certificate of destruction obtained for sensitive assets
- Asset removed from inventory
- Licenses returned/cancelled

#### 5.7.2 Disposal Methods

| Asset Type | Disposal Method |
|------------|-----------------|
| Hard drives | Secure wipe (DOD 5220.22-M) or physical destruction |
| SSDs | Secure erase or physical destruction |
| Paper documents | Cross-cut shredding |
| Optical media | Physical destruction |
| Mobile devices | Factory reset + secure wipe |
| Whole systems | Certified ITAD vendor |

#### 5.7.3 Environmental Compliance

Disposal shall comply with:
- Environmental regulations
- WEEE directive (where applicable)
- Company sustainability policy

## 6. Special Asset Types

### 6.1 Mobile and Portable Assets

- Registered before use
- Encryption enabled
- Remote wipe capability
- Tracked via MDM where applicable
- Special care in transport

### 6.2 Cloud Assets

- Included in asset inventory
- Owner assigned
- Contract/subscription tracked
- Data location documented
- Exit strategy planned

### 6.3 Software Licenses

- All licenses tracked
- Compliance monitored
- Renewals managed
- Under/over licensing addressed

### 6.4 Intellectual Property

- Identified and documented
- Ownership clear
- Protection measures in place
- Access strictly controlled

## 7. Roles and Responsibilities

### 7.1 IT Department
- Maintain asset register
- Implement asset controls
- Support asset lifecycle
- Conduct audits

### 7.2 Procurement
- Follow asset acquisition procedures
- Coordinate with IT on requirements
- Track asset purchases

### 7.3 Finance
- Track asset values
- Manage depreciation
- Support audits

### 7.4 All Employees
- Use assets responsibly
- Report issues
- Return assets when required

## 8. Compliance

### 8.1 Monitoring

- Regular asset audits
- License compliance checks
- Reconciliation with inventory
- Exception reporting

### 8.2 Violations

Violations may result in:
- Disciplinary action
- Access revocation
- Recovery of costs
- Legal action if warranted

## 9. Related Documents

- [Information Security Policy](./information-security-policy.md)
- [Acceptable Use Policy](./acceptable-use-policy.md)
- [Data Classification Policy](./data-classification-policy.md)
- [Asset Inventory Template](../risk-assessment/templates/asset-inventory-template.md)
- [Disposal Procedure](../procedures/disposal-procedure.md)

## 10. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

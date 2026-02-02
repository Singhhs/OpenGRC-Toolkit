# Business Impact Analysis (BIA) Template

**Organization:** [ORGANIZATION NAME]
**BIA Date:** [DATE]
**Prepared By:** [NAME]
**Approved By:** [NAME]
**Version:** [VERSION]

---

## 1. Executive Summary

[Provide a brief summary of the BIA findings including:
- Number of processes/functions assessed
- Critical functions identified
- Key dependencies
- Recommended RTOs and RPOs]

### Summary of Critical Functions

| Rank | Business Function | RTO | RPO | Impact if Unavailable |
|------|-------------------|-----|-----|----------------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

---

## 2. Purpose and Scope

### 2.1 Purpose

This Business Impact Analysis identifies and evaluates the potential effects of disruptions to critical business operations at [ORGANIZATION NAME].

### 2.2 Scope

**In Scope:**
- [Departments/functions included]
- [Locations included]
- [Systems included]

**Out of Scope:**
- [Explicitly excluded items]

### 2.3 Methodology

- Interviews with process owners
- Document review
- Workshop sessions
- Questionnaire responses

---

## 3. Business Function Assessment

### Function: [FUNCTION NAME]

| Field | Details |
|-------|---------|
| **Function ID** | BF-[XXX] |
| **Function Name** | |
| **Department** | |
| **Process Owner** | |
| **Description** | |

#### 3.1 Function Overview

**Purpose:**
[Describe what this function does and why it's important]

**Key Activities:**
1. [Activity 1]
2. [Activity 2]
3. [Activity 3]

**Peak Periods:**
[When is this function most critical - end of month, specific seasons, etc.]

---

#### 3.2 Impact Assessment

**Financial Impact Over Time:**

| Timeframe | Revenue Loss | Additional Costs | Penalties/Fines | Total |
|-----------|--------------|------------------|-----------------|-------|
| 0-4 hours | $[X] | $[X] | $[X] | $[X] |
| 4-24 hours | $[X] | $[X] | $[X] | $[X] |
| 1-3 days | $[X] | $[X] | $[X] | $[X] |
| 3-7 days | $[X] | $[X] | $[X] | $[X] |
| 1-2 weeks | $[X] | $[X] | $[X] | $[X] |
| > 2 weeks | $[X] | $[X] | $[X] | $[X] |

**Operational Impact:**

| Timeframe | Impact Description | Severity (1-5) |
|-----------|-------------------|----------------|
| 0-4 hours | | |
| 4-24 hours | | |
| 1-3 days | | |
| 3-7 days | | |
| 1-2 weeks | | |
| > 2 weeks | | |

**Reputational Impact:**

| Timeframe | Impact Description | Severity (1-5) |
|-----------|-------------------|----------------|
| 0-4 hours | | |
| 4-24 hours | | |
| 1-3 days | | |
| 3-7 days | | |

**Regulatory/Legal Impact:**

| Requirement | Consequence of Non-Compliance | Timeframe |
|-------------|------------------------------|-----------|
| [Regulation/Contract] | [Consequence] | |
| | | |

---

#### 3.3 Dependencies

**Internal Dependencies:**

| Dependent On | Type | Impact if Unavailable |
|--------------|------|----------------------|
| [Department/Function] | Process | |
| [System/Application] | Technology | |
| [Role/Team] | Staff | |

**External Dependencies:**

| Vendor/Partner | Service Provided | Impact if Unavailable |
|----------------|------------------|----------------------|
| | | |
| | | |

**Technology Dependencies:**

| System/Application | Purpose | Criticality |
|-------------------|---------|-------------|
| | | Critical/High/Medium/Low |
| | | |

**Data Dependencies:**

| Data Type | Source | Acceptable Age |
|-----------|--------|----------------|
| | | |
| | | |

---

#### 3.4 Recovery Requirements

**Recovery Time Objective (RTO):**

| Scenario | RTO | Justification |
|----------|-----|---------------|
| Normal Operations | [X] hours/days | [Based on impact analysis] |
| Peak Period | [X] hours/days | [More stringent if needed] |

**Recovery Point Objective (RPO):**

| Data Type | RPO | Justification |
|-----------|-----|---------------|
| [Critical data] | [X] hours | [Max acceptable data loss] |
| [Other data] | [X] hours | |

**Minimum Business Continuity Objective (MBCO):**

[Minimum level of service that must be maintained during a disruption]

---

#### 3.5 Resource Requirements for Recovery

**Minimum Staffing:**

| Role | Number Required | Skills/Access Needed |
|------|-----------------|---------------------|
| | | |
| | | |

**Equipment/Technology:**

| Item | Quantity | Notes |
|------|----------|-------|
| | | |
| | | |

**Workspace:**

| Requirement | Details |
|-------------|---------|
| Workstations | [Number] |
| Phone lines | [Number] |
| Network connectivity | [Requirements] |
| Special equipment | [Details] |

**Vital Records:**

| Record Type | Location | Recovery Priority |
|-------------|----------|-------------------|
| | | High/Medium/Low |
| | | |

---

#### 3.6 Workarounds

**Manual Workarounds:**

| Scenario | Workaround | Duration Sustainable |
|----------|------------|---------------------|
| System unavailable | [Manual process] | [X] hours/days |
| | | |

**Alternative Resources:**

| Resource | Alternative | Notes |
|----------|-------------|-------|
| | | |

---

### Function: [FUNCTION NAME 2]

[Repeat sections 3.1 through 3.6 for each business function]

---

## 4. Criticality Rankings

### 4.1 Criticality Matrix

| Rank | Function | RTO | RPO | Priority |
|------|----------|-----|-----|----------|
| 1 | | | | Critical |
| 2 | | | | Critical |
| 3 | | | | High |
| 4 | | | | High |
| 5 | | | | Medium |
| 6 | | | | Medium |
| 7 | | | | Low |

### 4.2 Recovery Sequence

| Order | Function | Dependencies | RTO |
|-------|----------|--------------|-----|
| 1 | | Must be recovered first | |
| 2 | | Requires [Function 1] | |
| 3 | | Requires [Functions 1, 2] | |

---

## 5. System Criticality

### 5.1 Critical Systems

| System | Supports Functions | RTO | RPO | Backup Location |
|--------|-------------------|-----|-----|-----------------|
| | | | | |
| | | | | |

### 5.2 System Recovery Sequence

| Order | System | Dependencies | RTO |
|-------|--------|--------------|-----|
| 1 | | None | |
| 2 | | [System 1] | |
| 3 | | [Systems 1, 2] | |

---

## 6. Gap Analysis

### 6.1 Identified Gaps

| Gap | Current State | Required State | Risk | Recommendation |
|-----|---------------|----------------|------|----------------|
| [Description] | [Current RTO/capability] | [Required RTO/capability] | H/M/L | [Action] |
| | | | | |

### 6.2 Recommendations

| # | Recommendation | Priority | Estimated Cost | Timeline |
|---|----------------|----------|----------------|----------|
| 1 | | High | | |
| 2 | | Medium | | |
| 3 | | Low | | |

---

## 7. Appendices

### Appendix A: Participants

| Name | Role | Department | Contribution |
|------|------|------------|--------------|
| | | | |

### Appendix B: Assumptions

1. [Assumption 1]
2. [Assumption 2]
3. [Assumption 3]

### Appendix C: Impact Criteria

| Level | Financial Impact | Operational Impact | Reputational Impact |
|-------|------------------|-------------------|---------------------|
| 5 - Critical | > $[X]M | Operations halt | Major media coverage |
| 4 - High | $[X]K - $[X]M | Significant disruption | Regional media |
| 3 - Medium | $[X]K - $[X]K | Moderate impact | Customer complaints |
| 2 - Low | $[X]K - $[X]K | Minor inconvenience | Isolated incidents |
| 1 - Minimal | < $[X]K | Negligible | No external impact |

---

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Prepared By | | | |
| Reviewed By | | | |
| Approved By | | | |

---

## Review History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial version |

---

[Back to Templates](./README.md) | [Back to Home](../README.md)

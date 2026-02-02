# Corrective Action Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., CISO / Quality Manager] |
| **Approved By** | [ROLE - e.g., CEO] |
| **ISO 27001 Reference** | Clause 10.1, 10.2 |

---

## 1. Purpose

This procedure defines the process for identifying, documenting, investigating, and correcting nonconformities within the Information Security Management System (ISMS), and for implementing actions to prevent recurrence.

## 2. Scope

This procedure applies to:
- All nonconformities identified through any source
- All ISMS processes and controls
- All personnel responsible for ISMS activities
- All corrective and preventive actions

## 3. Definitions

| Term | Definition |
|------|------------|
| **Nonconformity** | Non-fulfillment of a requirement (ISO 27001, policy, procedure, or control) |
| **Correction** | Action to eliminate a detected nonconformity |
| **Corrective Action** | Action to eliminate the cause of a nonconformity to prevent recurrence |
| **Root Cause** | The fundamental reason for the occurrence of a nonconformity |

## 4. Sources of Nonconformities

Nonconformities may be identified through:

| Source | Examples |
|--------|----------|
| Internal audits | Audit findings, observations |
| External audits | Certification body findings |
| Security incidents | Incident investigations |
| Management reviews | Review outcomes |
| Performance monitoring | KPI failures, metric deviations |
| Customer feedback | Complaints, concerns |
| Employee reports | Issues raised by staff |
| Risk assessments | Unaddressed risks |
| Control testing | Failed control tests |

## 5. Procedure

### 5.1 Identification and Logging

**Step 1: Identify the Nonconformity**
- Document what requirement was not met
- Note where and when it occurred
- Identify who discovered it

**Step 2: Log the Nonconformity**

Record in the Nonconformity Register:

| Field | Description |
|-------|-------------|
| NCR Number | Unique identifier (e.g., NCR-2024-001) |
| Date Identified | When discovered |
| Source | How it was identified |
| Description | What the nonconformity is |
| Requirement | Which requirement is not met |
| Severity | Critical / Major / Minor |
| Status | Open / In Progress / Closed |

### 5.2 Severity Classification

| Severity | Criteria | Response Time |
|----------|----------|---------------|
| **Critical** | Significant security risk, certification at risk, regulatory breach | Immediate (24-48 hours) |
| **Major** | Significant gap in ISMS, audit major finding | Priority (1-2 weeks) |
| **Minor** | Limited impact, isolated instance, observation | Standard (30 days) |

### 5.3 Immediate Correction

**Step 3: Take Immediate Action**

React to the nonconformity:
- Contain the immediate issue
- Mitigate any current impact
- Document the correction taken

Example corrections:
- Restore a failed control
- Address the immediate security gap
- Implement temporary workaround

### 5.4 Root Cause Analysis

**Step 4: Investigate the Root Cause**

Determine why the nonconformity occurred using appropriate methods:

**5 Whys Method:**
1. Why did X happen? → Because of Y
2. Why did Y happen? → Because of Z
3. Continue until root cause is identified

**Fishbone (Ishikawa) Diagram Categories:**
- People (training, awareness, skills)
- Process (procedures, workflows)
- Technology (systems, tools)
- Management (resources, oversight)
- Environment (external factors)

**Step 5: Document Root Cause**

Record:
- Analysis method used
- Contributing factors identified
- Root cause determination
- Evidence supporting conclusion

### 5.5 Corrective Action Planning

**Step 6: Determine Corrective Action**

Define actions to prevent recurrence:
- Address the root cause, not just symptoms
- Consider effectiveness and feasibility
- Ensure proportionate to severity

**Step 7: Evaluate Consequences**

Consider:
- Will action introduce new risks?
- Are resources available?
- What is the timeline?
- Who needs to be involved?

**Step 8: Document Action Plan**

| Field | Description |
|-------|-------------|
| Action description | What will be done |
| Owner | Who is responsible |
| Due date | When it must be complete |
| Resources needed | Budget, personnel, tools |
| Success criteria | How we know it's effective |

### 5.6 Implementation

**Step 9: Implement Corrective Actions**
- Execute the action plan
- Document progress
- Escalate delays or blockers

**Step 10: Update Documentation**

If corrective action requires changes to:
- Policies → Follow document control procedure
- Procedures → Update and communicate
- Training → Deliver updated training
- Controls → Implement and test

### 5.7 Verification and Closure

**Step 11: Verify Effectiveness**

After implementation:
- Confirm action was completed
- Verify root cause addressed
- Check nonconformity has not recurred
- Test relevant controls

**Step 12: Document Evidence**

Record:
- Verification activities performed
- Evidence of effectiveness
- Date verified
- Person who verified

**Step 13: Close the NCR**

If effective:
- Update status to "Closed"
- Record closure date
- File all documentation

If not effective:
- Reopen and reassess
- Determine additional actions
- Repeat process

## 6. Nonconformity Report (NCR) Form

```
═══════════════════════════════════════════════════════════════
              NONCONFORMITY AND CORRECTIVE ACTION REPORT
═══════════════════════════════════════════════════════════════

NCR Number: ____________    Date Raised: ____________

SECTION 1: NONCONFORMITY DETAILS
─────────────────────────────────────────────────────────────
Source (audit/incident/other): _______________________________
Requirement not met: ________________________________________
Severity:  [ ] Critical   [ ] Major   [ ] Minor

Description of nonconformity:
______________________________________________________________
______________________________________________________________
______________________________________________________________

Raised by: ___________________    Date: ____________

SECTION 2: IMMEDIATE CORRECTION
─────────────────────────────────────────────────────────────
Correction taken:
______________________________________________________________
______________________________________________________________

Completed by: ________________    Date: ____________

SECTION 3: ROOT CAUSE ANALYSIS
─────────────────────────────────────────────────────────────
Analysis method:  [ ] 5 Whys   [ ] Fishbone   [ ] Other: _____

Root cause identified:
______________________________________________________________
______________________________________________________________

Analyzed by: _________________    Date: ____________

SECTION 4: CORRECTIVE ACTION PLAN
─────────────────────────────────────────────────────────────
Action required:
______________________________________________________________
______________________________________________________________

Owner: _______________________    Due date: ____________

SECTION 5: IMPLEMENTATION
─────────────────────────────────────────────────────────────
Action completed:
______________________________________________________________

Completed by: ________________    Date: ____________

SECTION 6: VERIFICATION
─────────────────────────────────────────────────────────────
Verification method:
______________________________________________________________

Result:  [ ] Effective   [ ] Not effective (reopen)

Verified by: _________________    Date: ____________

SECTION 7: CLOSURE
─────────────────────────────────────────────────────────────
Status:  [ ] Closed   [ ] Reopened

Closed by: __________________    Date: ____________

═══════════════════════════════════════════════════════════════
```

## 7. Escalation

| Condition | Escalate To | Timeframe |
|-----------|-------------|-----------|
| Critical NCR | CISO / Management | Immediately |
| Overdue action | Process owner's manager | Upon due date |
| Repeated nonconformity | Management review | Next review |
| Certification risk | Top management | Immediately |

## 8. Monitoring and Reporting

### 8.1 Metrics

Track and report:
- Number of NCRs by source, severity, status
- Average time to close
- Overdue actions
- Effectiveness rate (% verified effective)
- Repeat nonconformities

### 8.2 Reporting

| Report | Frequency | Audience |
|--------|-----------|----------|
| NCR status summary | Monthly | ISMS Manager |
| Detailed NCR report | Quarterly | Management |
| Trend analysis | Annually | Management review |

## 9. Records

Retain the following records:

| Record | Retention Period |
|--------|------------------|
| NCR forms | Minimum 3 years |
| Root cause analysis | Minimum 3 years |
| Evidence of actions | Minimum 3 years |
| Verification records | Minimum 3 years |

## 10. Related Documents

- [Internal Audit Procedure](../../../procedures/internal-audit-procedure.md)
- [Internal Audit Program](./internal-audit-program.md)
- [Management Review Procedure](./management-review-procedure.md)
- [Incident Response Procedure](../../../procedures/incident-response-procedure.md)
- [Document Control Procedure](./document-control-procedure.md)

## 11. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to ISO 27001 Procedures](./README.md) | [Back to ISO 27001](../README.md)

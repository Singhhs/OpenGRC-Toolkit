# Change Management Policy

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Next Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Operations Manager] |
| **Approved By** | [ROLE - e.g., CIO/CISO] |
| **Classification** | Internal |

---

## 1. Purpose

This policy establishes the framework for managing changes to [ORGANIZATION NAME]'s information systems, applications, and infrastructure to minimize risk and ensure stability.

## 2. Scope

This policy applies to changes affecting:
- Production IT systems and infrastructure
- Applications and databases
- Network devices and configurations
- Security controls and settings
- Cloud services and environments
- Operational procedures

**Exclusions:**
- Standard operating procedures (routine maintenance)
- Emergency changes (governed by emergency procedures)
- Development/test environments (unless affecting production)

## 3. Definitions

| Term | Definition |
|------|------------|
| **Change** | Addition, modification, or removal of anything that could affect IT services |
| **RFC** | Request for Change - formal proposal for a change |
| **CAB** | Change Advisory Board - group that assesses and authorizes changes |
| **Standard Change** | Pre-approved, low-risk, routine change |
| **Normal Change** | Change requiring assessment and approval |
| **Emergency Change** | Urgent change to resolve critical incident |

## 4. Policy Statements

### 4.1 Change Management Principles

All changes shall:

1. Be documented and tracked
2. Be assessed for risk and impact
3. Be approved before implementation
4. Be tested where possible
5. Include rollback procedures
6. Be communicated to stakeholders
7. Be reviewed after implementation

### 4.2 Change Categories

| Category | Risk | Approval | Lead Time | Examples |
|----------|------|----------|-----------|----------|
| **Standard** | Low/None | Pre-approved | None | Password resets, routine patches |
| **Minor** | Low | Change Manager | 3 days | Non-critical updates, minor configs |
| **Significant** | Medium | CAB | 5 days | System upgrades, new applications |
| **Major** | High | CAB + Executive | 10 days | Infrastructure changes, migrations |
| **Emergency** | Variable | Emergency CAB | Immediate | Critical incident resolution |

<!-- CUSTOMIZE: Adjust categories and lead times for your organization -->

### 4.3 Change Request Process

```
┌─────────────┐   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐
│   Submit    │──▶│   Assess    │──▶│   Approve   │──▶│  Implement  │──▶│   Review    │
│     RFC     │   │    Risk     │   │   Change    │   │   Change    │   │   Change    │
└─────────────┘   └─────────────┘   └─────────────┘   └─────────────┘   └─────────────┘
```

### 4.4 Request for Change (RFC)

All change requests must include:

| Field | Description |
|-------|-------------|
| Change Title | Clear description of the change |
| Requestor | Person requesting the change |
| Business Justification | Why the change is needed |
| Description | Detailed technical description |
| Systems Affected | All impacted systems/services |
| Risk Assessment | Potential risks and mitigation |
| Impact Assessment | Business and user impact |
| Implementation Plan | Step-by-step procedures |
| Rollback Plan | How to reverse the change |
| Test Plan | How the change will be tested |
| Schedule | Proposed implementation window |
| Resources Required | Personnel, time, costs |
| Communication Plan | Who needs to be notified |

### 4.5 Risk Assessment

#### 4.5.1 Risk Factors

| Factor | Low (1) | Medium (2) | High (3) |
|--------|---------|------------|----------|
| **Scope** | Single system | Multiple systems | Enterprise-wide |
| **Complexity** | Simple, routine | Moderate complexity | Complex, first-time |
| **Reversibility** | Easy rollback | Difficult rollback | Irreversible |
| **Testing** | Fully tested | Partially tested | Cannot test |
| **Experience** | Proven, documented | Some experience | New procedure |
| **Business Impact** | Non-critical | Important | Critical services |

#### 4.5.2 Risk Score

- **Low (6-8)**: Standard approval process
- **Medium (9-12)**: CAB review required
- **High (13-18)**: CAB + Executive approval

### 4.6 Change Advisory Board (CAB)

#### 4.6.1 Composition

- IT Operations Manager (Chair)
- IT Security Representative
- Application/Development Lead
- Infrastructure Lead
- Business Representative(s)
- [Additional roles as needed]

#### 4.6.2 CAB Meetings

- Regular CAB: [Weekly - specify day/time]
- Emergency CAB: Convened as needed
- Quorum: Minimum [3] members including Chair

#### 4.6.3 CAB Responsibilities

- Review and assess change requests
- Approve, reject, or defer changes
- Prioritize and schedule changes
- Resolve conflicts between changes
- Review failed changes

### 4.7 Implementation

#### 4.7.1 Implementation Requirements

Before implementation:
- [ ] All approvals obtained
- [ ] Implementation plan reviewed
- [ ] Rollback plan documented
- [ ] Backups completed
- [ ] Stakeholders notified
- [ ] Resources available

#### 4.7.2 Change Windows

| Window Type | Timing | Restrictions |
|-------------|--------|--------------|
| Standard | [Specify - e.g., Tues/Thurs 22:00-02:00] | Non-critical changes |
| Extended | [Specify - e.g., Weekends] | Major changes |
| Emergency | Any time | Critical fixes only |
| Blackout | [Specify periods] | No changes permitted |

<!-- CUSTOMIZE: Define your change windows -->

#### 4.7.3 Implementation Steps

1. Confirm change window and resources
2. Notify affected parties
3. Complete pre-change backup
4. Execute implementation plan
5. Verify change success
6. Document results
7. Close change record

### 4.8 Post-Implementation Review

All changes shall be reviewed to verify:
- Change implemented as planned
- Expected outcomes achieved
- No unexpected impacts
- Documentation updated
- Lessons learned captured

Failed changes require:
- Root cause analysis
- Corrective actions
- Process improvements

### 4.9 Emergency Changes

#### 4.9.1 Emergency Criteria

Emergency changes are only for:
- Resolution of critical incidents
- Urgent security vulnerabilities
- Regulatory compliance deadlines
- Imminent service failure

#### 4.9.2 Emergency Process

1. Verbal approval from [On-call Manager/CISO]
2. Implement change
3. Document RFC within 24 hours
4. Review at next CAB meeting

### 4.10 Standard Changes

Pre-approved changes with:
- Documented procedures
- Known and accepted risk
- Clear success criteria
- No further approval needed

Examples:
- Password resets
- Standard software installation
- Routine patches (tested)
- User provisioning
- Scheduled maintenance

## 5. Roles and Responsibilities

### 5.1 Change Requestor
- Submit complete RFC
- Provide accurate information
- Participate in implementation
- Verify change success

### 5.2 Change Manager
- Manage change process
- Coordinate CAB meetings
- Track and report on changes
- Ensure policy compliance

### 5.3 CAB Members
- Assess and approve changes
- Attend CAB meetings
- Represent their areas

### 5.4 Implementer
- Follow approved implementation plan
- Execute rollback if needed
- Document implementation
- Report issues

## 6. Documentation and Records

All changes must be recorded in [Change Management System/Tool].

Records retained for [3 years / as per retention policy].

## 7. Metrics and Reporting

| Metric | Target |
|--------|--------|
| Change success rate | > 95% |
| Emergency change rate | < 10% |
| Changes implemented on schedule | > 90% |
| Post-implementation issues | < 5% |

## 8. Compliance

Violations may result in:
- Change reversal
- Disciplinary action
- Access restrictions

## 9. Related Documents

- [Change Management Procedure](../procedures/change-management-procedure.md)
- [Incident Response Policy](./incident-response-policy.md)
- [Patch Management Procedure](../procedures/patch-management-procedure.md)

## 10. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Policies](./README.md) | [Back to Home](../README.md)

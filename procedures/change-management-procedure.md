# Change Management Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Operations Manager] |
| **Classification** | Internal |

---

## 1. Purpose

This procedure provides step-by-step guidance for requesting, assessing, approving, and implementing changes to [ORGANIZATION NAME]'s IT systems and infrastructure.

## 2. Scope

Applies to all changes affecting:
- Production systems and applications
- Network infrastructure
- Security configurations
- Databases
- Cloud environments

## 3. Change Categories

| Category | Risk | Approval | Lead Time | Examples |
|----------|------|----------|-----------|----------|
| **Standard** | Pre-approved | None needed | None | Password resets, routine patches |
| **Minor** | Low | Change Manager | 3 business days | Config changes, minor updates |
| **Significant** | Medium | CAB | 5 business days | System upgrades, new apps |
| **Major** | High | CAB + Executive | 10 business days | Infrastructure changes |
| **Emergency** | Variable | Emergency CAB | Immediate | Critical fixes |

## 4. Procedure

### Step 1: Submit Change Request

**Responsibility:** Change Requestor

**Timeline:** Before lead time requirement

1. [ ] Log into [Change Management System]
2. [ ] Create new Request for Change (RFC)
3. [ ] Complete all required fields:

| Field | Description | Required |
|-------|-------------|----------|
| Change Title | Clear, descriptive name | Yes |
| Description | Detailed technical description | Yes |
| Business Justification | Why change is needed | Yes |
| Systems Affected | All impacted systems | Yes |
| Risk Assessment | Potential risks | Yes |
| Implementation Plan | Step-by-step procedure | Yes |
| Rollback Plan | How to reverse change | Yes |
| Test Plan | Validation steps | Yes |
| Proposed Schedule | Date/time for implementation | Yes |
| Outage Required | Yes/No, duration | Yes |
| Resources Needed | Personnel, tools | Yes |

4. [ ] Attach supporting documentation
5. [ ] Submit RFC for review

---

### Step 2: Initial Review

**Responsibility:** Change Manager

**Timeline:** Within 1 business day

1. [ ] Review RFC for completeness
2. [ ] Verify all required fields populated
3. [ ] Confirm appropriate category assigned
4. [ ] Check for scheduling conflicts
5. [ ] If incomplete:
   - [ ] Return to requestor with comments
   - [ ] Request additional information
6. [ ] If complete:
   - [ ] Assign RFC number
   - [ ] Route for appropriate approval

---

### Step 3: Technical Assessment

**Responsibility:** Technical Reviewers (as assigned)

**Timeline:** Within 2 business days

1. [ ] Review technical details
2. [ ] Assess:
   - [ ] Technical feasibility
   - [ ] Resource requirements
   - [ ] Dependencies on other systems
   - [ ] Impact on other changes
   - [ ] Security implications
3. [ ] Validate implementation plan
4. [ ] Validate rollback plan
5. [ ] Provide assessment and recommendation
6. [ ] Flag any concerns for CAB

---

### Step 4: Risk Assessment

**Responsibility:** Change Manager / IT Security

**Timeline:** Part of technical assessment

Score each factor 1-3:

| Factor | 1 (Low) | 2 (Medium) | 3 (High) |
|--------|---------|------------|----------|
| Scope | Single system | Multiple systems | Enterprise |
| Complexity | Simple/routine | Moderate | Complex/new |
| Reversibility | Easy rollback | Difficult | Irreversible |
| Testing | Fully tested | Partial | Cannot test |
| Business Impact | Non-critical | Important | Critical |

**Total Score:**
- 5-7: Low Risk → Minor change process
- 8-11: Medium Risk → CAB review
- 12-15: High Risk → CAB + Executive approval

---

### Step 5: CAB Review (if required)

**Responsibility:** Change Advisory Board

**Timeline:** Weekly CAB meeting or emergency CAB

**CAB Members:**
- Change Manager (Chair)
- IT Operations Representative
- IT Security Representative
- Application/Development Lead
- Business Representative

**Agenda:**
1. [ ] Review pending RFCs
2. [ ] Discuss risk assessments
3. [ ] Review implementation schedules
4. [ ] Identify conflicts
5. [ ] Vote on approval/rejection
6. [ ] Document decisions

**Decisions:**
- **Approved** - Proceed as planned
- **Approved with conditions** - Proceed with modifications
- **Deferred** - Postpone to future date
- **Rejected** - Do not proceed (with reason)

---

### Step 6: Schedule Change

**Responsibility:** Change Manager

**Timeline:** After approval

1. [ ] Confirm implementation window
2. [ ] Check for conflicts with:
   - [ ] Other approved changes
   - [ ] Business blackout periods
   - [ ] Resource availability
   - [ ] Maintenance windows
3. [ ] Reserve change window
4. [ ] Update change calendar
5. [ ] Notify stakeholders

**Standard Change Windows:**
- [Day/Time]: [e.g., Tuesday/Thursday 22:00-02:00]
- Extended: [e.g., Weekends]
- Blackout periods: [e.g., End of quarter, holidays]

---

### Step 7: Pre-Implementation

**Responsibility:** Implementation Team

**Timeline:** Before change window

**24-48 Hours Before:**
- [ ] Final review of implementation plan
- [ ] Confirm all approvals in place
- [ ] Verify resources available
- [ ] Confirm rollback plan ready
- [ ] Complete pre-change backup
- [ ] Notify affected users/teams

**Day of Change:**
- [ ] Confirm team assembled
- [ ] Verify access to all systems
- [ ] Confirm communication channels
- [ ] Final go/no-go decision

---

### Step 8: Implementation

**Responsibility:** Implementation Team

**Timeline:** During change window

1. [ ] Begin implementation log
2. [ ] Execute implementation plan step-by-step
3. [ ] Document each action with timestamp
4. [ ] At each checkpoint:
   - [ ] Verify step completed successfully
   - [ ] Check for unexpected issues
   - [ ] Decide continue or rollback

**Implementation Log Format:**
```
[TIME] - [PERSON] - [ACTION] - [RESULT]
```

**If Issues Occur:**
- Minor: Document and continue if safe
- Major: Assess rollback decision
- Critical: Initiate rollback immediately

---

### Step 9: Rollback (if needed)

**Responsibility:** Implementation Team Lead

**Timeline:** When rollback criteria met

**Rollback Triggers:**
- Critical functionality broken
- Cannot complete within window
- Unexpected security issue
- Data integrity concerns
- Stakeholder request

**Rollback Steps:**
1. [ ] Announce rollback decision
2. [ ] Execute rollback plan
3. [ ] Verify systems restored
4. [ ] Document rollback reason
5. [ ] Notify stakeholders
6. [ ] Schedule post-mortem

---

### Step 10: Verification

**Responsibility:** Implementation Team + Requestor

**Timeline:** Immediately after implementation

1. [ ] Execute test plan
2. [ ] Verify change objectives met
3. [ ] Check system functionality
4. [ ] Verify no unexpected impacts
5. [ ] Confirm with business users
6. [ ] Document verification results

**Verification Checklist:**
- [ ] Primary function working
- [ ] Dependent systems working
- [ ] Performance acceptable
- [ ] Security controls intact
- [ ] Monitoring active
- [ ] No error alerts

---

### Step 11: Post-Implementation

**Responsibility:** Change Manager / Implementation Team

**Timeline:** Within 1-2 business days

1. [ ] Update system documentation
2. [ ] Update configuration records
3. [ ] Close change ticket with results
4. [ ] Conduct post-implementation review (PIR) for significant changes
5. [ ] Document lessons learned
6. [ ] Archive change documentation

**Post-Implementation Review:**
- Was change successful?
- Were there unexpected issues?
- Was the plan adequate?
- What could be improved?

---

## 5. Emergency Change Process

### When to Use
- Critical production issue
- Active security incident
- Regulatory compliance deadline
- Imminent service failure

### Emergency Process

1. [ ] Contact on-call Change Manager
2. [ ] Obtain verbal approval from:
   - [ ] Change Manager
   - [ ] IT Director/CISO (for security changes)
3. [ ] Document approval via email/chat
4. [ ] Implement change
5. [ ] Submit formal RFC within 24 hours
6. [ ] Review at next CAB meeting

### Emergency Contacts

| Role | Name | Phone |
|------|------|-------|
| Change Manager (On-Call) | [NAME] | [PHONE] |
| IT Director | [NAME] | [PHONE] |
| CISO | [NAME] | [PHONE] |

---

## 6. Standard Changes

Pre-approved changes that follow documented procedures:

| Standard Change | Procedure | Conditions |
|-----------------|-----------|------------|
| Password reset | [Link] | Valid request |
| User account creation | [Link] | Approved request |
| Approved software installation | [Link] | From approved list |
| Scheduled patch deployment | [Link] | Tested patches |
| Backup restoration (non-prod) | [Link] | Authorized request |

---

## 7. Metrics

| Metric | Target |
|--------|--------|
| Change success rate | > 95% |
| Emergency change rate | < 10% |
| Changes on schedule | > 90% |
| Average approval time | < 3 days |
| Post-implementation issues | < 5% |

---

## 8. Related Documents

- [Change Management Policy](../policies/change-management-policy.md)
- [Incident Response Procedure](./incident-response-procedure.md)
- [Patch Management Procedure](./patch-management-procedure.md)

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

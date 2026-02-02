# Disaster Recovery Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Director / DR Manager] |
| **Approved By** | [ROLE - e.g., CIO] |
| **Related Policy** | [Business Continuity Policy](../policies/business-continuity-policy.md) |

---

## 1. Purpose

This procedure defines the process for recovering IT systems, applications, and data following a disaster or major disruption at [ORGANIZATION NAME].

## 2. Scope

This procedure applies to:
- All critical IT systems and applications
- Data centers and infrastructure
- Cloud services and platforms
- Network and communications
- All personnel involved in disaster recovery

## 3. Definitions

| Term | Definition |
|------|------------|
| **Disaster** | Event causing significant disruption to normal operations |
| **RTO** | Recovery Time Objective - maximum acceptable downtime |
| **RPO** | Recovery Point Objective - maximum acceptable data loss |
| **DR Site** | Alternate location for recovery operations |
| **Failover** | Switch from primary to backup systems |
| **Failback** | Return from backup to primary systems |

## 4. Recovery Objectives

### 4.1 System Classifications

| Tier | RTO | RPO | Examples |
|------|-----|-----|----------|
| **Tier 1 - Critical** | 4 hours | 1 hour | [Core business systems, email, ERP] |
| **Tier 2 - Essential** | 24 hours | 4 hours | [Secondary applications, file shares] |
| **Tier 3 - Important** | 72 hours | 24 hours | [Development, non-critical apps] |
| **Tier 4 - Non-Critical** | 1 week+ | 24 hours | [Archive, training systems] |

### 4.2 Critical Systems Inventory

| System | Tier | RTO | RPO | Recovery Method | Owner |
|--------|------|-----|-----|-----------------|-------|
| [System 1] | 1 | 4h | 1h | [Hot standby] | [Owner] |
| [System 2] | 1 | 4h | 1h | [Cloud failover] | [Owner] |
| [System 3] | 2 | 24h | 4h | [Backup restore] | [Owner] |
| [Add systems] | | | | | |

## 5. DR Infrastructure

### 5.1 Recovery Sites

| Site | Type | Location | Capacity | Activation Time |
|------|------|----------|----------|-----------------|
| Primary | Production | [Location] | 100% | N/A |
| DR Site | [Hot/Warm/Cold] | [Location] | [%] | [Time] |
| Cloud DR | [Provider] | [Region] | [%] | [Time] |

### 5.2 Recovery Resources

- Backup systems and storage
- Network connectivity
- Backup power
- Communication systems
- Recovery documentation
- Recovery tools and media

## 6. Disaster Recovery Procedure

### Phase 1: Detection and Assessment

**Step 1: Detect Incident**
- Monitoring alerts
- User reports
- Facility notifications
- Vendor communications

**Step 2: Initial Assessment**

Determine:
- Nature of incident (what happened)
- Scope of impact (what's affected)
- Current status (systems up/down)
- Estimated duration
- Safety concerns

**Step 3: Classify Severity**

| Level | Description | Response |
|-------|-------------|----------|
| **Level 1** | Complete site loss | Full DR activation |
| **Level 2** | Major system failure | Partial DR activation |
| **Level 3** | Significant disruption | Enhanced response |
| **Level 4** | Limited impact | Standard incident response |

**Step 4: Activate DR Team**

Notification chain:
1. IT Director / DR Manager
2. CISO / IT Security
3. Business Continuity Manager
4. Executive Management
5. DR Team members
6. Key stakeholders

### Phase 2: DR Activation Decision

**Step 5: Convene DR Team**

Emergency meeting (in person or virtual):
- Review incident details
- Assess recovery options
- Estimate recovery time at primary
- Determine if DR activation needed

**Step 6: Make Go/No-Go Decision**

| Criteria | Threshold for DR Activation |
|----------|----------------------------|
| Estimated primary restoration | > RTO for Tier 1 systems |
| Data integrity compromised | Unable to verify data integrity |
| Facility access | Primary site inaccessible |
| Safety concerns | Personnel safety at risk |

**Decision Authority:**
- Level 1/2: CIO or designated alternate
- Level 3/4: IT Director

**Step 7: Document Decision**

Record:
- Decision made (activate/not activate)
- Rationale
- Time of decision
- Approver
- Systems to be recovered

### Phase 3: DR Site Activation

**Step 8: Notify Stakeholders**

| Audience | Communication Method | Responsible |
|----------|---------------------|-------------|
| Executive team | Direct call/message | DR Manager |
| Department heads | Emergency notification | BC Manager |
| All employees | Mass notification system | HR/Communications |
| Customers | [Per communication plan] | Communications |
| Vendors | Direct contact | Procurement/IT |
| Regulators | [As required] | Legal/Compliance |

**Step 9: Activate DR Site**

- [ ] Contact DR site / cloud provider
- [ ] Confirm site availability and access
- [ ] Activate network connectivity
- [ ] Verify power and environmental systems
- [ ] Establish communications
- [ ] Prepare recovery environment

**Step 10: Mobilize Recovery Team**

- [ ] Assign team to DR site (if physical)
- [ ] Establish remote access (if applicable)
- [ ] Distribute recovery runbooks
- [ ] Confirm team communications
- [ ] Set up command center

### Phase 4: System Recovery

**Step 11: Execute Recovery Sequence**

Recover in priority order:

**Tier 1 Systems (First - within 4 hours)**
```
1. Core infrastructure (AD, DNS, network)
2. Database servers
3. Critical applications
4. Email and communications
```

**Tier 2 Systems (Second - within 24 hours)**
```
5. Secondary applications
6. File services
7. Supporting systems
```

**Tier 3/4 Systems (Third - within 72 hours+)**
```
8. Development systems
9. Non-critical applications
10. Archive and historical systems
```

**Step 12: Restore Data**

For each system:
1. Identify most recent valid backup
2. Verify backup integrity
3. Restore data to recovery environment
4. Validate data completeness
5. Document any data loss (vs RPO)

**Step 13: Validate Recovery**

| Validation Type | Description | Performed By |
|-----------------|-------------|--------------|
| System health | Servers running, services started | IT Operations |
| Application function | Core functions working | Application owners |
| Data integrity | Data accurate and complete | Business users |
| Integration | Systems communicating | IT Operations |
| Security | Controls in place | IT Security |

**Step 14: User Access**

- [ ] Verify user accounts functional
- [ ] Confirm authentication working
- [ ] Test VPN/remote access
- [ ] Validate permissions
- [ ] Communicate access instructions

### Phase 5: Operations at DR Site

**Step 15: Transition to DR Operations**

- [ ] Confirm all critical systems operational
- [ ] Business validation complete
- [ ] Declare DR environment "live"
- [ ] Update DNS/routing as needed
- [ ] Enable user access
- [ ] Begin DR site operations

**Step 16: Ongoing DR Operations**

- Monitor system performance
- Address issues as they arise
- Maintain communication with stakeholders
- Document all activities
- Plan for failback

### Phase 6: Failback to Primary

**Step 17: Assess Primary Site**

Before failback:
- [ ] Primary site accessible and safe
- [ ] Infrastructure restored
- [ ] Root cause addressed
- [ ] Systems rebuilt/repaired
- [ ] Network connectivity restored

**Step 18: Plan Failback**

- Schedule failback window
- Identify data synchronization needs
- Plan cutover sequence
- Prepare rollback plan
- Notify stakeholders

**Step 19: Execute Failback**

1. Final data sync from DR to primary
2. Validate data integrity
3. Stop DR site operations
4. Redirect traffic to primary
5. Verify primary operations
6. Test all systems
7. Confirm with business

**Step 20: Deactivate DR Site**

- [ ] Confirm all operations on primary
- [ ] Remove DR site from production
- [ ] Reset DR environment
- [ ] Restore backup configurations
- [ ] Document lessons learned

### Phase 7: Post-Recovery

**Step 21: Post-Incident Review**

Conduct review within 2 weeks:
- Timeline of events
- What worked well
- What could improve
- Gaps identified
- Action items

**Step 22: Update Documentation**

- [ ] Update DR procedures based on lessons
- [ ] Revise system recovery runbooks
- [ ] Update contact lists
- [ ] Refresh backup strategies
- [ ] Schedule additional testing

## 7. Recovery Runbooks

Detailed runbooks should exist for each critical system:

### Runbook Template

```
═══════════════════════════════════════════════════════════════
                    SYSTEM RECOVERY RUNBOOK
═══════════════════════════════════════════════════════════════

System Name: _________________
Tier: ____  RTO: ____  RPO: ____

DEPENDENCIES
─────────────────────────────────────────────────────────────
Prerequisites (must be recovered first):
1. _______________
2. _______________

RECOVERY STEPS
─────────────────────────────────────────────────────────────
Step 1: _______________
        Command/Action: _______________
        Expected Result: _______________
        Verification: _______________

Step 2: _______________
        [Continue for all steps]

VALIDATION CHECKLIST
─────────────────────────────────────────────────────────────
[ ] Service started
[ ] Database connected
[ ] Application responding
[ ] Users can log in
[ ] Core functions working
[ ] Integrations functional

TROUBLESHOOTING
─────────────────────────────────────────────────────────────
Common Issue 1: _______________
Resolution: _______________

CONTACTS
─────────────────────────────────────────────────────────────
System Owner: _______________
Technical Lead: _______________
Vendor Support: _______________

═══════════════════════════════════════════════════════════════
```

## 8. Communication Plan

### 8.1 Internal Communications

| Milestone | Audience | Message | Channel |
|-----------|----------|---------|---------|
| DR Activated | All staff | Incident notification, expected impact | Mass notification |
| Systems Recovering | Department heads | Recovery progress, timeline | Email/Call |
| Systems Available | Users | Access instructions | Email |
| Normal Operations | All staff | Incident resolved | Email |

### 8.2 External Communications

| Audience | When to Notify | Responsible |
|----------|----------------|-------------|
| Customers | If service impacted | Communications |
| Vendors | If support needed | IT/Procurement |
| Regulators | Per requirements | Legal/Compliance |
| Media | Only if necessary | Communications |

## 9. Testing Requirements

| Test Type | Frequency | Scope |
|-----------|-----------|-------|
| Tabletop exercise | Quarterly | DR team walkthrough |
| Component test | Monthly | Individual system recovery |
| Partial DR test | Semi-annually | Tier 1 systems |
| Full DR test | Annually | Complete DR activation |

## 10. Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| **DR Manager** | Overall DR coordination, decision authority |
| **IT Operations** | System recovery execution |
| **IT Security** | Security validation, access control |
| **Database Admin** | Database recovery, data validation |
| **Network Admin** | Network recovery, connectivity |
| **Application Owners** | Application validation, user support |
| **Communications** | Stakeholder communications |

## 11. Contact List

| Role | Name | Phone | Email | Alternate |
|------|------|-------|-------|-----------|
| DR Manager | [Name] | [Phone] | [Email] | [Backup] |
| IT Director | [Name] | [Phone] | [Email] | [Backup] |
| [Add all DR team members] | | | | |

## 12. Related Documents

- [Business Continuity Policy](../policies/business-continuity-policy.md)
- [Backup Policy](../policies/backup-policy.md)
- [Backup Procedure](./backup-procedure.md)
- [Incident Response Policy](../policies/incident-response-policy.md)
- [Business Impact Analysis](../templates/business-impact-analysis.md)

## 13. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

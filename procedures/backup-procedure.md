# Data Backup and Recovery Procedure

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Effective Date** | [DATE] |
| **Last Review** | [DATE] |
| **Owner** | [ROLE - e.g., IT Operations Manager] |
| **Classification** | Internal |

---

## 1. Purpose

This procedure provides step-by-step guidance for performing data backups and restoring data at [ORGANIZATION NAME].

## 2. Scope

Applies to:
- Production servers and databases
- File servers and shares
- Email systems
- Business applications
- Configuration data
- Cloud environments

## 3. Backup Schedule

### 3.1 Standard Backup Schedule

| System Type | Full Backup | Incremental | Retention |
|-------------|-------------|-------------|-----------|
| Production Databases | Weekly (Sunday) | Daily | 90 days |
| File Servers | Weekly (Saturday) | Daily | 90 days |
| Email Systems | Weekly (Sunday) | Daily | 1 year |
| Application Servers | Weekly | Daily | 60 days |
| Domain Controllers | Weekly | Daily | 60 days |
| Network Configs | Weekly | After changes | 1 year |
| Virtual Machines | Weekly | Daily | 60 days |

### 3.2 Backup Windows

| Backup Type | Start Time | Max Duration |
|-------------|------------|--------------|
| Full Backups | 22:00 Saturday/Sunday | 8 hours |
| Incremental | 01:00 Daily | 4 hours |
| Transaction Logs | Every 15 minutes | N/A |

---

## 4. Backup Procedure

### Step 1: Pre-Backup Checks

**Responsibility:** Backup Administrator

**Timeline:** Before scheduled backup

1. [ ] Verify backup media/storage available
2. [ ] Check backup system health
3. [ ] Verify network connectivity
4. [ ] Confirm backup agents running
5. [ ] Review previous backup status
6. [ ] Address any outstanding issues

---

### Step 2: Execute Backup

**Responsibility:** Automated / Backup Administrator

**For Automated Backups:**
1. [ ] Backup job starts per schedule
2. [ ] System quiesces applications (if required)
3. [ ] Data copied to backup location
4. [ ] Backup verified
5. [ ] Job completion logged

**For Manual Backups:**
1. [ ] Log into backup system
2. [ ] Select systems/data to backup
3. [ ] Choose backup type (full/incremental)
4. [ ] Select destination
5. [ ] Initiate backup
6. [ ] Monitor progress
7. [ ] Verify completion

---

### Step 3: Verify Backup

**Responsibility:** Backup Administrator

**Timeline:** Within 4 hours of completion

1. [ ] Check backup job status
2. [ ] Verify completion without errors
3. [ ] Confirm data size reasonable
4. [ ] Spot-check file integrity
5. [ ] Update backup log

**Backup Log Entry:**
```
Date: [DATE]
System: [SYSTEM NAME]
Type: Full / Incremental
Start: [TIME]
End: [TIME]
Size: [SIZE]
Status: Success / Failed / Partial
Errors: [ANY ERRORS]
Verified By: [NAME]
```

---

### Step 4: Offsite Replication

**Responsibility:** Automated / Backup Administrator

**Timeline:** Within 24 hours of backup

1. [ ] Verify replication job scheduled
2. [ ] Monitor replication progress
3. [ ] Confirm successful transfer
4. [ ] Verify offsite copy integrity
5. [ ] Document replication status

**Offsite Locations:**
- Primary: [LOCATION/SERVICE]
- Secondary: [LOCATION/SERVICE]

---

### Step 5: Media Management (if applicable)

**Responsibility:** Backup Administrator

**For Tape/Physical Media:**
1. [ ] Label media clearly
2. [ ] Update media inventory
3. [ ] Store onsite copy securely
4. [ ] Prepare offsite rotation
5. [ ] Track media lifecycle

**Media Labeling Format:**
```
[SYSTEM]-[DATE]-[TYPE]-[SEQUENCE]
Example: FILESRV-20240115-FULL-001
```

---

## 5. Backup Monitoring

### Daily Checks

| Check | Action |
|-------|--------|
| All jobs completed | Review backup console |
| No failures | Investigate and resolve |
| Storage capacity | Verify sufficient space |
| Replication status | Confirm offsite sync |

### Weekly Checks

| Check | Action |
|-------|--------|
| Full backup success | Verify all systems |
| Storage trends | Plan capacity |
| Failed job analysis | Root cause review |
| Documentation update | Update any changes |

### Monthly Checks

| Check | Action |
|-------|--------|
| Recovery test | Test restore capability |
| Policy compliance | Verify all systems covered |
| Retention cleanup | Remove expired backups |
| Report to management | Status summary |

---

## 6. Data Recovery Procedure

### Step 1: Receive Recovery Request

**Responsibility:** IT Service Desk / Backup Administrator

1. [ ] Receive and log request
2. [ ] Gather information:
   - Requestor name and contact
   - What data needs restoration
   - Original location of data
   - Date/time data was valid
   - Reason for restoration
   - Target location for restore
   - Priority/urgency

**Recovery Request Form:**
| Field | Information |
|-------|-------------|
| Ticket # | |
| Requestor | |
| Data Description | |
| Original Path | |
| Point-in-Time Needed | |
| Restore Location | |
| Priority | Critical / High / Standard |
| Approved By | |

---

### Step 2: Validate Request

**Responsibility:** Backup Administrator

**Timeline:** Within 2 hours (critical) / 1 business day (standard)

1. [ ] Verify requestor authorization
2. [ ] Confirm manager approval (if required)
3. [ ] Identify backup containing data
4. [ ] Verify backup integrity
5. [ ] Confirm restore location
6. [ ] Estimate restoration time

---

### Step 3: Prepare for Restoration

**Responsibility:** Backup Administrator

1. [ ] Notify requestor of timeline
2. [ ] Prepare restore location
3. [ ] Verify sufficient space
4. [ ] Coordinate with system owners if needed
5. [ ] Schedule restoration window

---

### Step 4: Execute Restoration

**Responsibility:** Backup Administrator

**For File-Level Restore:**
1. [ ] Mount backup or access catalog
2. [ ] Locate requested files/folders
3. [ ] Select restore destination
4. [ ] Choose overwrite options:
   - [ ] Restore to alternate location (recommended)
   - [ ] Overwrite existing (with approval)
5. [ ] Initiate restore
6. [ ] Monitor progress

**For System/Application Restore:**
1. [ ] Coordinate with application team
2. [ ] Plan restoration sequence
3. [ ] Stop dependent services
4. [ ] Restore system/database
5. [ ] Verify application consistency
6. [ ] Restart services
7. [ ] Test functionality

**For Bare Metal Recovery:**
1. [ ] Boot from recovery media
2. [ ] Connect to backup system
3. [ ] Select system image
4. [ ] Restore to hardware
5. [ ] Verify boot and operation
6. [ ] Rejoin domain/network
7. [ ] Apply any missing updates

---

### Step 5: Verify Restoration

**Responsibility:** Backup Administrator + Requestor

1. [ ] Confirm files restored
2. [ ] Verify file integrity
3. [ ] Check file permissions
4. [ ] Requestor validates data
5. [ ] Test functionality (for applications)

---

### Step 6: Complete and Document

**Responsibility:** Backup Administrator

1. [ ] Document restoration:
   - What was restored
   - Source backup used
   - Destination location
   - Time taken
   - Any issues encountered
2. [ ] Update recovery log
3. [ ] Notify requestor of completion
4. [ ] Close ticket

---

## 7. Recovery Testing

### Monthly Recovery Test

**Objective:** Verify backup integrity and restore capability

1. [ ] Select random file/folder
2. [ ] Restore to test location
3. [ ] Verify integrity
4. [ ] Document results
5. [ ] Delete test restore

### Quarterly Application Recovery Test

**Objective:** Verify application can be recovered

1. [ ] Select test application/database
2. [ ] Restore to test environment
3. [ ] Verify functionality
4. [ ] Document recovery time
5. [ ] Clean up test environment

### Annual Disaster Recovery Test

**Objective:** Verify full system recovery capability

1. [ ] Define test scope
2. [ ] Execute DR plan
3. [ ] Restore critical systems
4. [ ] Verify operations
5. [ ] Document RTO achieved
6. [ ] Identify improvements

---

## 8. Backup Failure Handling

### When Backup Fails

1. [ ] Document failure details
2. [ ] Identify root cause:
   - Network issues
   - Storage capacity
   - Agent problems
   - Application conflicts
3. [ ] Resolve issue
4. [ ] Re-run backup
5. [ ] Verify success
6. [ ] Escalate if unresolved

### Escalation

| Failure Duration | Escalation |
|------------------|------------|
| Single failure | Backup Admin resolves |
| 2 consecutive | IT Operations Manager |
| 3+ or critical system | IT Director |

---

## 9. Contacts

| Role | Name | Phone | Email |
|------|------|-------|-------|
| Backup Administrator | [NAME] | [PHONE] | [EMAIL] |
| IT Operations Manager | [NAME] | [PHONE] | [EMAIL] |
| Backup Vendor Support | [VENDOR] | [PHONE] | [CASE #] |

---

## 10. Related Documents

- [Backup Policy](../policies/backup-policy.md)
- [Business Continuity Policy](../policies/business-continuity-policy.md)
- [Disaster Recovery Procedure](./disaster-recovery-procedure.md)

---

[Back to Procedures](./README.md) | [Back to Home](../README.md)

# Lessons Learned / Post-Incident Review Template

Use this template to conduct and document post-incident reviews (also known as post-mortems, retrospectives, or after-action reviews).

---

## Post-Incident Review Report

### Document Information

| Field | Details |
|-------|---------|
| **Incident ID** | [INC-YYYY-XXXX] |
| **Incident Name** | [Descriptive name] |
| **Review Date** | [DATE] |
| **Review Facilitator** | [NAME] |
| **Report Author** | [NAME] |
| **Classification** | [CONFIDENTIAL / INTERNAL] |

---

## 1. Executive Summary

### Incident Overview

**What happened:** [2-3 sentence summary]

**When:** [Date/time range]

**Impact:** [Brief description of business impact]

**Resolution:** [How it was resolved]

### Key Metrics

| Metric | Value |
|--------|-------|
| Time to Detect (TTD) | [Hours/Minutes] |
| Time to Respond (TTR) | [Hours/Minutes] |
| Time to Contain (TTC) | [Hours/Minutes] |
| Time to Resolve (MTTR) | [Hours/Minutes] |
| Total Downtime | [Hours/Minutes] |
| Systems Affected | [Number] |
| Users Affected | [Number] |
| Data Records Affected | [Number or N/A] |
| Estimated Cost | [$XXX,XXX] |

### Top 3 Takeaways

1. [Most important lesson learned]
2. [Second most important lesson learned]
3. [Third most important lesson learned]

---

## 2. Incident Timeline

### Chronological Events

| Date/Time | Event | Actor |
|-----------|-------|-------|
| [TIMESTAMP] | [First indicator / attack begins] | [Attacker/System] |
| [TIMESTAMP] | [Alert generated / Detection] | [System/Person] |
| [TIMESTAMP] | [Investigation begins] | [Team/Person] |
| [TIMESTAMP] | [Incident confirmed] | [Team/Person] |
| [TIMESTAMP] | [Escalation] | [Team/Person] |
| [TIMESTAMP] | [Containment action] | [Team/Person] |
| [TIMESTAMP] | [Additional containment] | [Team/Person] |
| [TIMESTAMP] | [Threat eradicated] | [Team/Person] |
| [TIMESTAMP] | [Recovery begins] | [Team/Person] |
| [TIMESTAMP] | [Normal operations restored] | [Team/Person] |
| [TIMESTAMP] | [Incident closed] | [Team/Person] |

### Timeline Visualization

```
[DETECTION]----[RESPONSE]----[CONTAINMENT]----[ERADICATION]----[RECOVERY]----[CLOSED]
    |              |              |                |               |            |
  Day 1         Day 1          Day 1            Day 2           Day 3        Day 4
 10:00am       10:30am        11:45am          9:00am          2:00pm       5:00pm
```

---

## 3. Incident Analysis

### Root Cause Analysis

**Primary Root Cause:**
[Description of the fundamental cause that allowed this incident to occur]

**Contributing Factors:**
1. [Factor 1]
2. [Factor 2]
3. [Factor 3]

**5 Whys Analysis:**

| Why | Answer |
|-----|--------|
| Why did [incident] happen? | [Answer 1] |
| Why did [Answer 1] happen? | [Answer 2] |
| Why did [Answer 2] happen? | [Answer 3] |
| Why did [Answer 3] happen? | [Answer 4] |
| Why did [Answer 4] happen? | [Root Cause] |

### Attack Chain / Kill Chain Analysis (If Applicable)

| Phase | What Happened | Detection | Prevention |
|-------|---------------|-----------|------------|
| Reconnaissance | [Description] | [How/If detected] | [How could prevent] |
| Weaponization | [Description] | [How/If detected] | [How could prevent] |
| Delivery | [Description] | [How/If detected] | [How could prevent] |
| Exploitation | [Description] | [How/If detected] | [How could prevent] |
| Installation | [Description] | [How/If detected] | [How could prevent] |
| Command & Control | [Description] | [How/If detected] | [How could prevent] |
| Actions on Objectives | [Description] | [How/If detected] | [How could prevent] |

---

## 4. Response Evaluation

### What Went Well

| Area | Description | Evidence |
|------|-------------|----------|
| Detection | [What worked in detection] | [Specific examples] |
| Response | [What worked in response] | [Specific examples] |
| Communication | [What worked in communication] | [Specific examples] |
| Coordination | [What worked in coordination] | [Specific examples] |
| Tools | [What tools helped] | [Specific examples] |

### What Could Be Improved

| Area | Issue | Impact | Recommendation |
|------|-------|--------|----------------|
| Detection | [Gap identified] | [How it affected response] | [Suggested improvement] |
| Response | [Gap identified] | [How it affected response] | [Suggested improvement] |
| Communication | [Gap identified] | [How it affected response] | [Suggested improvement] |
| Process | [Gap identified] | [How it affected response] | [Suggested improvement] |
| Tools | [Gap identified] | [How it affected response] | [Suggested improvement] |
| Training | [Gap identified] | [How it affected response] | [Suggested improvement] |

### Where We Got Lucky

[List any factors that helped but weren't by design - these represent risks that need addressing]

1. [Lucky factor 1]
2. [Lucky factor 2]

---

## 5. Impact Assessment

### Business Impact

| Impact Area | Description | Quantification |
|-------------|-------------|----------------|
| Revenue | [Description] | [$XXX] |
| Productivity | [Description] | [Hours lost] |
| Reputation | [Description] | [Assessment] |
| Customer Impact | [Description] | [Number affected] |
| Regulatory | [Description] | [Fines/requirements] |
| Legal | [Description] | [Assessment] |

### Technical Impact

| Impact Area | Description | Recovery Time |
|-------------|-------------|---------------|
| Systems | [Description] | [Time] |
| Data | [Description] | [Time/N/A] |
| Network | [Description] | [Time] |
| Applications | [Description] | [Time] |

### Total Cost Estimate

| Cost Category | Amount |
|---------------|--------|
| Incident Response (internal) | $[XXX] |
| External Consultants/Forensics | $[XXX] |
| Legal Fees | $[XXX] |
| Notification Costs | $[XXX] |
| Credit Monitoring | $[XXX] |
| System Recovery | $[XXX] |
| Lost Revenue | $[XXX] |
| Regulatory Fines | $[XXX] |
| Other | $[XXX] |
| **Total** | **$[XXX]** |

---

## 6. Action Items

### Immediate Actions (0-30 Days)

| ID | Action | Owner | Deadline | Status |
|----|--------|-------|----------|--------|
| 1 | [Action item] | [Name] | [Date] | [Status] |
| 2 | [Action item] | [Name] | [Date] | [Status] |
| 3 | [Action item] | [Name] | [Date] | [Status] |

### Short-Term Actions (30-90 Days)

| ID | Action | Owner | Deadline | Status |
|----|--------|-------|----------|--------|
| 4 | [Action item] | [Name] | [Date] | [Status] |
| 5 | [Action item] | [Name] | [Date] | [Status] |
| 6 | [Action item] | [Name] | [Date] | [Status] |

### Long-Term Actions (90+ Days)

| ID | Action | Owner | Deadline | Status |
|----|--------|-------|----------|--------|
| 7 | [Action item] | [Name] | [Date] | [Status] |
| 8 | [Action item] | [Name] | [Date] | [Status] |
| 9 | [Action item] | [Name] | [Date] | [Status] |

---

## 7. Recommendations

### Process Improvements

1. **[Recommendation Title]**
   - Current State: [Description]
   - Recommended Change: [Description]
   - Expected Benefit: [Description]
   - Priority: [High/Medium/Low]

2. **[Recommendation Title]**
   - Current State: [Description]
   - Recommended Change: [Description]
   - Expected Benefit: [Description]
   - Priority: [High/Medium/Low]

### Technology Improvements

1. **[Recommendation Title]**
   - Gap Addressed: [Description]
   - Solution: [Description]
   - Estimated Cost: [$XXX]
   - Priority: [High/Medium/Low]

### Training Improvements

1. **[Recommendation Title]**
   - Current Gap: [Description]
   - Training Needed: [Description]
   - Target Audience: [Description]
   - Priority: [High/Medium/Low]

### Policy/Procedure Updates

| Document | Change Needed | Owner |
|----------|---------------|-------|
| [Document name] | [Description of change] | [Name] |
| [Document name] | [Description of change] | [Name] |

---

## 8. Review Participants

### Post-Incident Review Meeting

**Date:** [DATE]

**Duration:** [TIME]

**Attendees:**

| Name | Role | Department |
|------|------|------------|
| [Name] | [Role in incident/review] | [Department] |
| [Name] | [Role in incident/review] | [Department] |
| [Name] | [Role in incident/review] | [Department] |

---

## 9. Appendices

### Appendix A: Evidence Log

| Item | Description | Location |
|------|-------------|----------|
| [Evidence 1] | [Description] | [Storage location] |
| [Evidence 2] | [Description] | [Storage location] |

### Appendix B: Related Documents

- [Link to incident report]
- [Link to forensics report]
- [Link to communication logs]

### Appendix C: Indicators of Compromise

[List IoCs for future detection]

---

## Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Review Facilitator | | | |
| Security Lead | | | |
| IT Manager | | | |
| [Other stakeholder] | | | |

---

## Review Schedule

- **30-Day Follow-up:** [DATE] - Review action item progress
- **90-Day Follow-up:** [DATE] - Verify improvements implemented
- **Annual Review:** Include in yearly security review

---

[Back to Templates](./README.md) | [Back to Crisis Management](../README.md)

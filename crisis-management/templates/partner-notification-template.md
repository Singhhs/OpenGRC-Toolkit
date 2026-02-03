# Partner/Vendor Notification Templates

Templates for notifying business partners, vendors, and third parties about security incidents.

**IMPORTANT:** Review contractual notification requirements before sending. Coordinate with Legal.

---

## Partner Breach Notification

### Formal Partner Notification Letter

**[ORGANIZATION LETTERHEAD]**

**CONFIDENTIAL**

[DATE]

[PARTNER CONTACT NAME]
[TITLE]
[COMPANY NAME]
[ADDRESS]

**RE: Security Incident Notification**

Dear [NAME],

We are writing to notify you of a security incident that [may affect your organization / involves data shared as part of our business relationship].

**Incident Summary**

On [DATE], [ORGANIZATION NAME] discovered [brief description of incident]. We are notifying you because [reason - e.g., "we share data with your organization" / "your systems may have been affected" / "per our contractual requirements"].

**What Happened**

[Description appropriate for partner, including:]
- Nature of the incident
- Timeline
- Systems or data involved

**Impact to Your Organization**

Based on our investigation, [description of how partner may be affected]:
- Data shared between our organizations: [DESCRIPTION]
- Systems with connectivity: [DESCRIPTION]
- Potential exposure: [DESCRIPTION]

**Actions Taken**

We have taken the following steps:
- [Action 1]
- [Action 2]
- [Action 3]

**Recommended Actions for Your Organization**

We recommend you consider:
1. [Recommendation 1 - e.g., Review access logs for connections to our systems]
2. [Recommendation 2 - e.g., Rotate credentials used for integration]
3. [Recommendation 3]

**Technical Indicators**

[If applicable, provide IoCs:]
- IP Addresses: [LIST]
- Domains: [LIST]
- File Hashes: [LIST]
- Timeframe of concern: [DATES]

**Point of Contact**

For questions or to coordinate response:

| Role | Name | Contact |
|------|------|---------|
| Primary Contact | [NAME] | [EMAIL / PHONE] |
| Technical Contact | [NAME] | [EMAIL / PHONE] |
| Legal Contact | [NAME] | [EMAIL / PHONE] |

**Confidentiality**

We request that you treat this notification as confidential. Please do not disclose incident details publicly without coordinating with us first.

**Contractual Notification**

This notification is being provided [in accordance with Section [X] of our [AGREEMENT NAME] dated [DATE] / as a courtesy notification].

We regret any concern this may cause and are committed to transparency with our valued partners.

Sincerely,

[SIGNATURE]

[NAME]
[TITLE]
[ORGANIZATION NAME]

---

## Vendor Security Alert

### Email Template - Informing Vendors

**To:** [VENDOR SECURITY CONTACT]

**From:** [YOUR SECURITY CONTACT]

**Subject:** CONFIDENTIAL - Security Incident Notification

---

Dear [NAME],

This message is to notify you of a security incident at [ORGANIZATION NAME] that may be relevant to your organization due to our business relationship.

**Summary**

We have experienced [type of incident]. While our investigation is ongoing, we are proactively notifying partners and vendors who [may be affected / have system integrations with us].

**Relevance to Your Organization**

You are receiving this notification because:
- [ ] You have system access to our environment
- [ ] We share data with your organization
- [ ] Your credentials may need to be rotated
- [ ] Contractual notification requirement
- [ ] Other: [SPECIFY]

**Action Requested**

Please take the following steps:

1. **[Immediate Action]** - [Description]
2. **[Short-term Action]** - [Description]
3. **Confirm receipt** of this notification to [EMAIL]

**Timeline**

- Please complete requested actions by: [DATE]
- Please confirm completion to: [EMAIL]

**Questions?**

Contact our security team:
- Email: [EMAIL]
- Phone: [PHONE]
- Secure portal: [URL if applicable]

Thank you for your prompt attention to this matter.

[NAME]
[TITLE]

---

## Customer (B2B) Notification

### Enterprise Customer Notification

**To:** [CUSTOMER SECURITY/IT CONTACT]

**From:** [YOUR CISO/SECURITY LEAD]

**Subject:** Security Incident Notification - [ORGANIZATION NAME]

---

Dear [NAME],

We are writing to inform you of a security incident at [ORGANIZATION NAME].

**Incident Overview**

| Detail | Information |
|--------|-------------|
| Date Discovered | [DATE] |
| Date of Incident | [DATE or RANGE] |
| Type | [DESCRIPTION] |
| Status | [CONTAINED / INVESTIGATING / RESOLVED] |

**Impact Assessment**

**Your data/systems:**
[Description of whether customer data was affected, what data, and to what extent]

**Our services to you:**
[Description of any service impact]

**Actions We Have Taken**

- [Action 1]
- [Action 2]
- [Action 3]

**Recommendations**

Based on our analysis, we recommend:
- [Recommendation 1]
- [Recommendation 2]

**Support Available**

We are prepared to:
- Provide detailed technical briefing
- Share indicators of compromise (IoCs)
- Coordinate incident response activities
- Answer questions from your security team

**Contact Information**

| Purpose | Contact |
|---------|---------|
| Technical questions | [NAME, EMAIL, PHONE] |
| Business questions | [NAME, EMAIL, PHONE] |
| Scheduled briefing | [BOOKING LINK or INSTRUCTIONS] |

**Confidentiality**

Please treat this notification as confidential pending our coordinated communication plan.

We sincerely apologize for any concern this causes and are committed to maintaining your trust.

[NAME]
[TITLE]

---

## Integration Partner Alert

### Technical Partner Notification

**To:** [TECHNICAL CONTACT]

**Subject:** URGENT: Security Alert - API/Integration Credentials

---

**Priority:** HIGH

**Action Required:** Credential rotation and access review

---

**Situation**

We have identified a security incident that may affect the integration between our systems. Out of an abundance of caution, we recommend the following immediate actions.

**Affected Integration**

| Component | Details |
|-----------|---------|
| Integration Type | [API / SSO / Data Feed / etc.] |
| Your System | [DESCRIPTION] |
| Our System | [DESCRIPTION] |
| Credentials Type | [API Key / OAuth / Certificate / etc.] |

**Recommended Actions**

**Immediate (Within 24 Hours):**
1. Rotate API keys / credentials used for integration
2. Review access logs for unusual activity from [DATE] to present
3. Verify integration configurations have not been modified

**Short-term (Within 1 Week):**
1. Review user accounts with access to integration
2. Audit data exchanged via integration
3. Update to latest security patches

**We Will Provide:**
- New credentials via secure channel
- Updated certificates (if applicable)
- Technical support for reconfiguration

**Coordination**

Let's schedule a brief call to coordinate:
- Available times: [OPTIONS]
- Or book directly: [CALENDLY/BOOKING LINK]

**Secure Communication**

For sensitive technical details, please use:
- Encrypted email: [PGP KEY or SECURE EMAIL ADDRESS]
- Secure file share: [LINK]

Contact me immediately at [PHONE] if you observe any unusual activity.

[NAME]
[TITLE]

---

## Notification Tracking Log

### Partner Notification Record

| Partner | Contact | Method | Date Sent | Acknowledged | Follow-up |
|---------|---------|--------|-----------|--------------|-----------|
| [Partner 1] | [Name] | Email | [Date] | [Yes/No] | [Date/Action] |
| [Partner 2] | [Name] | Email + Call | [Date] | [Yes/No] | [Date/Action] |
| [Partner 3] | [Name] | Letter | [Date] | [Yes/No] | [Date/Action] |

---

## Contractual Requirements Checklist

Before notifying, verify:

- [ ] Reviewed contract for notification requirements
- [ ] Identified notification timeline (e.g., 24 hours, 72 hours)
- [ ] Identified required notification method
- [ ] Identified required recipients
- [ ] Identified required content elements
- [ ] Legal approved notification
- [ ] Documented notification for compliance

---

[Back to Templates](./README.md) | [Back to Crisis Management](../README.md)

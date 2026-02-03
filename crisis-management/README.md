# Crisis Management

Resources for managing security incidents, crises, and business continuity events.

## Contents

- [Playbooks](./playbooks/README.md) - Incident response playbooks for specific scenarios
- [Templates](./templates/README.md) - Communication and documentation templates

## Quick Reference

### Severity Levels

| Level | Description | Response Team |
|-------|-------------|---------------|
| **Critical (P1)** | Business-threatening, active attack | Full CSIRT, Executive |
| **High (P2)** | Significant impact, contained | CSIRT core team |
| **Medium (P3)** | Moderate impact, limited scope | Security team |
| **Low (P4)** | Minimal impact, routine | On-call analyst |

### Immediate Actions for Critical Incidents

1. **Assess** - Confirm incident and severity
2. **Contain** - Stop the bleeding, isolate affected systems
3. **Notify** - Alert CSIRT, management, stakeholders
4. **Investigate** - Gather evidence, determine scope
5. **Remediate** - Remove threat, restore systems
6. **Communicate** - Keep stakeholders informed
7. **Review** - Document and learn

### Emergency Contacts

<!-- CUSTOMIZE: Add your organization's emergency contacts -->

| Role | Name | Phone | Email |
|------|------|-------|-------|
| Incident Manager | [NAME] | [PHONE] | [EMAIL] |
| IT Security Lead | [NAME] | [PHONE] | [EMAIL] |
| CISO | [NAME] | [PHONE] | [EMAIL] |
| Legal | [NAME] | [PHONE] | [EMAIL] |
| Communications/PR | [NAME] | [PHONE] | [EMAIL] |
| Executive Sponsor | [NAME] | [PHONE] | [EMAIL] |

### Bridge Call Information

```
Primary: [PHONE NUMBER / CONFERENCE URL]
Backup:  [ALTERNATE PHONE / URL]
PIN:     [IF APPLICABLE]
```

## Playbook Index (11 Playbooks)

### Core Incident Playbooks
| Scenario | Playbook | Priority |
|----------|----------|----------|
| Ransomware | [Ransomware Playbook](./playbooks/ransomware-playbook.md) | Critical |
| Data Breach | [Data Breach Playbook](./playbooks/data-breach-playbook.md) | Critical |
| Phishing/BEC | [Phishing Playbook](./playbooks/phishing-playbook.md) | Critical |
| Malware (non-ransomware) | [Malware Playbook](./playbooks/malware-playbook.md) | High |
| Account Compromise | [Account Compromise Playbook](./playbooks/account-compromise-playbook.md) | High |

### Infrastructure & Service Playbooks
| Scenario | Playbook | Priority |
|----------|----------|----------|
| DDoS Attack | [DDoS Playbook](./playbooks/ddos-playbook.md) | High |
| Third-Party Breach | [Third Party Playbook](./playbooks/third-party-breach-playbook.md) | High |

### Physical & Human-Focused Playbooks
| Scenario | Playbook | Priority |
|----------|----------|----------|
| Lost/Stolen Device | [Lost Device Playbook](./playbooks/lost-device-playbook.md) | High |
| Insider Threat | [Insider Threat Playbook](./playbooks/insider-threat-playbook.md) | High |
| Social Engineering | [Social Engineering Playbook](./playbooks/social-engineering-playbook.md) | Medium |
| Physical Security Breach | [Physical Security Playbook](./playbooks/physical-security-playbook.md) | Medium |

## Communication Templates

| Template | Use |
|----------|-----|
| [Internal Notification](./templates/internal-notification-template.md) | Alert internal teams |
| [Executive Briefing](./templates/executive-briefing-template.md) | Update leadership |
| [Customer Notification](./templates/customer-notification-template.md) | Notify affected customers |
| [Press Statement](./templates/press-statement-template.md) | Media response |
| [Regulatory Notification](./templates/regulatory-notification-template.md) | Report to authorities |

## Related Documents

- [Incident Response Policy](../policies/incident-response-policy.md)
- [Incident Response Procedure](../procedures/incident-response-procedure.md)
- [Business Continuity Policy](../policies/business-continuity-policy.md)

---

[Back to Home](../README.md)

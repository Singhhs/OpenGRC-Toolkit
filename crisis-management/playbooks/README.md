# Incident Response Playbooks

Step-by-step guides for responding to specific incident types.

## Available Playbooks (11)

### Core Incident Playbooks

| Playbook | Scenario | Priority |
|----------|----------|----------|
| [Ransomware](./ransomware-playbook.md) | Ransomware infection and encryption | Critical |
| [Data Breach](./data-breach-playbook.md) | Unauthorized data access or exfiltration | Critical |
| [Phishing/BEC](./phishing-playbook.md) | Phishing attacks and business email compromise | Critical |
| [Malware](./malware-playbook.md) | General malware (trojans, worms, spyware, RATs) | High |
| [Account Compromise](./account-compromise-playbook.md) | Credential theft, account takeover | High |

### Infrastructure & Service Playbooks

| Playbook | Scenario | Priority |
|----------|----------|----------|
| [DDoS Attack](./ddos-playbook.md) | Volumetric, protocol, and application layer attacks | High |
| [Third-Party Breach](./third-party-breach-playbook.md) | Vendor, supplier, or supply chain incident | High |

### Physical & Human-Focused Playbooks

| Playbook | Scenario | Priority |
|----------|----------|----------|
| [Lost/Stolen Device](./lost-device-playbook.md) | Lost or stolen laptops, phones, media | High |
| [Insider Threat](./insider-threat-playbook.md) | Malicious or negligent insider activity | High |
| [Social Engineering](./social-engineering-playbook.md) | Vishing, pretexting, impersonation, baiting | Medium |
| [Physical Security](./physical-security-playbook.md) | Unauthorized access, theft, vandalism | Medium |

---

## Planned Playbooks (To Do)

| Playbook | Scenario | Priority |
|----------|----------|----------|
| Website Defacement | Public website compromise | Medium |
| Cryptojacking | Unauthorized cryptocurrency mining | Low |
| Cloud Security Incident | Cloud-specific breach or misconfiguration | Medium |
| IoT/OT Compromise | Industrial control or IoT device incident | Low |

---

## Playbook Structure

Each playbook follows a consistent structure:

1. **Overview** - What this playbook covers
2. **Detection Indicators** - How to identify this incident type
3. **Severity Assessment** - How to classify severity
4. **Immediate Actions** - First 30 minutes
5. **Containment** - Stop the bleeding
6. **Investigation** - Determine scope and cause
7. **Eradication** - Remove the threat
8. **Recovery** - Restore normal operations
9. **Communication** - Who to notify and when
10. **Post-Incident** - Documentation and improvements

---

## How to Use

1. Identify the incident type
2. Open the corresponding playbook
3. Follow the steps in order
4. Adapt as needed for your specific situation
5. Document all actions taken
6. Conduct post-incident review

---

## Quick Reference

### Severity Levels

| Level | Description | Response |
|-------|-------------|----------|
| **P1 Critical** | Business-threatening, active attack | Immediate, all hands |
| **P2 High** | Significant impact, contained | Priority response |
| **P3 Medium** | Moderate impact, limited scope | Standard response |
| **P4 Low** | Minimal impact, routine | Normal process |

### Response Times

| Severity | Initial Response | Escalation |
|----------|-----------------|------------|
| P1 | Immediate | Executive immediately |
| P2 | < 1 hour | Management within 4 hours |
| P3 | < 4 hours | Daily update |
| P4 | < 24 hours | Weekly update |

---

## Contributing

We welcome contributions of new playbooks. See [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines.

Priority playbooks needed:
- Website Defacement
- Cloud Security Incident
- IoT/OT Compromise

---

[Back to Crisis Management](../README.md) | [Back to Home](../../README.md)

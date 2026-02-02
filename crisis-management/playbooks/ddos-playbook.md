# DDoS Attack Response Playbook

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Classification** | Internal |

---

## 1. Overview

This playbook provides step-by-step guidance for responding to Distributed Denial of Service (DDoS) attacks against [ORGANIZATION NAME] infrastructure and services.

### Attack Types Covered
- **Volumetric attacks**: UDP floods, ICMP floods, amplification attacks
- **Protocol attacks**: SYN floods, fragmented packet attacks, Ping of Death
- **Application layer attacks**: HTTP floods, slowloris, DNS query floods

---

## 2. Detection Indicators

### 2.1 Technical Indicators

| Indicator | Description |
|-----------|-------------|
| Sudden traffic spike | Abnormal increase in inbound traffic |
| Service unavailability | Websites or applications not responding |
| High bandwidth utilization | Network links saturated |
| High CPU/memory on network devices | Firewalls, routers overwhelmed |
| Unusual traffic patterns | Single IP, geographic anomaly, specific ports |
| Connection timeouts | Legitimate users cannot connect |
| Increased latency | Slow response times |
| Alert from DDoS protection service | Mitigation triggered |

### 2.2 User Reports

- Unable to access websites or services
- Extremely slow performance
- Connection errors or timeouts
- Intermittent availability

---

## 3. Severity Assessment

| Level | Criteria | Response |
|-------|----------|----------|
| **P1 Critical** | Business-critical services down, revenue impact, customer-facing outage | Immediate, all hands |
| **P2 High** | Significant services affected, degraded performance widespread | Priority response |
| **P3 Medium** | Non-critical services affected, limited user impact | Standard response |
| **P4 Low** | Attack detected but mitigated, no service impact | Monitor and document |

---

## 4. Response Team

| Role | Responsibility | Contact |
|------|----------------|---------|
| Incident Commander | Overall coordination | [NAME/PHONE] |
| Network Team Lead | Traffic analysis, mitigation | [NAME/PHONE] |
| Security Analyst | Attack analysis, threat intel | [NAME/PHONE] |
| ISP/CDN Contact | Upstream mitigation | [PROVIDER/PHONE] |
| DDoS Service Contact | Scrubbing activation | [PROVIDER/PHONE] |
| Communications Lead | Internal/external comms | [NAME/PHONE] |
| Management Contact | Escalation, decisions | [NAME/PHONE] |

---

## 5. Immediate Actions (First 15 Minutes)

### 5.1 Confirm the Attack

```
□ Step 1: Verify service unavailability
  - Check from multiple locations/networks
  - Confirm not an internal issue (server, application)
  - Check monitoring dashboards

□ Step 2: Analyze traffic patterns
  - Review firewall/IDS logs
  - Check NetFlow/traffic analysis
  - Identify attack characteristics:
    • Source IPs (single/distributed)
    • Target (IP, port, service)
    • Attack type (volumetric, protocol, application)
    • Traffic volume

□ Step 3: Document initial findings
  - Time attack started
  - Services affected
  - Initial traffic analysis
  - Impact assessment
```

### 5.2 Activate Response

```
□ Step 4: Notify response team
  - Alert Incident Commander
  - Notify Network Team
  - Contact Security Team

□ Step 5: Establish communication channel
  - Open bridge call/war room
  - Create incident chat channel
  - Assign note-taker

□ Step 6: Classify severity
  - Assess business impact
  - Determine response level
  - Escalate if P1/P2
```

---

## 6. Containment (15-60 Minutes)

### 6.1 Initial Mitigation

```
□ Step 7: Activate DDoS protection
  - Enable cloud-based scrubbing (if available)
  - Contact DDoS mitigation provider
  - Redirect traffic through scrubbing center

□ Step 8: Implement edge filtering
  - Block obvious attack sources (if identifiable)
  - Rate limit suspicious traffic
  - Enable SYN cookies (if SYN flood)
  - Implement geo-blocking (if appropriate)

□ Step 9: Contact upstream providers
  - Notify ISP of attack
  - Request upstream filtering
  - Coordinate mitigation efforts
```

### 6.2 Traffic Management

```
□ Step 10: Analyze and filter attack traffic

  For Volumetric Attacks:
  - Identify attack signatures
  - Block at perimeter/upstream
  - Null-route if necessary

  For Protocol Attacks:
  - Tune firewall settings
  - Adjust connection limits
  - Enable protocol-specific protections

  For Application Attacks:
  - Enable WAF rules
  - Implement CAPTCHA/challenge
  - Rate limit by IP/session
  - Block malicious patterns

□ Step 11: Protect critical services
  - Prioritize business-critical applications
  - Consider temporary service restrictions
  - Enable maintenance page if needed
```

### 6.3 Infrastructure Protection

```
□ Step 12: Protect infrastructure
  - Monitor firewall/router health
  - Scale resources if cloud-based
  - Distribute load across resources
  - Consider CDN for static content

□ Step 13: Document all actions
  - Log all mitigation steps
  - Record traffic patterns
  - Capture evidence for analysis
```

---

## 7. Eradication and Recovery

### 7.1 Monitor and Adjust

```
□ Step 14: Continuously monitor
  - Track attack evolution
  - Adjust filters as attack changes
  - Monitor service availability
  - Watch for secondary attacks

□ Step 15: Verify mitigation effectiveness
  - Confirm legitimate traffic passing
  - Check service availability
  - Monitor false positive rate
  - Adjust rules as needed
```

### 7.2 Service Restoration

```
□ Step 16: Gradually restore services
  - Monitor for attack resumption
  - Remove temporary restrictions carefully
  - Test service functionality
  - Verify user access

□ Step 17: Maintain elevated monitoring
  - Keep enhanced monitoring active
  - Watch for attack pattern changes
  - Be prepared to re-engage mitigation
```

---

## 8. Communication

### 8.1 Internal Communication

| Audience | When | Message |
|----------|------|---------|
| IT Teams | Immediately | Attack details, actions needed |
| Help Desk | Immediately | Service status, user guidance |
| Management | Within 30 min | Impact summary, response status |
| All Staff | If prolonged | Service status update |

### 8.2 External Communication

| Audience | When | Message |
|----------|------|---------|
| Customers | If customer-facing impact | Service status, ETA |
| Partners | If partner services affected | Impact and status |
| Regulators | If required | Per regulatory requirements |

### 8.3 Status Page Updates

```
Example Messages:

Initial:
"We are currently experiencing a service disruption. Our team is
investigating and working to restore normal operations. Updates
will be provided as available."

During:
"We have identified a network attack affecting our services.
Mitigation measures are in place. Some users may experience
intermittent access. We appreciate your patience."

Resolved:
"The service disruption has been resolved. All services are
operating normally. We apologize for any inconvenience."
```

---

## 9. Post-Incident

### 9.1 Immediate Actions

```
□ Step 18: Confirm attack has ended
  - Traffic returned to normal
  - Services fully operational
  - No residual issues

□ Step 19: Stand down response
  - Close bridge call
  - Thank response team
  - Schedule post-incident review

□ Step 20: Initial documentation
  - Complete incident timeline
  - Document all actions taken
  - Capture traffic/log samples
```

### 9.2 Post-Incident Review (Within 5 Days)

```
□ Step 21: Conduct post-incident review

  Review Topics:
  - Attack characteristics and timeline
  - Detection effectiveness
  - Response time and actions
  - Mitigation effectiveness
  - Communication effectiveness
  - What worked well
  - What could improve

□ Step 22: Document lessons learned
  - Update playbook if needed
  - Identify security improvements
  - Create action items

□ Step 23: Update defenses
  - Tune detection rules
  - Update firewall configurations
  - Enhance DDoS protection
  - Consider additional services
```

---

## 10. Mitigation Techniques Reference

### 10.1 Volumetric Attack Mitigation

| Technique | Description |
|-----------|-------------|
| Cloud scrubbing | Route traffic through DDoS mitigation service |
| Upstream filtering | ISP-level traffic filtering |
| Black hole routing | Null-route attack traffic |
| Rate limiting | Limit traffic rates |
| Geo-blocking | Block traffic from specific regions |

### 10.2 Protocol Attack Mitigation

| Technique | Description |
|-----------|-------------|
| SYN cookies | Handle SYN floods without state |
| Connection limits | Limit connections per source |
| Timeout tuning | Adjust connection timeouts |
| Protocol validation | Drop malformed packets |

### 10.3 Application Attack Mitigation

| Technique | Description |
|-----------|-------------|
| WAF rules | Block malicious requests |
| CAPTCHA | Challenge suspicious requests |
| Rate limiting | Limit requests per IP/session |
| Bot detection | Identify and block bots |
| Caching | Reduce origin load |

---

## 11. Tools and Resources

### 11.1 Monitoring Tools

| Tool | Purpose | Access |
|------|---------|--------|
| [Network monitoring] | Traffic analysis | [URL/Location] |
| [SIEM] | Log analysis | [URL/Location] |
| [DDoS dashboard] | Attack visibility | [URL/Location] |
| [Status page] | External status | [URL/Location] |

### 11.2 Mitigation Services

| Service | Purpose | Contact |
|---------|---------|---------|
| [DDoS protection] | Cloud scrubbing | [Contact info] |
| [CDN provider] | Edge protection | [Contact info] |
| [ISP] | Upstream filtering | [Contact info] |

---

## 12. Escalation Matrix

| Condition | Escalate To | Contact |
|-----------|-------------|---------|
| P1 attack confirmed | IT Director + CISO | [PHONE] |
| Customer impact >30 min | Executive team | [PHONE] |
| Attack >2 hours | CEO/COO | [PHONE] |
| Data breach suspected | Legal + CISO | [PHONE] |
| Media inquiry | Communications | [PHONE] |

---

## 13. Related Documents

- [Incident Response Policy](../../policies/incident-response-policy.md)
- [Incident Response Procedure](../../procedures/incident-response-procedure.md)
- [Business Continuity Policy](../../policies/business-continuity-policy.md)
- [Network Security Policy](../../policies/network-security-policy.md)

---

## 14. Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Playbooks](./README.md) | [Back to Crisis Management](../README.md)

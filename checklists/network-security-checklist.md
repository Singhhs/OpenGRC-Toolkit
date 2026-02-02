# Network Security Checklist

| Document Control | |
|-----------------|---|
| **Version** | [VERSION] |
| **Date** | [DATE] |
| **Assessor** | [NAME] |
| **Network/Segment** | [NETWORK NAME] |

---

## Purpose

Use this checklist to assess network security controls and configurations. Applicable for network architecture reviews, audits, and security assessments.

---

## Section 1: Network Information

| Field | Information |
|-------|-------------|
| Network/Segment Name | |
| Network Range | |
| Environment | ☐ Production ☐ Corporate ☐ DMZ ☐ Development ☐ Guest |
| Data Classification | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| Network Owner | |
| Last Assessment Date | |

---

## Section 2: Network Architecture

### 2.1 Documentation

| # | Item | Status | Location | Notes |
|---|------|--------|----------|-------|
| 2.1.1 | Network topology diagram current | ☐ Yes ☐ No ☐ Partial | | |
| 2.1.2 | IP addressing scheme documented | ☐ Yes ☐ No | | |
| 2.1.3 | VLAN assignments documented | ☐ Yes ☐ No | | |
| 2.1.4 | Firewall rules documented | ☐ Yes ☐ No ☐ Partial | | |
| 2.1.5 | Network device inventory maintained | ☐ Yes ☐ No | | |
| 2.1.6 | Data flow diagrams available | ☐ Yes ☐ No ☐ Partial | | |

### 2.2 Segmentation

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 2.2.1 | Network properly segmented by function | ☐ Yes ☐ No ☐ Partial | |
| 2.2.2 | Sensitive systems in separate segment | ☐ Yes ☐ No | |
| 2.2.3 | DMZ properly isolated | ☐ Yes ☐ No ☐ N/A | |
| 2.2.4 | Development/test separated from production | ☐ Yes ☐ No | |
| 2.2.5 | Guest network isolated | ☐ Yes ☐ No ☐ N/A | |
| 2.2.6 | IoT/OT networks isolated | ☐ Yes ☐ No ☐ N/A | |
| 2.2.7 | Management network separated | ☐ Yes ☐ No | |
| 2.2.8 | VLANs properly configured | ☐ Yes ☐ No | |
| 2.2.9 | Inter-VLAN routing controlled | ☐ Yes ☐ No | |

---

## Section 3: Perimeter Security

### 3.1 Firewall Configuration

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.1.1 | Firewall deployed at perimeter | ☐ Yes ☐ No | |
| 3.1.2 | Default deny rule in place | ☐ Yes ☐ No | |
| 3.1.3 | Stateful inspection enabled | ☐ Yes ☐ No | |
| 3.1.4 | Rules follow least privilege | ☐ Yes ☐ No ☐ Partial | |
| 3.1.5 | Rules documented with justification | ☐ Yes ☐ No ☐ Partial | |
| 3.1.6 | "Any" source/destination rules minimized | ☐ Yes ☐ No | Count: |
| 3.1.7 | Unused rules removed | ☐ Yes ☐ No | |
| 3.1.8 | Temporary rules have expiration | ☐ Yes ☐ No ☐ N/A | |
| 3.1.9 | Rules reviewed periodically | ☐ Yes ☐ No | Frequency: |
| 3.1.10 | Change control for rule changes | ☐ Yes ☐ No | |

### 3.2 Intrusion Detection/Prevention

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.2.1 | IDS/IPS deployed at perimeter | ☐ Yes ☐ No | |
| 3.2.2 | Signatures updated regularly | ☐ Yes ☐ No | |
| 3.2.3 | Custom rules for environment | ☐ Yes ☐ No | |
| 3.2.4 | Alerts reviewed and actioned | ☐ Yes ☐ No | |
| 3.2.5 | False positives tuned | ☐ Yes ☐ No | |
| 3.2.6 | Integration with SIEM | ☐ Yes ☐ No | |
| 3.2.7 | Prevention mode enabled (IPS) | ☐ Yes ☐ No ☐ N/A | |

### 3.3 DDoS Protection

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 3.3.1 | DDoS mitigation capability | ☐ Yes ☐ No | |
| 3.3.2 | Rate limiting configured | ☐ Yes ☐ No | |
| 3.3.3 | SYN flood protection | ☐ Yes ☐ No | |
| 3.3.4 | Traffic anomaly detection | ☐ Yes ☐ No | |
| 3.3.5 | Scrubbing service available | ☐ Yes ☐ No ☐ N/A | |

---

## Section 4: Internal Network Security

### 4.1 Switch Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.1.1 | Unused ports disabled | ☐ Yes ☐ No ☐ Partial | |
| 4.1.2 | Port security enabled | ☐ Yes ☐ No ☐ Partial | |
| 4.1.3 | MAC address limiting configured | ☐ Yes ☐ No | |
| 4.1.4 | DHCP snooping enabled | ☐ Yes ☐ No | |
| 4.1.5 | Dynamic ARP inspection enabled | ☐ Yes ☐ No | |
| 4.1.6 | IP source guard configured | ☐ Yes ☐ No | |
| 4.1.7 | BPDU guard enabled | ☐ Yes ☐ No | |
| 4.1.8 | Root guard enabled | ☐ Yes ☐ No | |
| 4.1.9 | Private VLANs used where appropriate | ☐ Yes ☐ No ☐ N/A | |

### 4.2 Router Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.2.1 | Access control lists configured | ☐ Yes ☐ No | |
| 4.2.2 | Unused interfaces disabled | ☐ Yes ☐ No | |
| 4.2.3 | Source routing disabled | ☐ Yes ☐ No | |
| 4.2.4 | ICMP redirects disabled | ☐ Yes ☐ No | |
| 4.2.5 | Proxy ARP disabled | ☐ Yes ☐ No | |
| 4.2.6 | IP directed broadcast disabled | ☐ Yes ☐ No | |
| 4.2.7 | Anti-spoofing filters in place | ☐ Yes ☐ No | |

### 4.3 Network Access Control (NAC)

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 4.3.1 | NAC solution deployed | ☐ Yes ☐ No | Product: |
| 4.3.2 | 802.1X authentication configured | ☐ Yes ☐ No | |
| 4.3.3 | Device health/posture checking | ☐ Yes ☐ No | |
| 4.3.4 | Unknown devices quarantined | ☐ Yes ☐ No | |
| 4.3.5 | Guest portal configured | ☐ Yes ☐ No ☐ N/A | |

---

## Section 5: Wireless Security

### 5.1 Corporate Wireless

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.1.1 | WPA3 or WPA2-Enterprise used | ☐ Yes ☐ No ☐ N/A | Protocol: |
| 5.1.2 | 802.1X/RADIUS authentication | ☐ Yes ☐ No ☐ N/A | |
| 5.1.3 | Strong encryption (AES) | ☐ Yes ☐ No | |
| 5.1.4 | SSID not revealing organization info | ☐ Yes ☐ No | |
| 5.1.5 | Management interface secured | ☐ Yes ☐ No | |
| 5.1.6 | Access points physically secured | ☐ Yes ☐ No | |
| 5.1.7 | Signal strength appropriate (not extending beyond premises) | ☐ Yes ☐ No | |
| 5.1.8 | Client isolation enabled where appropriate | ☐ Yes ☐ No ☐ N/A | |

### 5.2 Guest Wireless

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.2.1 | Guest network isolated from corporate | ☐ Yes ☐ No ☐ N/A | |
| 5.2.2 | Internet access only | ☐ Yes ☐ No | |
| 5.2.3 | Terms of use acknowledgment | ☐ Yes ☐ No | |
| 5.2.4 | Bandwidth limited | ☐ Yes ☐ No | |
| 5.2.5 | Session time limits | ☐ Yes ☐ No | Duration: |
| 5.2.6 | Usage logged | ☐ Yes ☐ No | |

### 5.3 Rogue Detection

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 5.3.1 | Rogue AP detection enabled | ☐ Yes ☐ No | |
| 5.3.2 | Unauthorized AP alerting | ☐ Yes ☐ No | |
| 5.3.3 | Regular wireless assessments | ☐ Yes ☐ No | Frequency: |

---

## Section 6: Remote Access

### 6.1 VPN Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 6.1.1 | VPN required for remote access | ☐ Yes ☐ No | |
| 6.1.2 | Strong encryption (AES-256) | ☐ Yes ☐ No | |
| 6.1.3 | MFA required for VPN | ☐ Yes ☐ No | |
| 6.1.4 | Modern protocols (IKEv2, OpenVPN, WireGuard) | ☐ Yes ☐ No | Protocol: |
| 6.1.5 | Split tunneling disabled (or controlled) | ☐ Yes ☐ No | |
| 6.1.6 | Session timeout configured | ☐ Yes ☐ No | Timeout: |
| 6.1.7 | VPN access logged | ☐ Yes ☐ No | |
| 6.1.8 | Endpoint compliance checked | ☐ Yes ☐ No | |

### 6.2 Third-Party Access

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 6.2.1 | Separate accounts for third parties | ☐ Yes ☐ No ☐ N/A | |
| 6.2.2 | Access time-limited | ☐ Yes ☐ No | |
| 6.2.3 | Access scope restricted | ☐ Yes ☐ No | |
| 6.2.4 | Session recording (if required) | ☐ Yes ☐ No ☐ N/A | |
| 6.2.5 | Access reviewed regularly | ☐ Yes ☐ No | |

---

## Section 7: Network Services

### 7.1 DNS Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.1.1 | Internal DNS servers used | ☐ Yes ☐ No | |
| 7.1.2 | DNS traffic monitored | ☐ Yes ☐ No | |
| 7.1.3 | DNS filtering/blocking configured | ☐ Yes ☐ No | |
| 7.1.4 | DNSSEC enabled (if applicable) | ☐ Yes ☐ No ☐ N/A | |
| 7.1.5 | DNS over HTTPS/TLS for privacy | ☐ Yes ☐ No ☐ N/A | |
| 7.1.6 | DNS query logging enabled | ☐ Yes ☐ No | |

### 7.2 DHCP Security

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.2.1 | Authorized DHCP servers only | ☐ Yes ☐ No | |
| 7.2.2 | DHCP snooping enabled | ☐ Yes ☐ No | |
| 7.2.3 | DHCP leases logged | ☐ Yes ☐ No | |
| 7.2.4 | Static reservations for critical systems | ☐ Yes ☐ No | |

### 7.3 Time Synchronization

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 7.3.1 | NTP configured on all devices | ☐ Yes ☐ No | |
| 7.3.2 | Authenticated NTP (if available) | ☐ Yes ☐ No ☐ N/A | |
| 7.3.3 | Time synchronization monitored | ☐ Yes ☐ No | |

---

## Section 8: Network Device Management

### 8.1 Device Hardening

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 8.1.1 | Default credentials changed | ☐ Yes ☐ No | |
| 8.1.2 | Strong passwords/keys used | ☐ Yes ☐ No | |
| 8.1.3 | Unnecessary services disabled | ☐ Yes ☐ No | |
| 8.1.4 | Firmware/software current | ☐ Yes ☐ No | |
| 8.1.5 | Security patches applied | ☐ Yes ☐ No | |
| 8.1.6 | Management interface secured | ☐ Yes ☐ No | |
| 8.1.7 | SNMP secured (v3 or disabled) | ☐ Yes ☐ No | |
| 8.1.8 | Telnet disabled (SSH only) | ☐ Yes ☐ No | |
| 8.1.9 | HTTP disabled (HTTPS only) | ☐ Yes ☐ No | |
| 8.1.10 | Logging enabled | ☐ Yes ☐ No | |

### 8.2 Configuration Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 8.2.1 | Configuration backup automated | ☐ Yes ☐ No | |
| 8.2.2 | Configuration version controlled | ☐ Yes ☐ No | |
| 8.2.3 | Change control for configurations | ☐ Yes ☐ No | |
| 8.2.4 | Configuration drift monitoring | ☐ Yes ☐ No | |
| 8.2.5 | Baseline configurations documented | ☐ Yes ☐ No | |

### 8.3 Access Management

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 8.3.1 | Individual accounts for administrators | ☐ Yes ☐ No | |
| 8.3.2 | Role-based access configured | ☐ Yes ☐ No | |
| 8.3.3 | MFA for administrative access | ☐ Yes ☐ No | |
| 8.3.4 | Management access from specific IPs/networks | ☐ Yes ☐ No | |
| 8.3.5 | Access logging enabled | ☐ Yes ☐ No | |
| 8.3.6 | Session timeout configured | ☐ Yes ☐ No | |

---

## Section 9: Network Monitoring

### 9.1 Traffic Monitoring

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 9.1.1 | Network traffic monitored | ☐ Yes ☐ No | |
| 9.1.2 | NetFlow/IPFIX collection enabled | ☐ Yes ☐ No | |
| 9.1.3 | Baseline traffic patterns established | ☐ Yes ☐ No | |
| 9.1.4 | Anomaly detection configured | ☐ Yes ☐ No | |
| 9.1.5 | Full packet capture available (if needed) | ☐ Yes ☐ No ☐ N/A | |

### 9.2 Logging and Alerting

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 9.2.1 | Network device logs collected centrally | ☐ Yes ☐ No | |
| 9.2.2 | Firewall logs collected | ☐ Yes ☐ No | |
| 9.2.3 | Alerts for security events | ☐ Yes ☐ No | |
| 9.2.4 | Integration with SIEM | ☐ Yes ☐ No | |
| 9.2.5 | Log retention meets requirements | ☐ Yes ☐ No | Retention: |

---

## Section 10: Encryption

| # | Control | Status | Notes |
|---|---------|--------|-------|
| 10.1 | TLS 1.2+ required for web traffic | ☐ Yes ☐ No | |
| 10.2 | Weak ciphers disabled | ☐ Yes ☐ No | |
| 10.3 | Perfect forward secrecy enabled | ☐ Yes ☐ No | |
| 10.4 | Valid certificates from trusted CAs | ☐ Yes ☐ No | |
| 10.5 | Certificate expiry monitored | ☐ Yes ☐ No | |
| 10.6 | Internal traffic encrypted where required | ☐ Yes ☐ No ☐ Partial | |

---

## Section 11: Assessment Summary

### 11.1 Findings

| # | Finding | Severity | Remediation |
|---|---------|----------|-------------|
| 1 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 2 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 3 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 4 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |
| 5 | | ☐ Critical ☐ High ☐ Medium ☐ Low | |

### 11.2 Recommendations

| Priority | Recommendation | Owner | Target Date |
|----------|----------------|-------|-------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

### 11.3 Overall Assessment

☐ **Satisfactory** - Network security controls meet requirements
☐ **Needs Improvement** - Address findings within defined timeframe
☐ **Unsatisfactory** - Significant gaps require immediate attention

---

## Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Assessor | | | |
| Network Manager | | | |
| Security Manager | | | |

---

[Back to Checklists](./README.md) | [Back to Home](../README.md)

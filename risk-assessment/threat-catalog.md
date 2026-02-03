# Threat Catalog

A comprehensive catalog of information security threats for use in risk assessments, threat modeling, and security planning.

---

## Document Control

| Field | Details |
|-------|---------|
| **Version** | [VERSION] |
| **Last Updated** | [DATE] |
| **Owner** | [ROLE - e.g., IT Security Manager] |
| **Review Frequency** | Annual or after significant threat landscape changes |
| **Classification** | Internal |

---

## How to Use This Catalog

1. **Risk Assessments** - Use as a reference when identifying threats to assets and processes
2. **Threat Modeling** - Apply relevant threats to systems and applications
3. **Security Planning** - Prioritize controls based on applicable threats
4. **Awareness Training** - Educate staff about relevant threats
5. **Incident Preparation** - Develop playbooks for high-priority threats

---

## Business Process Context

**Critical Principle:** Threats should be evaluated in the context of the business processes they could impact. A threat to a system supporting a critical revenue-generating process has different risk implications than the same threat to a non-critical system.

### Why Process Context Matters

- The same technical threat can have vastly different business impacts depending on which processes are affected
- Recovery priorities should be based on process criticality, not just system importance
- Control investments should protect the most critical business processes first
- Incident response priorities depend on understanding which processes are at risk

### Business Impact Analysis (BIA) Integration

**Before using this threat catalog, ensure you have:**

1. **Identified Critical Business Processes**
   - Revenue-generating processes
   - Customer-facing processes
   - Regulatory/compliance processes
   - Operational support processes

2. **Mapped Systems to Processes**
   - Which systems support each process?
   - What are the dependencies between systems?
   - Which data is required for each process?

3. **Determined Process Criticality**
   - Recovery Time Objective (RTO) for each process
   - Recovery Point Objective (RPO) for data
   - Maximum Tolerable Downtime (MTD)
   - Financial impact of downtime

### Process-to-System Mapping Template

Use this structure to map your systems to business processes before assessing threats:

| Business Process | Criticality | Supporting Systems | Data Dependencies | RTO | RPO |
|------------------|-------------|-------------------|-------------------|-----|-----|
| [Process 1] | Critical | [System A, System B] | [Customer DB, Orders] | 4 hrs | 1 hr |
| [Process 2] | High | [System C] | [Inventory data] | 24 hrs | 4 hrs |
| [Process 3] | Medium | [System D, System E] | [Reports, Analytics] | 72 hrs | 24 hrs |
| [Process 4] | Low | [System F] | [Archives] | 1 week | 1 week |

### Process Criticality Levels

| Level | Definition | Examples | Typical RTO |
|-------|------------|----------|-------------|
| **Critical** | Immediate and severe impact to revenue, safety, or legal compliance if unavailable | Payment processing, Emergency services, Trading systems | < 4 hours |
| **High** | Significant business impact; operations severely degraded | Order management, Customer service, Core manufacturing | 4-24 hours |
| **Medium** | Moderate impact; business can function with workarounds | Reporting, HR systems, Internal communications | 24-72 hours |
| **Low** | Minimal immediate impact; inconvenience rather than disruption | Archives, Development environments, Training systems | 72+ hours |

### Contextualizing Threat Impact

When assessing threats from this catalog against your organization:

**Step 1:** Identify which systems could be affected by the threat

**Step 2:** Map those systems to business processes using your BIA

**Step 3:** Adjust the impact rating based on process criticality:

| Base Impact | Critical Process | High Process | Medium Process | Low Process |
|-------------|------------------|--------------|----------------|-------------|
| 5 - Catastrophic | 5 | 5 | 4 | 3 |
| 4 - Major | 5 | 4 | 3 | 2 |
| 3 - Moderate | 4 | 3 | 3 | 2 |
| 2 - Minor | 3 | 2 | 2 | 1 |
| 1 - Negligible | 2 | 1 | 1 | 1 |

**Example:**
- Ransomware (Base Impact: 5) affecting a system supporting a **Critical** process = Impact 5
- Same ransomware affecting a system supporting only **Low** processes = Impact 3

### Process-Based Threat Prioritization

When reviewing threats, consider:

| Question | Implication |
|----------|-------------|
| Which of our critical processes could this threat disrupt? | Determines true business impact |
| How many processes depend on the targeted systems? | Identifies concentration risk |
| Do we have manual workarounds for affected processes? | Affects actual downtime impact |
| What's the recovery complexity for affected processes? | Influences RTO achievability |
| Are there upstream/downstream process dependencies? | Reveals cascade effects |

### Single Points of Failure

Identify systems that are:
- The sole support for a critical process
- Required by multiple critical processes
- Without viable manual workarounds
- Difficult to recover quickly

These systems warrant elevated threat concern regardless of the base threat rating.

---

### Threat Rating Scale

| Rating | Likelihood | Description |
|--------|------------|-------------|
| 5 | Almost Certain | Expected to occur multiple times per year |
| 4 | Likely | Expected to occur at least once per year |
| 3 | Possible | Could occur within 1-3 years |
| 2 | Unlikely | Could occur within 3-5 years |
| 1 | Rare | Unlikely to occur within 5 years |

| Rating | Impact | Description |
|--------|--------|-------------|
| 5 | Catastrophic | Existential threat to organization |
| 4 | Major | Significant financial loss, regulatory action, major breach |
| 3 | Moderate | Notable disruption, contained breach, material cost |
| 2 | Minor | Limited disruption, minimal cost |
| 1 | Negligible | No significant impact |

---

## 1. Cyber Attack Threats

### 1.1 Malware

| Threat ID | T-MAL-001 |
|-----------|-----------|
| **Threat Name** | Ransomware |
| **Category** | Malware |
| **Description** | Malicious software that encrypts data and demands payment for decryption keys. May also exfiltrate data before encryption (double extortion). |
| **Threat Actor** | Organized crime, nation-states, hacktivists |
| **Attack Vector** | Phishing emails, exploited vulnerabilities, RDP compromise, supply chain |
| **Target Assets** | Servers, workstations, backups, file shares, databases |
| **Potential Impact** | Business disruption, data loss, financial loss, reputational damage |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 5 - Catastrophic |
| **MITRE ATT&CK** | T1486 (Data Encrypted for Impact) |
| **Example Controls** | EDR, backups, network segmentation, email filtering, patch management |

---

| Threat ID | T-MAL-002 |
|-----------|-----------|
| **Threat Name** | Banking Trojan |
| **Category** | Malware |
| **Description** | Malware designed to steal financial credentials, intercept transactions, or manipulate banking sessions. |
| **Threat Actor** | Organized crime |
| **Attack Vector** | Phishing emails, malicious downloads, compromised websites |
| **Target Assets** | Workstations, browsers, financial applications |
| **Potential Impact** | Financial fraud, credential theft |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1185 (Browser Session Hijacking) |
| **Example Controls** | EDR, web filtering, transaction verification, MFA |

---

| Threat ID | T-MAL-003 |
|-----------|-----------|
| **Threat Name** | Remote Access Trojan (RAT) |
| **Category** | Malware |
| **Description** | Malware providing persistent remote access to compromised systems, enabling surveillance, data theft, and further attacks. |
| **Threat Actor** | Nation-states, organized crime, corporate espionage |
| **Attack Vector** | Spear phishing, watering hole attacks, supply chain |
| **Target Assets** | Workstations, servers, executive devices |
| **Potential Impact** | Data exfiltration, persistent access, espionage |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1219 (Remote Access Software) |
| **Example Controls** | EDR, network monitoring, application whitelisting |

---

| Threat ID | T-MAL-004 |
|-----------|-----------|
| **Threat Name** | Cryptominer |
| **Category** | Malware |
| **Description** | Malware that uses system resources to mine cryptocurrency without authorization. |
| **Threat Actor** | Opportunistic attackers, organized crime |
| **Attack Vector** | Exploited vulnerabilities, compromised containers, malicious scripts |
| **Target Assets** | Servers, cloud instances, containers, workstations |
| **Potential Impact** | Resource consumption, increased costs, performance degradation |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 2 - Minor |
| **MITRE ATT&CK** | T1496 (Resource Hijacking) |
| **Example Controls** | Vulnerability management, container security, resource monitoring |

---

| Threat ID | T-MAL-005 |
|-----------|-----------|
| **Threat Name** | Wiper Malware |
| **Category** | Malware |
| **Description** | Destructive malware designed to permanently destroy data with no recovery mechanism. |
| **Threat Actor** | Nation-states, hacktivists |
| **Attack Vector** | Supply chain, exploited vulnerabilities, insider access |
| **Target Assets** | Servers, workstations, storage systems, backups |
| **Potential Impact** | Permanent data loss, business destruction |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 5 - Catastrophic |
| **MITRE ATT&CK** | T1485 (Data Destruction) |
| **Example Controls** | Offline backups, network segmentation, EDR |

---

| Threat ID | T-MAL-006 |
|-----------|-----------|
| **Threat Name** | Spyware/Keylogger |
| **Category** | Malware |
| **Description** | Software that secretly monitors user activity, captures keystrokes, screenshots, or other sensitive information. |
| **Threat Actor** | Organized crime, corporate espionage, stalkers |
| **Attack Vector** | Phishing, bundled software, physical access |
| **Target Assets** | Workstations, mobile devices |
| **Potential Impact** | Credential theft, privacy violation, data exfiltration |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1056 (Input Capture) |
| **Example Controls** | EDR, application control, security awareness |

---

### 1.2 Social Engineering

| Threat ID | T-SOC-001 |
|-----------|-----------|
| **Threat Name** | Phishing |
| **Category** | Social Engineering |
| **Description** | Fraudulent emails designed to trick recipients into revealing credentials, clicking malicious links, or downloading malware. |
| **Threat Actor** | Organized crime, opportunistic attackers, nation-states |
| **Attack Vector** | Email |
| **Target Assets** | Users, credentials, workstations |
| **Potential Impact** | Credential compromise, malware infection, data breach |
| **Base Likelihood** | 5 - Almost Certain |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1566 (Phishing) |
| **Example Controls** | Email filtering, security awareness training, MFA, phishing simulations |

---

| Threat ID | T-SOC-002 |
|-----------|-----------|
| **Threat Name** | Spear Phishing |
| **Category** | Social Engineering |
| **Description** | Targeted phishing attacks using personalized content to increase effectiveness against specific individuals or organizations. |
| **Threat Actor** | Nation-states, organized crime, corporate espionage |
| **Attack Vector** | Email, social media, messaging platforms |
| **Target Assets** | Executives, finance staff, IT administrators, specific employees |
| **Potential Impact** | Credential compromise, targeted malware, data breach |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1566.001 (Spearphishing Attachment) |
| **Example Controls** | Advanced email security, executive protection, security awareness |

---

| Threat ID | T-SOC-003 |
|-----------|-----------|
| **Threat Name** | Business Email Compromise (BEC) |
| **Category** | Social Engineering |
| **Description** | Attacks where criminals impersonate executives or vendors to trick employees into making fraudulent wire transfers or sharing sensitive data. |
| **Threat Actor** | Organized crime |
| **Attack Vector** | Email spoofing, account compromise, domain impersonation |
| **Target Assets** | Finance department, executives, accounts payable |
| **Potential Impact** | Financial fraud (often $100K+), data exposure |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1534 (Internal Spearphishing) |
| **Example Controls** | Payment verification procedures, DMARC, executive awareness training |

---

| Threat ID | T-SOC-004 |
|-----------|-----------|
| **Threat Name** | Vishing (Voice Phishing) |
| **Category** | Social Engineering |
| **Description** | Phone-based social engineering to extract sensitive information, credentials, or convince victims to take harmful actions. |
| **Threat Actor** | Organized crime, scammers |
| **Attack Vector** | Phone calls, voicemail |
| **Target Assets** | Help desk, employees, customers |
| **Potential Impact** | Credential disclosure, unauthorized access, financial fraud |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1566 (Phishing) |
| **Example Controls** | Verification procedures, security awareness, callback policies |

---

| Threat ID | T-SOC-005 |
|-----------|-----------|
| **Threat Name** | Pretexting |
| **Category** | Social Engineering |
| **Description** | Creating a fabricated scenario to manipulate victims into providing information or access they wouldn't normally give. |
| **Threat Actor** | Social engineers, corporate espionage, organized crime |
| **Attack Vector** | Phone, email, in-person |
| **Target Assets** | Employees, help desk, reception |
| **Potential Impact** | Information disclosure, unauthorized access |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1598 (Phishing for Information) |
| **Example Controls** | Verification procedures, security awareness, need-to-know policies |

---

| Threat ID | T-SOC-006 |
|-----------|-----------|
| **Threat Name** | Baiting |
| **Category** | Social Engineering |
| **Description** | Leaving malware-infected physical media (USB drives, CDs) or creating enticing digital downloads to trick victims. |
| **Threat Actor** | Organized crime, nation-states, penetration testers |
| **Attack Vector** | Physical media, malicious downloads |
| **Target Assets** | Workstations, curious employees |
| **Potential Impact** | Malware infection, network compromise |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1091 (Replication Through Removable Media) |
| **Example Controls** | USB controls, security awareness, endpoint protection |

---

### 1.3 Network Attacks

| Threat ID | T-NET-001 |
|-----------|-----------|
| **Threat Name** | Distributed Denial of Service (DDoS) |
| **Category** | Network Attack |
| **Description** | Overwhelming systems, networks, or applications with traffic to cause service unavailability. |
| **Threat Actor** | Hacktivists, competitors, extortionists, nation-states |
| **Attack Vector** | Botnets, amplification attacks, application-layer attacks |
| **Target Assets** | Web applications, networks, DNS, APIs |
| **Potential Impact** | Service outage, revenue loss, reputational damage |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1498 (Network Denial of Service) |
| **Example Controls** | DDoS protection services, CDN, rate limiting, redundancy |

---

| Threat ID | T-NET-002 |
|-----------|-----------|
| **Threat Name** | Man-in-the-Middle (MitM) |
| **Category** | Network Attack |
| **Description** | Intercepting communications between two parties to eavesdrop or modify data in transit. |
| **Threat Actor** | Organized crime, nation-states, malicious insiders |
| **Attack Vector** | Rogue Wi-Fi, ARP spoofing, DNS hijacking, compromised routers |
| **Target Assets** | Network communications, credentials, sensitive data |
| **Potential Impact** | Data interception, credential theft, session hijacking |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1557 (Adversary-in-the-Middle) |
| **Example Controls** | TLS/encryption, certificate pinning, network monitoring |

---

| Threat ID | T-NET-003 |
|-----------|-----------|
| **Threat Name** | DNS Attacks |
| **Category** | Network Attack |
| **Description** | Attacks targeting DNS infrastructure including cache poisoning, hijacking, or amplification. |
| **Threat Actor** | Nation-states, organized crime |
| **Attack Vector** | DNS server compromise, cache poisoning, registrar compromise |
| **Target Assets** | DNS infrastructure, domain names, web traffic |
| **Potential Impact** | Traffic redirection, service disruption, phishing enablement |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1584.002 (DNS Server) |
| **Example Controls** | DNSSEC, DNS monitoring, registrar security, redundant DNS |

---

| Threat ID | T-NET-004 |
|-----------|-----------|
| **Threat Name** | Network Intrusion |
| **Category** | Network Attack |
| **Description** | Unauthorized access to internal networks through exploitation of perimeter defenses or lateral movement. |
| **Threat Actor** | Nation-states, organized crime, hacktivists |
| **Attack Vector** | Vulnerability exploitation, credential theft, VPN compromise |
| **Target Assets** | Network infrastructure, internal systems, data |
| **Potential Impact** | Data breach, persistent access, lateral movement |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1133 (External Remote Services) |
| **Example Controls** | Firewalls, IDS/IPS, network segmentation, zero trust |

---

### 1.4 Web Application Attacks

| Threat ID | T-WEB-001 |
|-----------|-----------|
| **Threat Name** | SQL Injection |
| **Category** | Web Application Attack |
| **Description** | Injecting malicious SQL code through application inputs to access, modify, or delete database data. |
| **Threat Actor** | Hackers, organized crime, script kiddies |
| **Attack Vector** | Web forms, URL parameters, APIs |
| **Target Assets** | Databases, web applications, customer data |
| **Potential Impact** | Data breach, data manipulation, system compromise |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1190 (Exploit Public-Facing Application) |
| **Example Controls** | Input validation, parameterized queries, WAF, code review |

---

| Threat ID | T-WEB-002 |
|-----------|-----------|
| **Threat Name** | Cross-Site Scripting (XSS) |
| **Category** | Web Application Attack |
| **Description** | Injecting malicious scripts into web pages viewed by other users to steal data or perform actions on their behalf. |
| **Threat Actor** | Hackers, organized crime |
| **Attack Vector** | User input fields, URL parameters, stored content |
| **Target Assets** | Web applications, user sessions, customer data |
| **Potential Impact** | Session hijacking, credential theft, malware distribution |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1059.007 (JavaScript) |
| **Example Controls** | Input validation, output encoding, CSP, WAF |

---

| Threat ID | T-WEB-003 |
|-----------|-----------|
| **Threat Name** | API Attacks |
| **Category** | Web Application Attack |
| **Description** | Exploiting vulnerabilities in APIs including authentication bypass, injection, and excessive data exposure. |
| **Threat Actor** | Hackers, organized crime, competitors |
| **Attack Vector** | API endpoints, mobile apps, third-party integrations |
| **Target Assets** | APIs, backend systems, customer data |
| **Potential Impact** | Data breach, unauthorized access, service abuse |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1190 (Exploit Public-Facing Application) |
| **Example Controls** | API gateway, authentication, rate limiting, input validation |

---

| Threat ID | T-WEB-004 |
|-----------|-----------|
| **Threat Name** | Server-Side Request Forgery (SSRF) |
| **Category** | Web Application Attack |
| **Description** | Tricking servers into making requests to unintended locations, potentially accessing internal resources or cloud metadata. |
| **Threat Actor** | Hackers, researchers |
| **Attack Vector** | Web applications with URL fetching functionality |
| **Target Assets** | Internal services, cloud metadata, databases |
| **Potential Impact** | Internal network access, credential theft, data breach |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1190 (Exploit Public-Facing Application) |
| **Example Controls** | Input validation, network segmentation, metadata protection |

---

### 1.5 Identity and Access Attacks

| Threat ID | T-IAM-001 |
|-----------|-----------|
| **Threat Name** | Credential Stuffing |
| **Category** | Identity Attack |
| **Description** | Using stolen username/password combinations from other breaches to attempt access to accounts. |
| **Threat Actor** | Organized crime, opportunistic attackers |
| **Attack Vector** | Login pages, APIs, automated tools |
| **Target Assets** | User accounts, customer portals, employee systems |
| **Potential Impact** | Account takeover, data breach, fraud |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1110.004 (Credential Stuffing) |
| **Example Controls** | MFA, breach monitoring, rate limiting, CAPTCHA |

---

| Threat ID | T-IAM-002 |
|-----------|-----------|
| **Threat Name** | Brute Force Attack |
| **Category** | Identity Attack |
| **Description** | Systematically attempting password combinations to gain unauthorized access. |
| **Threat Actor** | Hackers, automated tools |
| **Attack Vector** | Login pages, SSH, RDP, APIs |
| **Target Assets** | User accounts, administrative accounts, servers |
| **Potential Impact** | Account compromise, system access |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1110 (Brute Force) |
| **Example Controls** | Account lockout, MFA, strong passwords, monitoring |

---

| Threat ID | T-IAM-003 |
|-----------|-----------|
| **Threat Name** | Password Spraying |
| **Category** | Identity Attack |
| **Description** | Attempting common passwords against many accounts to avoid lockout detection. |
| **Threat Actor** | Organized crime, nation-states |
| **Attack Vector** | Authentication endpoints, cloud services |
| **Target Assets** | User accounts, especially privileged accounts |
| **Potential Impact** | Account compromise, initial access for further attacks |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1110.003 (Password Spraying) |
| **Example Controls** | MFA, password policies, monitoring, conditional access |

---

| Threat ID | T-IAM-004 |
|-----------|-----------|
| **Threat Name** | Session Hijacking |
| **Category** | Identity Attack |
| **Description** | Stealing or manipulating session tokens to impersonate authenticated users. |
| **Threat Actor** | Hackers, malware |
| **Attack Vector** | XSS, network interception, malware |
| **Target Assets** | User sessions, web applications |
| **Potential Impact** | Account takeover, unauthorized actions |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 3 - Moderate |
| **MITRE ATT&CK** | T1185 (Browser Session Hijacking) |
| **Example Controls** | Secure cookies, session management, TLS |

---

| Threat ID | T-IAM-005 |
|-----------|-----------|
| **Threat Name** | MFA Bypass/Fatigue |
| **Category** | Identity Attack |
| **Description** | Techniques to bypass MFA including SIM swapping, push notification fatigue, or real-time phishing. |
| **Threat Actor** | Organized crime, sophisticated attackers |
| **Attack Vector** | Social engineering, technical exploitation |
| **Target Assets** | MFA-protected accounts, especially privileged |
| **Potential Impact** | Account compromise despite MFA |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1111 (Multi-Factor Authentication Interception) |
| **Example Controls** | Phishing-resistant MFA, number matching, user education |

---

### 1.6 Supply Chain Attacks

| Threat ID | T-SUP-001 |
|-----------|-----------|
| **Threat Name** | Software Supply Chain Attack |
| **Category** | Supply Chain |
| **Description** | Compromising software development or distribution processes to inject malicious code into legitimate software. |
| **Threat Actor** | Nation-states, sophisticated organized crime |
| **Attack Vector** | Compromised build systems, dependencies, updates |
| **Target Assets** | Software, development infrastructure, end users |
| **Potential Impact** | Widespread compromise, persistent access |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 5 - Catastrophic |
| **MITRE ATT&CK** | T1195 (Supply Chain Compromise) |
| **Example Controls** | Vendor assessment, SBOM, integrity verification, monitoring |

---

| Threat ID | T-SUP-002 |
|-----------|-----------|
| **Threat Name** | Third-Party Data Breach |
| **Category** | Supply Chain |
| **Description** | Breach at a vendor, partner, or service provider exposing shared data or providing attack path. |
| **Threat Actor** | Varies (attackers target the third party) |
| **Attack Vector** | Third-party compromise |
| **Target Assets** | Data shared with third parties, connected systems |
| **Potential Impact** | Data breach, regulatory impact, reputational damage |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1199 (Trusted Relationship) |
| **Example Controls** | Vendor risk management, data minimization, monitoring |

---

| Threat ID | T-SUP-003 |
|-----------|-----------|
| **Threat Name** | Dependency Confusion |
| **Category** | Supply Chain |
| **Description** | Tricking package managers into downloading malicious packages by exploiting naming conventions. |
| **Threat Actor** | Hackers, researchers |
| **Attack Vector** | Package repositories, build processes |
| **Target Assets** | Development environments, CI/CD pipelines |
| **Potential Impact** | Code execution, backdoor installation |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1195.001 (Compromise Software Dependencies) |
| **Example Controls** | Private repositories, namespace protection, dependency scanning |

---

## 2. Physical Security Threats

| Threat ID | T-PHY-001 |
|-----------|-----------|
| **Threat Name** | Unauthorized Physical Access |
| **Category** | Physical Security |
| **Description** | Gaining physical access to facilities, data centers, or restricted areas without authorization. |
| **Threat Actor** | Criminals, competitors, social engineers |
| **Attack Vector** | Tailgating, stolen credentials, break-in |
| **Target Assets** | Facilities, servers, equipment, documents |
| **Potential Impact** | Data theft, equipment theft, sabotage |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **Example Controls** | Access controls, CCTV, security guards, visitor management |

---

| Threat ID | T-PHY-002 |
|-----------|-----------|
| **Threat Name** | Theft of Equipment |
| **Category** | Physical Security |
| **Description** | Theft of laptops, mobile devices, servers, or storage media containing sensitive data. |
| **Threat Actor** | Opportunistic thieves, targeted attackers |
| **Attack Vector** | Burglary, theft from vehicles, office theft |
| **Target Assets** | Laptops, phones, servers, backup media |
| **Potential Impact** | Data breach, financial loss, operational disruption |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | Encryption, physical locks, tracking, secure storage |

---

| Threat ID | T-PHY-003 |
|-----------|-----------|
| **Threat Name** | Dumpster Diving |
| **Category** | Physical Security |
| **Description** | Searching through discarded materials for sensitive information, documents, or media. |
| **Threat Actor** | Social engineers, competitors, identity thieves |
| **Attack Vector** | Trash, recycling bins, discarded equipment |
| **Target Assets** | Printed documents, discarded media, old equipment |
| **Potential Impact** | Information disclosure, identity theft, reconnaissance |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 2 - Minor |
| **Example Controls** | Shredding, secure disposal, clear desk policy |

---

| Threat ID | T-PHY-004 |
|-----------|-----------|
| **Threat Name** | Shoulder Surfing |
| **Category** | Physical Security |
| **Description** | Observing screens, keyboards, or documents to capture sensitive information. |
| **Threat Actor** | Social engineers, opportunistic observers |
| **Attack Vector** | Visual observation in public or office spaces |
| **Target Assets** | Credentials, sensitive data on screens |
| **Potential Impact** | Credential theft, information disclosure |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 2 - Minor |
| **Example Controls** | Privacy screens, awareness training, clean desk |

---

## 3. Insider Threats

| Threat ID | T-INS-001 |
|-----------|-----------|
| **Threat Name** | Malicious Insider |
| **Category** | Insider Threat |
| **Description** | Employee or contractor intentionally stealing data, sabotaging systems, or abusing access for personal gain. |
| **Threat Actor** | Disgruntled employees, financially motivated insiders, recruited insiders |
| **Attack Vector** | Legitimate access, elevated privileges |
| **Target Assets** | Sensitive data, intellectual property, systems |
| **Potential Impact** | Data theft, sabotage, fraud, competitive harm |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1078 (Valid Accounts) |
| **Example Controls** | Access controls, monitoring, DLP, background checks |

---

| Threat ID | T-INS-002 |
|-----------|-----------|
| **Threat Name** | Negligent Insider |
| **Category** | Insider Threat |
| **Description** | Employees unintentionally causing security incidents through carelessness, mistakes, or policy violations. |
| **Threat Actor** | Well-meaning employees |
| **Attack Vector** | Phishing susceptibility, misconfigurations, lost devices |
| **Target Assets** | All systems and data |
| **Potential Impact** | Data breach, system compromise, compliance violations |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | Training, technical controls, usable security, DLP |

---

| Threat ID | T-INS-003 |
|-----------|-----------|
| **Threat Name** | Privilege Abuse |
| **Category** | Insider Threat |
| **Description** | Using legitimate access rights to access data or perform actions beyond business need. |
| **Threat Actor** | Curious employees, malicious insiders |
| **Attack Vector** | Legitimate credentials with excessive access |
| **Target Assets** | Sensitive data, customer records, colleague information |
| **Potential Impact** | Privacy violations, data misuse, compliance breach |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | Least privilege, access monitoring, regular reviews |

---

| Threat ID | T-INS-004 |
|-----------|-----------|
| **Threat Name** | Departing Employee Data Theft |
| **Category** | Insider Threat |
| **Description** | Employees taking sensitive data, intellectual property, or customer lists when leaving the organization. |
| **Threat Actor** | Departing employees, especially to competitors |
| **Attack Vector** | Email, USB, cloud storage, personal devices |
| **Target Assets** | Intellectual property, customer data, trade secrets |
| **Potential Impact** | Competitive harm, IP loss, customer loss |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | DLP, offboarding process, monitoring, exit interviews |

---

## 4. Environmental and Natural Threats

| Threat ID | T-ENV-001 |
|-----------|-----------|
| **Threat Name** | Natural Disaster |
| **Category** | Environmental |
| **Description** | Earthquakes, floods, hurricanes, tornadoes, or other natural events causing facility damage or disruption. |
| **Threat Actor** | Nature |
| **Attack Vector** | N/A |
| **Target Assets** | Facilities, data centers, infrastructure |
| **Potential Impact** | Extended outage, data loss, facility destruction |
| **Base Likelihood** | Varies by location |
| **Base Impact** | 5 - Catastrophic |
| **Example Controls** | Geographic redundancy, DR planning, insurance |

---

| Threat ID | T-ENV-002 |
|-----------|-----------|
| **Threat Name** | Fire |
| **Category** | Environmental |
| **Description** | Fire damage to facilities, equipment, or data centers. |
| **Threat Actor** | Accident, arson, environmental |
| **Attack Vector** | Electrical, environmental, deliberate |
| **Target Assets** | Facilities, equipment, data |
| **Potential Impact** | Equipment destruction, data loss, business disruption |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 4 - Major |
| **Example Controls** | Fire suppression, detection, offsite backups, insurance |

---

| Threat ID | T-ENV-003 |
|-----------|-----------|
| **Threat Name** | Power Failure |
| **Category** | Environmental |
| **Description** | Loss of electrical power affecting systems, data centers, or facilities. |
| **Threat Actor** | Utility issues, weather, infrastructure failure |
| **Attack Vector** | N/A |
| **Target Assets** | All powered systems |
| **Potential Impact** | Service outage, data corruption, equipment damage |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | UPS, generators, redundant power, cloud services |

---

| Threat ID | T-ENV-004 |
|-----------|-----------|
| **Threat Name** | HVAC Failure |
| **Category** | Environmental |
| **Description** | Failure of cooling systems leading to equipment overheating and failure. |
| **Threat Actor** | Equipment failure, maintenance issues |
| **Attack Vector** | N/A |
| **Target Assets** | Data centers, server rooms |
| **Potential Impact** | Equipment failure, data loss, service outage |
| **Base Likelihood** | 2 - Unlikely |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | Redundant cooling, monitoring, maintenance, cloud services |

---

## 5. Cloud and Third-Party Threats

| Threat ID | T-CLD-001 |
|-----------|-----------|
| **Threat Name** | Cloud Misconfiguration |
| **Category** | Cloud Security |
| **Description** | Security weaknesses from improperly configured cloud services, storage, or access controls. |
| **Threat Actor** | Internal (misconfiguration), external (exploitation) |
| **Attack Vector** | Exposed storage, overly permissive access, default settings |
| **Target Assets** | Cloud resources, data, applications |
| **Potential Impact** | Data exposure, unauthorized access, compliance violations |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | T1530 (Data from Cloud Storage) |
| **Example Controls** | CSPM, configuration standards, regular audits |

---

| Threat ID | T-CLD-002 |
|-----------|-----------|
| **Threat Name** | Cloud Account Compromise |
| **Category** | Cloud Security |
| **Description** | Unauthorized access to cloud management accounts enabling resource manipulation or data access. |
| **Threat Actor** | Nation-states, organized crime |
| **Attack Vector** | Credential theft, phishing, misconfiguration |
| **Target Assets** | Cloud infrastructure, data, applications |
| **Potential Impact** | Full environment compromise, data breach, resource abuse |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 5 - Catastrophic |
| **MITRE ATT&CK** | T1078.004 (Cloud Accounts) |
| **Example Controls** | MFA, privileged access management, monitoring, least privilege |

---

| Threat ID | T-CLD-003 |
|-----------|-----------|
| **Threat Name** | Cloud Service Provider Outage |
| **Category** | Cloud Security |
| **Description** | Service unavailability due to cloud provider issues affecting dependent systems. |
| **Threat Actor** | N/A (provider issue) |
| **Attack Vector** | N/A |
| **Target Assets** | Cloud-hosted applications and data |
| **Potential Impact** | Service disruption, business impact |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | Multi-region, multi-cloud, DR planning, SLAs |

---

| Threat ID | T-CLD-004 |
|-----------|-----------|
| **Threat Name** | Shadow IT / Unsanctioned Cloud |
| **Category** | Cloud Security |
| **Description** | Employees using unauthorized cloud services to store or process company data. |
| **Threat Actor** | Well-meaning employees |
| **Attack Vector** | Personal accounts, free services |
| **Target Assets** | Corporate data in uncontrolled environments |
| **Potential Impact** | Data exposure, compliance violations, lack of visibility |
| **Base Likelihood** | 4 - Likely |
| **Base Impact** | 3 - Moderate |
| **Example Controls** | CASB, approved alternatives, training, DLP |

---

## 6. Emerging and Advanced Threats

| Threat ID | T-ADV-001 |
|-----------|-----------|
| **Threat Name** | AI-Powered Attacks |
| **Category** | Emerging Threat |
| **Description** | Use of artificial intelligence to enhance attack capabilities, including deepfakes, automated attacks, and evasion. |
| **Threat Actor** | Nation-states, organized crime |
| **Attack Vector** | Enhanced phishing, voice cloning, automated exploitation |
| **Target Assets** | All systems and people |
| **Potential Impact** | More effective attacks, harder detection |
| **Base Likelihood** | 3 - Possible (increasing) |
| **Base Impact** | 4 - Major |
| **Example Controls** | AI-based defenses, verification procedures, awareness |

---

| Threat ID | T-ADV-002 |
|-----------|-----------|
| **Threat Name** | Zero-Day Exploitation |
| **Category** | Advanced Threat |
| **Description** | Exploitation of previously unknown vulnerabilities before patches are available. |
| **Threat Actor** | Nation-states, sophisticated organized crime |
| **Attack Vector** | Targeted attacks using unknown vulnerabilities |
| **Target Assets** | Any vulnerable systems |
| **Potential Impact** | System compromise, data breach |
| **Base Likelihood** | 2 - Unlikely (for most organizations) |
| **Base Impact** | 5 - Catastrophic |
| **MITRE ATT&CK** | T1190 (Exploit Public-Facing Application) |
| **Example Controls** | Defense in depth, monitoring, EDR, network segmentation |

---

| Threat ID | T-ADV-003 |
|-----------|-----------|
| **Threat Name** | Advanced Persistent Threat (APT) |
| **Category** | Advanced Threat |
| **Description** | Sophisticated, long-term targeted attacks by well-resourced adversaries seeking persistent access. |
| **Threat Actor** | Nation-states, state-sponsored groups |
| **Attack Vector** | Multi-stage attacks, custom malware, social engineering |
| **Target Assets** | Intellectual property, strategic information, infrastructure |
| **Potential Impact** | Long-term compromise, espionage, sabotage |
| **Base Likelihood** | Varies by sector/profile |
| **Base Impact** | 5 - Catastrophic |
| **MITRE ATT&CK** | Multiple TTPs |
| **Example Controls** | Threat intelligence, advanced detection, incident response |

---

| Threat ID | T-ADV-004 |
|-----------|-----------|
| **Threat Name** | IoT/OT Attacks |
| **Category** | Emerging Threat |
| **Description** | Attacks targeting Internet of Things devices or operational technology systems. |
| **Threat Actor** | Nation-states, hacktivists, organized crime |
| **Attack Vector** | Default credentials, unpatched vulnerabilities, network exposure |
| **Target Assets** | IoT devices, industrial control systems, building systems |
| **Potential Impact** | Physical damage, safety issues, disruption |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **MITRE ATT&CK** | Multiple ICS/OT TTPs |
| **Example Controls** | Network segmentation, inventory, monitoring, patching |

---

## 7. Compliance and Legal Threats

| Threat ID | T-LEG-001 |
|-----------|-----------|
| **Threat Name** | Regulatory Non-Compliance |
| **Category** | Compliance |
| **Description** | Failure to meet regulatory requirements resulting in fines, sanctions, or operational restrictions. |
| **Threat Actor** | Internal (failure to comply) |
| **Attack Vector** | N/A |
| **Target Assets** | Organization, specific business units |
| **Potential Impact** | Fines, legal action, operational restrictions, reputational damage |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **Example Controls** | Compliance program, audits, monitoring, training |

---

| Threat ID | T-LEG-002 |
|-----------|-----------|
| **Threat Name** | Data Privacy Violation |
| **Category** | Compliance |
| **Description** | Unauthorized processing, disclosure, or mishandling of personal data violating privacy regulations. |
| **Threat Actor** | Internal (negligence), external (breach) |
| **Attack Vector** | Process failures, breaches, unauthorized access |
| **Target Assets** | Personal data, customer information |
| **Potential Impact** | Regulatory fines (up to 4% revenue under GDPR), lawsuits, reputation |
| **Base Likelihood** | 3 - Possible |
| **Base Impact** | 4 - Major |
| **Example Controls** | Privacy program, DPIAs, data minimization, consent management |

---

## Appendix A: Threat Category Summary

| Category | Count | Highest Risk Threats |
|----------|-------|---------------------|
| Malware | 6 | Ransomware, RAT |
| Social Engineering | 6 | Phishing, BEC, Spear Phishing |
| Network Attacks | 4 | Network Intrusion, DDoS |
| Web Application | 4 | SQL Injection, API Attacks |
| Identity/Access | 5 | Password Spraying, Credential Stuffing |
| Supply Chain | 3 | Software Supply Chain, Third-Party Breach |
| Physical Security | 4 | Unauthorized Access, Equipment Theft |
| Insider Threats | 4 | Malicious Insider, Negligent Insider |
| Environmental | 4 | Natural Disaster, Fire |
| Cloud | 4 | Misconfiguration, Account Compromise |
| Emerging/Advanced | 4 | APT, Zero-Day |
| Compliance/Legal | 2 | Privacy Violation, Non-Compliance |

---

## Appendix B: MITRE ATT&CK Mapping

| Threat ID | ATT&CK Technique |
|-----------|------------------|
| T-MAL-001 | T1486 - Data Encrypted for Impact |
| T-MAL-003 | T1219 - Remote Access Software |
| T-MAL-004 | T1496 - Resource Hijacking |
| T-MAL-005 | T1485 - Data Destruction |
| T-MAL-006 | T1056 - Input Capture |
| T-SOC-001 | T1566 - Phishing |
| T-SOC-002 | T1566.001 - Spearphishing Attachment |
| T-SOC-003 | T1534 - Internal Spearphishing |
| T-NET-001 | T1498 - Network Denial of Service |
| T-NET-002 | T1557 - Adversary-in-the-Middle |
| T-IAM-001 | T1110.004 - Credential Stuffing |
| T-IAM-002 | T1110 - Brute Force |
| T-IAM-003 | T1110.003 - Password Spraying |
| T-SUP-001 | T1195 - Supply Chain Compromise |
| T-SUP-002 | T1199 - Trusted Relationship |
| T-CLD-001 | T1530 - Data from Cloud Storage |
| T-CLD-002 | T1078.004 - Cloud Accounts |

---

## Appendix C: Industry-Specific Threat Considerations

### Financial Services
- BEC and wire fraud (elevated risk)
- ATM/payment card attacks
- Regulatory compliance (PCI DSS, SOX)

### Healthcare
- Medical device vulnerabilities
- Patient data theft
- Ransomware (elevated impact)
- HIPAA compliance

### Manufacturing
- Industrial espionage
- OT/ICS attacks
- Supply chain disruption

### Retail
- Point-of-sale malware
- E-commerce fraud
- Customer data theft
- PCI DSS compliance

### Government
- Nation-state targeting
- Espionage
- Critical infrastructure protection

---

## Appendix D: Process-Based Threat Analysis

### Common Business Process Categories

When conducting BIA and mapping threats, consider these common process categories:

#### Revenue-Generating Processes

| Process Type | Typical Systems | Key Threats | Priority |
|--------------|-----------------|-------------|----------|
| Sales/Order Processing | CRM, E-commerce, POS | Ransomware, DDoS, Payment fraud | Critical |
| Service Delivery | Core business applications | All availability threats | Critical |
| Billing/Invoicing | ERP, Billing systems | BEC, Data manipulation | Critical |
| Customer Onboarding | CRM, Identity verification | Account fraud, Data breach | High |

#### Customer-Facing Processes

| Process Type | Typical Systems | Key Threats | Priority |
|--------------|-----------------|-------------|----------|
| Customer Portal | Web applications, APIs | DDoS, Web attacks, Account takeover | Critical |
| Customer Support | Ticketing, CRM, Phone systems | Social engineering, Data exposure | High |
| Communication | Email, Messaging | Phishing, BEC, Spoofing | High |

#### Operational Processes

| Process Type | Typical Systems | Key Threats | Priority |
|--------------|-----------------|-------------|----------|
| Manufacturing/Production | OT/ICS, MES, SCADA | OT attacks, Ransomware, Insider | Critical |
| Supply Chain Management | SCM, Logistics, EDI | Third-party breach, BEC | High |
| Inventory Management | WMS, ERP | Data manipulation, Ransomware | Medium |
| Facilities Management | BMS, Access control | Physical threats, IoT attacks | Medium |

#### Support Processes

| Process Type | Typical Systems | Key Threats | Priority |
|--------------|-----------------|-------------|----------|
| Human Resources | HRIS, Payroll | Insider threat, Data breach | High |
| Finance/Accounting | ERP, Banking | BEC, Fraud, Insider | Critical |
| IT Operations | Infrastructure, Monitoring | All technical threats | High |
| Legal/Compliance | Document management | Data breach, Insider | Medium |

### Process Dependency Mapping

**Identify dependencies to understand cascade effects:**

```
[Customer Order Process]
    ├── Requires: E-commerce Platform
    │       ├── Requires: Payment Gateway (External)
    │       ├── Requires: Product Database
    │       └── Requires: Customer Database
    ├── Requires: Inventory System
    │       └── Requires: Warehouse Management
    ├── Triggers: Fulfillment Process
    │       ├── Requires: Shipping Integration (External)
    │       └── Requires: Inventory System
    └── Triggers: Billing Process
            ├── Requires: ERP
            └── Requires: Email System
```

### Threat-to-Process Impact Matrix

Use this matrix to map which threats most significantly impact each process type:

| Threat | Revenue | Customer-Facing | Operations | Support |
|--------|---------|-----------------|------------|---------|
| Ransomware | CRITICAL | CRITICAL | CRITICAL | HIGH |
| DDoS | CRITICAL | CRITICAL | MEDIUM | LOW |
| Data Breach | HIGH | CRITICAL | MEDIUM | HIGH |
| BEC/Fraud | CRITICAL | MEDIUM | MEDIUM | CRITICAL |
| Insider Threat | HIGH | MEDIUM | HIGH | HIGH |
| Third-Party Breach | HIGH | HIGH | HIGH | MEDIUM |
| Phishing | MEDIUM | HIGH | MEDIUM | HIGH |
| Power/Environmental | HIGH | HIGH | CRITICAL | MEDIUM |

### BIA-Driven Control Prioritization

**Invest in controls based on process criticality:**

| Process Criticality | Control Investment | Recovery Investment |
|--------------------|-------------------|---------------------|
| **Critical** | Maximum - Defense in depth, redundancy | Hot standby, automated failover |
| **High** | High - Multiple control layers | Warm standby, documented recovery |
| **Medium** | Standard - Baseline controls | Cold standby, backup restoration |
| **Low** | Basic - Essential controls only | Backup only, extended RTO acceptable |

### Questions for Process Owners

When conducting BIA interviews, ask:

1. **Process Identification**
   - What does your process do?
   - Who depends on the output of your process?
   - Whose output do you depend on?

2. **System Dependencies**
   - What systems are required to perform this process?
   - Are there manual workarounds if systems are unavailable?
   - How long can you operate manually?

3. **Data Dependencies**
   - What data is required for this process?
   - How current must the data be?
   - What happens if data is lost or corrupted?

4. **Impact Assessment**
   - What happens if this process stops for 1 hour? 4 hours? 1 day? 1 week?
   - What's the financial impact of downtime?
   - What's the regulatory/compliance impact?
   - What's the reputational impact?

5. **Recovery Requirements**
   - How quickly must this process be restored?
   - How much data loss is acceptable?
   - What's the minimum functionality needed?

### Linking BIA Results to Threat Assessment

**Process for integrating BIA with threat analysis:**

1. **Complete BIA first** - Understand process criticality before assessing threats
2. **Map systems to processes** - Know which systems support which processes
3. **Identify single points of failure** - Systems without redundancy supporting critical processes
4. **Apply threat catalog** - Assess each relevant threat against critical systems
5. **Contextualize impact** - Adjust threat impact based on process criticality
6. **Prioritize controls** - Invest in protecting critical process dependencies
7. **Plan recovery** - Ensure recovery capabilities match process RTOs

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [AUTHOR] | Initial release |

---

[Back to Risk Assessment](./README.md) | [Back to Home](../README.md)

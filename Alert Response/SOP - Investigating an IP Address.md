## Purpose
Internet Protocol (IP) addresses are common Indicators of Compromise (IoC) and observable artifacts in Security Operations Center (SOC) alerts and investigations.  The purpose of this SOP is to provide a structured and detailed approach for SOC analysts to investigate an IP address suspected of malicious or suspicious activity. This process ensures thorough analysis while maintaining operational security (OPSEC) and minimizing the risk of alerting threat actors.

## Scope
This SOP applies to all SOC analysts and security personnel tasked with investigating suspicious IP addresses. It covers:

- IP reputation analysis using both closed and open intelligence sources
- Identification of endpoints within the organization that may have communicated with the IP
- Examination of DNS resolutions and network logs
- Analysis of traffic patterns, including ports, protocols, and potential malware Command and Control (C2) activity
- Documentation and escalation of findings, including Business Impact Assessments (BIA) and blocking recommendations

Internal, RFC 1918 reserved addresses, or other internal IPs should be excluded from external threat analysis.

## Prerequisites
Before conducting an investigation, the following must be in place:

1. **Access to Approved Tools** – SOC analysts should use only approved internal and external threat intelligence platforms, WHOIS lookup services, and network forensic tools.
2. **Tracking Platform** – A case management or ticketing system must be available to document all investigative activities.
3. **Threat Intelligence Sources** – SOC analysts should have access to both closed (internal and paid threat intel feeds) and open (OSINT) sources.
4. **Network Traffic Logs** – Analysts must have access to network logs, DNS resolution logs, and Endpoint Detection and Response (EDR) platforms.
5. **Clear Escalation Paths** – Defined procedures for escalating findings to Cyber Threat Intelligence (CTI) and networking/IT teams for mitigation actions.

## Roles and Responsibilities

| Role                           | Responsibility                                                                                                                                                                                                                                                                                                                                    |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                    | Initiates and conducts the investigation following the defined procedure.<br>Documents findings in the tracking platform.<br>Ensures OPSEC by avoiding direct interaction with the suspicious IP.<br>Collaborates with the CTI team and IT teams as necessary.<br>Submits IPs determined to be malicious for tracking and blocking consideration. |
| SOC Manager                    | Oversees investigations to ensure consistency and thoroughness.<br>Approves blocking recommendations after Business Impact Assessment (BIA) review.                                                                                                                                                                                               |
| Cyber Threat Intelligence Team | Validates findings and provides additional threat context.<br>Updates internal threat intelligence repositories with relevant indicators.<br>Assists in making final determinations regarding IP reputation and risk level.                                                                                                                       |
| Networking and IT Teams        | Implements temporary or permanent IP blocking when necessary.<br>Assesses operational risks associated with blocking actions.<br>Provides additional network insights if needed.                                                                                                                                                                  |

## Workflow Diagram
[Insert visual diagram of the SOP workflow]

## Procedure Steps
### **Step 1: Create a Ticket in the Tracking Platform**

- If an investigation ticket does not exist, create one and assign it appropriately.
- Include in the ticket:
    - The suspicious IP
    - Initial alert source
    - Date and time of detection
    - Any relevant details from the initial report

### **Step 2: Perform Initial IP Research**

- **Check WHOIS and ARIN Registration:**
    - Use tools like WHOIS and ARIN to determine the organization, country, and ASN (Autonomous System Number) associated with the IP.
    - Record findings in the tracking system.
- **Check Threat Intelligence Feeds:**
    - Query internal and external threat intelligence sources for prior malicious activity associated with the IP.
    - Note any associations with known threat actor groups, botnets, or malware campaigns.
- **Check Open-Source Intelligence (OSINT):**
    - Search for the IP in threat databases like VirusTotal, AlienVault OTX, AbuseIPDB, and Shodan.
    - Document any historical malicious behavior or relevant threat reports.

### **Step 3: Investigate Internal Network Logs**

- **Identify Internal Communications:**
    - Query network logs and firewall data for any internal endpoints that have communicated with the IP.
    - Check if any DNS queries resolved to the suspicious IP.
    - Review logs for traffic patterns, including:
        - Ports and protocols used
        - Duration and frequency of connections
        - Data transfer volume
        - Encrypted or unencrypted communication
- Assess Possible Anonymization Techniques:
    - Identify if the IP is linked to VPNs, TOR nodes, or other anonymizing services.

### **Step 4: Assess Potential Threats and Malicious Activity**

- Determine if the IP is associated with:
    - Malware Command and Control (C2) traffic
    - Phishing campaigns
    - Brute-force attacks
    - Data exfiltration
    - Unauthorized remote access
- Examine Network Intrusion Detection logs, alerts, and rules to determine if the IP or traffic are associated with any known signatures.

### **Step 5: Conduct a Business Impact Assessment (BIA)**

- Ref:  [[PRO - Business Impact Assessment]]
- If the IP is determined to be malicious, conduct a BIA to assess:
    - The potential operational impact of blocking the IP.
    - Whether legitimate business services rely on communication with the IP.
    - If any dependencies exist that could be disrupted.

### **Step 6: Escalation and Mitigation Actions**

- If the BIA determines no significant business impact:
    - Submit the IP to the Cyber Threat Intelligence (CTI) team for tracking.
    - Request networking and/or IT teams to implement a temporary block.
- If the BIA determines business impact is possible
    - Escalate the case to the SOC Director for review and final decision.

### **Step 7: Final Reporting and Documentation**

- Update the investigation ticket with:
    - Summary of findings
    - Actions taken
    - Any recommended follow-up steps
- Close the case once mitigation is confirmed.
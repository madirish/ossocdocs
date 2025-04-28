## Purpose
The purpose of this SOP is to provide a structured methodology for Security Operations Center (SOC) analysts to investigate suspicious domain registrations. These domains may be associated with typosquatting, brand impersonation, phishing, malware distribution, or other malicious activities. The SOP ensures that thorough investigations are conducted to assess risk, identify threats, and determine appropriate mitigation actions.

## Scope
his SOP applies to SOC analysts responsible for monitoring, investigating, and responding to suspicious domain registrations. It includes domains detected via proactive monitoring, threat intelligence feeds, or reported by internal or external stakeholders.

## Prerequisites
- Access to domain investigation tools (WHOIS lookup, passive DNS databases, reverse IP lookup, domain reputation services, etc.)
- Open-source intelligence (OSINT) tools for domain analysis
- Threat Intelligence Platform (TIP) access
- Access to a secure sandbox environment for testing
- Threat exchange community memberships
- Logging and monitoring tools for internal network and email traffic analysis
- Knowledge of DNS, cryptographic certificates, and common hosting providers

## Roles and Responsibilities

| Role                          | Responsibility                                                                                                                                                                                                                                                                |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                   | Conduct domain investigations using open-source and proprietary tools.<br>Analyze DNS records, domain age, ownership transfers, and hosting infrastructure.<br>Identify potential threats and escalate as necessary.<br>Document findings and coordinate with relevant teams. |
| SOC Manager                   | Collect metrics for reporting.                                                                                                                                                                                                                                                |
| Threat Intelligence (TI) Team | Provide intelligence enrichment for suspicious domains.<br>Share findings with trusted threat intelligence communities.                                                                                                                                                       |
| Incident Response (IR) Team   | Assist in cases where the domain is linked to ongoing security incidents.<br>Support containment and mitigation actions.                                                                                                                                                      |
| Security Engineers            | Implement blocks at the network and email security layers if required.                                                                                                                                                                                                        |

## Workflow Diagram
[Insert visual diagram of the SOP workflow]

## Procedure Steps
### 1. **Domain Identification & Initial Review**
- Determine the source of the alert (automated monitoring, threat feed, user report, etc.).
- Validate if the domain is newly registered, recently modified, or flagged as suspicious in any way.
        
### 2. **WHOIS & DNS Analysis**
- Perform WHOIS lookup:
    - Identify domain registrar and assess its reputation.
    - Check registration and expiration dates.
    - Review domain ownership history and transfer records.
- Analyze DNS records:
    - Review A, MX, NS, TXT, and CNAME records.
    - Identify non-standard records that may indicate abuse (e.g., SPF/DKIM/DMARC misconfigurations).
    - Determine if the domain uses privacy protection services to hide ownership details.
        
### 3. **Infrastructure and Hosting Investigation**
- Identify the hosting provider and assess its reputation.
- Perform a reverse IP lookup to check for additional suspicious domains hosted on the same IP.
- Check for historical resolutions of the domain to identify prior malicious activity.
        
### 4. **Email & Web Service Analysis**
- Determine if the domain has active email services (MX records) and assess any associated email security configurations (SPF, DKIM, DMARC).
- Identify any web services associated with the domain and analyze their content.
- Use a sandbox to safely analyze the website for:
    - Credential harvesting pages
    - Malware distribution
    - Redirects to other domains
    - Embedded malicious content (e.g., JavaScript skimmers, exploit kits)
            
### 5. **Certificate & Encryption Analysis**
- Identify cryptographic certificates associated with the domain.
- Look for known fingerprints linked to malicious infrastructure.
- Analyze the certificate authority issuing the certificate and its legitimacy.
        
### 6. **Threat Intelligence Correlation**
- Search the Threat Intelligence Platform (TIP) for:
    - Historical reports of abuse.
    - Associated threat actors or malware campaigns.
- Query public and private threat exchanges for prior sightings.
- Investigate passive DNS databases for prior domain resolution activity.
        
### 7. **Network & Email Traffic Investigation**
- Check internal logs for:
    - Network traffic to or from the domain.
    - Email logs for any messages sent to or received from the domain.
- Investigate any anomalies or signs of prior compromise.
        
### 8. **Risk Assessment & Mitigation Actions**
- If the domain is determined to be malicious:
    - Report it to Domain Take Down services if applicable.
    - Block the domain at:
        - Firewall and web proxy layers
        - Email security gateway
        - Endpoint protection solutions
        - Internal DNS 
 - If the domain is suspicious but not conclusively malicious:
    - Continue monitoring for further activity.
    - Add it to a watchlist for ongoing threat tracking.
            
### 9. **Documentation & Reporting**
- Document all findings, including investigative steps and conclusions.
- Share intelligence with relevant internal teams and trusted external partners.
- Update threat intelligence repositories for future reference.
        
### 10. **Continuous Monitoring & Follow-Up**
- Reassess flagged domains periodically for new activity.
- Identify trends in suspicious domain registrations to enhance detection strategies.
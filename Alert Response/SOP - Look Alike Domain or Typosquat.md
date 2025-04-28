## Purpose
The purpose of this SOP is to provide a structured approach for the Threat Intelligence (TI) team, or the Security Operations Center (SOC), to identify, evaluate, and mitigate the risks associated with look-alike domains and typosquatting. These domains may be used for brand impersonation, credential harvesting, phishing campaigns, or other malicious activities. The SOP ensures a consistent and effective response to mitigate potential threats to the organization and its stakeholders.
## Scope
This SOP applies to all Threat Intelligence (TI) analysts, Security Operations Center (SOC) personnel, and Incident Response (IR) teams responsible for detecting, investigating, and responding to typosquatting and look-alike domains associated with the organization’s brand, products, and trademarks.
## Prerequisites
- Access to domain monitoring and threat intelligence platforms
- A maintained list of priority brands, product names, trademarks, and organizational keywords
- Access to domain investigation tools and services
- Knowledge of the organization's security infrastructure, including firewalls, web proxies, and email filtering systems
- Communication channels with Domain Take Down services and trusted threat intelligence sharing communities
## Roles and Responsibilities

| Role                             | Responsibility                                                                                                                                                                                                                                                                                                                   |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                      | Investigate if internal traffic or email activity is associated with the domain.<br>Recommend domain acquisition if brand protection services are available.<br>Perform a Business Impact Assessment (BIA) and escalate to IR if necessary.<br>Implement domain blocking at firewalls, web proxies, and email filtering systems. |
| SOC Manager                      | Gathering metrics and reporting.                                                                                                                                                                                                                                                                                                 |
| Threat Intel Analyst             | Monitor and analyze alerts related to look-alike domains.<br>Investigate detected domains using the Suspicious Domain Investigation SOP.<br>Determine if the domain is malicious and recommend mitigation steps.<br>Report findings to relevant stakeholders.                                                                    |
| Incident Response (IR) Team      | Assist in response actions for confirmed malicious domains.<br>Support evidence collection for domain takedown requests.                                                                                                                                                                                                         |
| Legal and Brand Protection Teams | Review and approve recommendations for domain acquisition.<br>Coordinate with external parties for legal enforcement actions.                                                                                                                                                                                                    |
| Trusted Intel Sharing Community  | Receive reports on typosquatting domains to prevent broader social engineering risks.                                                                                                                                                                                                                                            |

## Procedure Steps

### 1. **Detection & Alert Review**
- Monitor domain registration feeds and threat intelligence alerts for look-alike domains.
- Assess the similarity of detected domains to priority brands, product names, or trademarks.
### 2. **Domain Investigation**
- Follow the [[SOP - Investigating Suspicious Domain Registration]] to evaluate:
    - WHOIS registration details
    - Hosting provider and IP geolocation
    - Website content and functionality
    - Presence of phishing indicators (login pages, branding misuse, certificate mismatches, etc.)
    - Determine whether the domain has overt malicious intent (e.g., phishing, impersonation, malware distribution).
### 3. **Internal Traffic & Email Activity Analysis**
- Check network, web proxy, and DNS logs for any internal traffic to the domain.
- Investigate whether any email has been sent to or received from the domain.
- Search the Threat Intel Platform for previous reports of the domain
### 4. **Mitigation Actions**
- If the organization has a **brand acquisition service**, recommend purchasing the domain to prevent misuse.
- If determined to be malicious:    
    - Report to the **Domain Take Down service** with supporting evidence.
    - Perform a **Business Impact Assessment (BIA)** [[PRO - Business Impact Assessment]] to evaluate risk to the organization.
    - Assuming no significant impact block the domain on:
        - Border firewalls
        - Internal DNS
        - Web proxies
        - Email security gateways
### 5. **Documentation & Reporting**
- Document findings, actions taken, and mitigation outcomes for future reference and correlation.
- Report the typosquat domain to trusted threat intelligence communities to warn third parties.
### 6. **Continuous Monitoring**
- Maintain ongoing monitoring of similar domains to detect further typosquatting threats.
- Reassess trends in domain impersonation to enhance proactive defense strategies.
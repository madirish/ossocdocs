## Purpose
The purpose of this Standard Operating Procedure (SOP) is to outline the steps for investigating an alert that indicates a potentially malicious website. This procedure ensures that SOC analysts follow a structured, methodical approach to assess the risk posed by the website, determine if endpoints have been compromised, and take appropriate actions to mitigate the threat while maintaining operational security.

## Scope
This SOP applies to all SOC personnel responsible for investigating alerts related to potentially malicious websites. It covers the procedures for investigating web traffic detections, analyzing the nature of the website, interacting with IT teams for mitigation, and managing the communication with business stakeholders regarding website blocking.

## Prerequisites
- **Access to Ticketing System:** The SOC analyst must have access to the ticketing system to log and track the investigation.
- **Threat Intelligence Feeds:** SOC analysts should have access to open and closed source threat intelligence feeds to gather relevant data on the suspected malicious website.
- **Sandboxing and Analysis Tools:** Analysts must have access to sandboxing tools (such as VirusTotal, UrlScan.io) for safe investigation of the website, as well as access to network, DNS, proxy, email defense, and process logs.
- **Security Policies and Procedures:** Analysts should be familiar with organizational policies regarding phishing, malware, and credential theft.
- **Collaboration with IT Teams:** Analysts must have access to IT, firewall, DNS, web proxy, and email defense teams for assistance with remediation and blocking actions.

## Roles and Responsibilities

| Role                                               | Responsibility                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                                        | -nvestigate the alert for the potentially malicious website.<br>Create a ticket in the ticketing system to track the investigation.<br>Gather threat intelligence and analyze the website using sandboxing tools.<br>Work with IT teams to patch systems, scan for malware, or reset credentials as needed.<br>Analyze logs to understand how the traffic was generated.<br>Assess the business impact of blocking the website and communicate with business stakeholders. |
| IT Teams including DNS, firewall, web proxy admins | Assist in performing system scans and patching affected systems.<br>Help to block access to the website using DNS, firewall, or web proxy tools.<br>Coordinate with the SOC to resolve endpoint issues if the website was accessed by a compromised host.                                                                                                                                                                                                                  |
| Business Stakeholders                              | Be informed when a website with business value is blocked.<br>Provide contact information for the website owner and follow up with them to resolve the issue.                                                                                                                                                                                                                                                                                                              |
| Identity and Access Management (IAM) Teams         | Reset user credentials if necessary.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Email Defense Team                                 | Remove malicious email and block malicious senders.                                                                                                                                                                                                                                                                                                                                                                                                                        |

## Workflow Diagram
[Insert visual diagram of the SOP workflow]

## Procedure Steps
### 1. Create a Ticket

1. **Log Ticket:** As soon as the alert for a potentially malicious website is identified, create a ticket in the ticketing system to track the investigation.
2. **Assign Priority:** Based on the severity of the alert, assign an appropriate priority level to the ticket.

### 2. Determine Source of Traffic Detection

1. **Identify Endpoints:** Determine the source of the traffic detection (e.g., firewall, proxy, or endpoint detection systems). Identify the affected endpoints that may have interacted with the suspicious website.
2. **Alert Validation:** Verify whether the traffic was generated by an internal host or an external source. Investigate any internal systems that may have attempted to access the website.

### 3. Gather Threat Intelligence

1. **Research Website:** Use threat intelligence sources to gather information about the website. Check open and closed source databases for any known associations with malicious activities.
2. **Sandboxing Tools:** Utilize sandboxing tools such as VirusTotal and UrlScan.io to analyze the website safely. Do not visit the site directly to avoid potential malware infection.
3. **Check Source Code and Screenshots:** Review source code and screenshots provided by sandbox tools to understand the potential risk. Look for indicators such as credential theft attempts, social engineering tactics, malware delivery mechanisms, or exploit code.

### 4. Examine Logs and Investigate Traffic Origins

1. **Log Analysis:** Review network, DNS, proxy, email defense, and process logs to trace how the traffic was generated.
    - Investigate whether the website was accessed via a command and control (C2) beacon from a compromised host.
    - Determine if the site was linked to from a malicious email or advertisement.
    - Investigate whether the site was accessed due to a typo in a domain name or other user action.
2. **Malicious Campaign Investigation:** If the site is part of a broader campaign (e.g., phishing or exploit kit), gather context to assist with larger-scale mitigation.

### 5. Perform Business Impact Assessment

1. **Assess Business Value:** Determine whether the potentially malicious website is critical to business operations. If the site is essential for business purposes, consult with relevant stakeholders to assess the impact of blocking it.
	1. Follow [[PRO - Business Impact Assessment]]
2. **Block the Site:** If the site poses a risk, work with IT teams to block the site using browser, DNS, firewall, or web proxy controls.

### 6. Work with IT and Perform Remediation

1. **End-User Actions:** If necessary, work with IT teams to contact the end users who visited the site to gather more information and inquire about their activities. This may include verifying if they encountered any suspicious behaviors or malware.
2. **Patch and Scan:** Collaborate with IT teams to ensure affected systems are patched, browsers are updated, and a full system malware scan is performed.
3. **Reset Credentials:** If there is suspicion that credentials were compromised, work with IAM to reset user credentials associated with the affected endpoints.
4. **Remove Malicious Email:** If malicious email is detected as the source of the traffic work with email defense teams to have malicious email removed from user inboxes and blocked.
	1. Follow [[PRO - Investigating Suspicious Email]]

### 7. Communicate with Business Stakeholders

1. **Inform Stakeholders:** If the site has business value, notify the relevant business stakeholders that the site is being blocked due to security concerns. Provide them with information on how to contact the site owner and request the issue be resolved.
2. **Site Owner Communication:** Business stakeholders are more likely to have a relationship with the owners of the site and therefore have a higher chance of successful contact and communication with the site owners.  Request that the business stakeholders inform the site owner that their site has been blocked for hosting malicious content and encourage them to reach out to the organization once the issue has been addressed.  The business stakeholder should be instructed to contact the SOC once the issue has been remedied so that the SOC can re-evaluate the site and, if found to be clean, work with IT teams to remove blocks.

### 8. Documentation and Closure

1. **Update the Ticket:** Document all investigation steps, findings, actions taken, and communications with relevant parties in the ticketing system.
2. **Close Ticket:** Once all actions are completed and the site has been properly blocked or resolved, close the investigation ticket, ensuring all information is properly documented for future reference.
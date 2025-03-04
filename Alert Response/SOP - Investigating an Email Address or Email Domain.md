## Purpose
Email is one of the most common vectors for malware transmission, fraud, and credential threat.  During alert investigations it is common to uncover email addresses that need to be investigated to see if they present a threat to the organization.  The purpose of this SOP is to provide a structured and detailed process for Security Operations Center (SOC) analysts to investigate email addresses and sender domains associated with suspicious or malicious activity. This SOP ensures operational security (OPSEC) is maintained during investigations and provides a comprehensive methodology for determining potential threats, business impact, and necessary mitigation actions.

## Scope
This SOP applies to all SOC personnel tasked with investigating email addresses and domains flagged by security alerts, including:

- Email defense alerts
- Suspicious email reports from users
- Malicious document (maldoc) detections
- Third-party email compromise concerns

The scope of this SOP includes:

- Email traffic analysis to determine legitimate business use
- Business Impact Assessments (BIA) to assess potential blocking effects
- Open and closed-source threat intelligence lookups
- Coordination with internal business stakeholders when appropriate
- Collaboration with IT teams for email remediation actions
- Submission of malicious findings to the Cyber Threat Intelligence (CTI) team

## Prerequisites
Before conducting an investigation, the following must be in place:

1. **Tracking Platform Access** – Analysts must log all investigations in an approved case management or ticketing system.
2. **Authorized Investigation Tools** – Only approved email analysis tools, SIEM queries, and threat intelligence platforms should be used.
3. **Privacy and Compliance Awareness** – Analysts must adhere to all policies regarding end-user privacy and seek necessary authorizations before accessing the contents of user emails.
4. **Escalation Paths** – Analysts should be aware of escalation procedures, including the Third-Party Email Compromise SOP.

## Roles and Responsibilities

| Role                                 | Responsibility                                                                                                                                                                                                                                                                                                                                                                                          |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                          | Initiates and conducts email and domain investigations following this SOP.<br>Ensures OPSEC best practices are followed.<br>Documents all findings in the tracking platform.<br>Coordinates with internal business units for impact assessments.<br>Works with IT teams to remove malicious emails when necessary.<br>Submits confirmed malicious entities to the CTI team for tracking and enrichment. |
| SOC Manager                          | Oversees investigations to ensure thoroughness and consistency.<br>Reviews Business Impact Assessments (BIA) before implementing blocking decisions.                                                                                                                                                                                                                                                    |
| Cyber Threat Intelligence (CTI) Team | Validates malicious indicators and enriches findings.<br>Updates internal threat intelligence repositories with relevant IOCs.<br>Provides additional threat context when needed.                                                                                                                                                                                                                       |
| Email Administration Team            | Assists in retrieving email logs and analyzing mail flow.<br>Removes malicious emails from user inboxes upon SOC request.<br>Implements sender or domain blocks as needed.                                                                                                                                                                                                                              |

## Workflow Diagram
[Insert visual diagram of the SOP workflow]

## Procedure Steps
### **Step 1: Create a Ticket in the Tracking Platform**

- Create a ticket for tracking if one does not already exist.
- Log all investigative activities in the ticketing system.
- Include:
    - The email address or domain under investigation.
    - The alert or incident source.
    - Date and time of detection.
    - Initial assessment details.

### **Step 2: Perform Email Traffic Analysis**

- Query email logs to determine:
    - If there is legitimate business communication with the sender.
    - Volume and frequency of emails exchanged.
    - Departments or users interacting with the sender.
- If there is a potential business impact, perform a **Business Impact Assessment (BIA)** before recommending any blocking actions.
	- Ref [[PRO - Business Impact Assessment]]

### **Step 3: Investigate Open and Closed Source Threat Intelligence**

- Use threat intelligence platforms to check if the email address or domain has been:
    - Reported in phishing or email abuse databases (e.g., Spamhaus, VirusTotal, AbuseIPDB).
    - Associated with known malware campaigns.
    - Referenced in closed-source threat intelligence reports.
- Document findings in the investigation ticket

### **Step 4: Investigate the Scope of Potential Email Threats**

- If the email address or domain is linked to malicious activity:
    - Query email logs to determine how many recipients received emails from the sender.
    - Check for user interactions, such as:
        - Opening attachments.
        - Clicking on embedded links.
    - Identify and escalate cases where potential compromise is suspected.

### **Step 5: Assess Business Impact and Notify Stakeholders**

- If blocking the sender/domain **will have a business impact**:
    - Identify an internal business relationship owner associated with the sender.
    - Notify them and provide an overview of the risk.
    - Work with SOC leadership to determine alternative mitigations if blocking is not an option.
- If a **third-party email compromise is suspected**, follow the **Third-Party Email Compromise SOP**

### **Step 6: Remove Malicious Emails from User Inboxes**

- Coordinate with the Email Administration Team to:
    - Remove all instances of malicious emails from user inboxes.
    - Block future emails from the sender/domain if deemed necessary.
    - Implement additional security measures as needed.

### **Step 7: Escalate and Submit to Cyber Threat Intelligence (CTI)**

- If the sender or domain is confirmed to be malicious:
    - Submit it to the CTI team for tracking and enrichment.
    - Ensure threat indicators (IOCs) are added to internal watchlists.
    - Recommend firewall, proxy, and email security team actions where applicable.

### **Step 8: Final Reporting and Closure**

- Document the final assessment, actions taken, and recommendations in the investigation ticket.
- Close the case after all necessary mitigations have been implemented and verified.
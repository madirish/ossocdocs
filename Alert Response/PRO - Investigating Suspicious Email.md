## Purpose
The purpose of this process is to establish a structured approach for Security Operations Center (SOC) analysts to investigate alerts for suspicious or malicious email content. These emails may contain phishing attempts, malware, social engineering tactics, business email compromise (BEC), financial fraud schemes, or other forms of cyber threats. Proper investigation ensures timely detection, containment, and mitigation to protect the organization from potential harm.  Alerts might originate from automated alerting platforms or from direct end user reports.

## Scope
This process applies to all SOC personnel responsible for investigating suspicious email reports and alerts. It involves collaboration with IT teams, email administrators, cyber threat intelligence teams, malware analysts, and identity and access management teams to fully assess and mitigate threats.

The scope includes:

- Analysis of suspicious email artifacts, including headers, body content, and attachments.
- Identification of phishing, malware, BEC, fraud, or other cyber threats.
- Investigation of user interactions with the suspicious email (e.g., clicks, opened attachments).
- Coordination with IT and security teams for containment and mitigation.
- Submission of threat indicators to cyber threat intelligence teams for tracking.
- Ensuring proper response actions, including user notification, credential resets, and email blocking.

## Roles and Responsibilities

| Role                                      | Responsibility                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                               | Investigates reported suspicious emails and associated artifacts.<br>Conducts in-depth analysis using cyber threat intelligence sources, sandbox environments, and open-source tools.<br>Reviews network, system, and Endpoint Detection and Response (EDR) logs to determine if users interacted with malicious elements.<br>Identifies VIPs or sensitive employee groups affected by the suspicious email.<br>Coordinates with IT teams for containment actions such as email removal and domain blocking.<br>Escalates cases where blocking actions may impact business operations. |
| SOC Director                              |  Reviews cases where blocking malicious domains or senders could cause operational harm.<br>Provides final approval on escalation and mitigation strategies.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Email Administration Team                 | Provides copies of suspicious emails for analysis.<br>Assists in identifying email recipients across the organization.<br>Removes malicious emails from user inboxes when necessary.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Cyber Threat Intelligence Team            | Tracks and documents indicators of compromise (IOCs) identified during the investigation.<br>Updates threat intelligence sources with newly discovered malicious domains, email addresses, or URLs.                                                                                                                                                                                                                                                                                                                                                                                    |
| Malware Analysis Team                     | Analyzes any suspected malware contained within email attachments.<br>Provides assessments on malware impact and possible containment actions.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Identity and Access Management (IAM) Team | Resets credentials for users suspected of compromise due to phishing or credential theft.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
## Process Steps
### **Step 0:  Create a Ticket for Tracking**

*  SOC analysts should assign security alerts in the queue based on priority and availability.
- Analysts must acknowledge ownership of an alert in the ticketing platform. If a ticket doesn’t exist the SOC Analyst should create one and assign it to themselves.

### **Step 1: Initial Triage and Analysis**

- Review the reported email to determine if it is suspicious or malicious.
	- Ref [[SOP - Investigating an Email Address or Email Domain]]
- Extract and analyze email headers, body content, and attachments for signs of phishing, malware, or fraud.
	- Ref [[SOP - Investigating an IP Address]]
- Use cyber threat intelligence sources and sandbox environments to further assess potential threats.
- Identify recipients and determine whether VIPs or sensitive employee groups are targeted.

### **Step 2: Investigate Organizational Impact**

- Check email logs to determine if other users received the same email.
- Review network, system, web, and EDR logs for signs of user interaction (e.g., clicking links, opening attachments).
- Assess whether any credentials were compromised and require immediate action.

### **Step 3: Containment and Mitigation**

- Credential Security: If user credentials are suspected to be compromised, coordinate with the Identity and Access Management (IAM) team for immediate password resets.
- Email Removal: Work with the email administration team to remove the malicious email from all affected inboxes.
- Domain/Sender Blocking:
    - Identify malicious email domains, senders, and URLs.
    - Conduct a Business Impact Assessment (BIA) to evaluate potential disruptions before blocking.  Ref [[PRO - Business Impact Assessment]]
    - If blocking could impact business operations, escalate to the SOC Director for final review.
- Malware Submission: If an attachment is suspected to contain malware, submit it to the malware analysis team for examination.

### **Step 4: Communication and Reporting**

- Notify impacted users and provide guidance on next steps.
- Document all findings, actions taken, and indicators in the case management system.
- Share identified threat indicators with the cyber threat intelligence team for tracking and dissemination.
- Escalate cases as necessary for executive review if broader business risks are identified.

### **Step 5: Escalation and Final Decision**

- If a malware infection is confirmed, refer to the **Malware Infection Alert Response SOP** for additional containment steps.
- If a blocking action is deemed necessary but could disrupt operations, escalate to the SOC Director for evaluation.

### **Step 6: Post-Incident Review and Continuous Improvement**

- Conduct a post-investigation review to evaluate the effectiveness of detection and response.
- Update SOC detection rules and response playbooks based on lessons learned.
- Provide awareness training to users on emerging email threats and prevention strategies.
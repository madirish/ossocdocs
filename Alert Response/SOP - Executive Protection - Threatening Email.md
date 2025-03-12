## Purpose
The purpose of this SOP is to define the Security Operations Center (SOC) response process for investigating threatening emails sent to employees, especially executives and publicly identifiable individuals associated with the company. The goal is to assess risk, retain evidence for investigations and law enforcement, and implement mitigation measures to prevent future occurrences.

## Scope
This SOP applies to all SOC analysts, email security teams, physical security personnel, legal teams, Human Resources (HR), and the Cyber Threat Intelligence (CTI) team involved in detecting, investigating, and responding to threatening emails. It also applies to employees who report receiving such communications.

## Prerequisites
- A dedicated security operations shared inbox for storing and tracking threatening emails.
- Email security tools to set up redirect rules and block senders.
- Access to threat intelligence and OSINT tools for investigating email senders.
- Established communication channels with physical security, legal, HR, and law enforcement.
- Regulatory guidance on handling and retaining email data for compliance purposes.

## Roles and Responsibilities

| Role                           | Responsibility                                                                                                                                                                                                                                    |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                    | Receive reports of threatening emails and log incidents.<br>Work with the email security team to implement redirect and blocking rules.<br>Investigate the sender for contextual intelligence.<br>Notify relevant teams for coordinated response. |
| SOC Manager                    | Track metrics for volume and response                                                                                                                                                                                                             |
| Physical Security Team         | Assess potential threats and determine protective responses. <br>Coordinate with law enforcement as necessary.                                                                                                                                    |
| HR                             | Evaluate any internal personnel implications of the email.<br>Provide support for staff.                                                                                                                                                          |
| Data Privacy                   | Provide regulatory guidance on email redirection and retention policies.                                                                                                                                                                          |
| Legal                          | Review legal implications of the threatening communication.<br>Provide guidance on law enforcement collaboration.                                                                                                                                 |
| Email Security Team            | Configure email redirect rules tailored to the specific sender or recipient.<br>Ensure original emails are retained in the dedicated security operations inbox.                                                                                   |
| Cyber Threat Intelligence Team | Enrich the investigation with threat intelligence.<br>Assess broader threat actor activity related to the email.                                                                                                                                  |

## Procedure Steps
#### 1.Threatening Email Report Intake ####
    
- Employees report threatening emails to the SOC via established channels (security hotline, email, ticketing system).
- SOC analysts create a case file in the incident management system.
	- Analyst provides rough details on the case, taking care to avoid putting any confidential information into the ticketing system that could compromise further investigation
#### 2. Email Collection & Storage ####
    
- Forward the email to the security operations shared inbox for tracking.
- Create a dedicated case folder within the shared inbox to store email evidence, possible naming conventions include the ticket number from Step 1.
- Retain the original email, ensuring email headers and metadata remain intact.
#### 3. Compliance & Legal Review####
    
- Consult the Data Privacy Team to ensure compliance with regulations and company policies surrounding email redirection as well as threats identified.
- Coordinate with the Legal Team to determine any necessary legal action.
#### 4. Email Redirect & Blocking Configuration####
    
- Work with the email security team to set up a redirect rule tailored to the sender(s) or recipient(s).
- Optionally implement sender blocking rules as necessary while ensuring original emails are retained.
- Grant access to the dedicated case folder to partner teams (physical security, legal, HR) as needed.
#### 5. Threat Investigation & Intelligence Gathering####
    
- Conduct an email sender investigation using OSINT and proprietary tools:
    - Analyze email headers for sender origin and infrastructure details.
    - Check domain reputation and IP addresses for known threat indicators.
    - Look for related activity in Threat Intelligence Platforms (TIPs) and open-source threat exchanges.
- Escalate findings to the CTI Team for enrichment and deeper analysis.
- Correlate observables with any previous cases or indicators.
#### 6. Internal & External Coordination####
    
- Physical Security Team:
    - Assess if the threat warrants a protective response.
    - Coordinate with law enforcement if deemed necessary.
- Legal & HR Teams:
    - Evaluate risks related to company personnel and legal action.
    - Track cases for legal or disciplinary measures.
- Cyber Threat Intelligence Team:
    - Analyze if the sender is linked to other threats or campaigns.
    - Contribute intelligence findings to internal tracking systems.

#### 7. Mitigation & Prevention Measures####
    
- If required, update email security policies to block the sender across corporate email systems.
- Educate employees on handling and reporting threatening emails.
- Monitor for any recurring threats from the same sender or affiliated sources.
#### 8. Documentation & Case Closure####
    
- Document all findings, investigative steps, and communications in the incident management system.
- Share a summary with relevant teams (SOC, physical security, legal, HR, CTI).
- Retain the email evidence per legal and compliance requirements.
- Conduct a post-incident review to improve future response capabilities.
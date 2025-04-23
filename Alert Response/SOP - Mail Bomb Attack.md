## Purpose
The purpose of this SOP is to define the Security Operations Center (SOC) response to mail bomb attacks—where legitimate email services are abused to flood a target inbox with a high volume of emails. This type of denial-of-service attack can distract or overwhelm recipients, often to obscure or delay their awareness of another attack (e.g., fraud or compromise).

## Scope
This SOP applies to all SOC analysts and email security personnel involved in detecting, investigating, and mitigating mail bomb attacks affecting users within the organization. It includes coordination with the email security team, help desk, and other partner teams as required.

## Prerequisites
- Access to email security gateway and spam/quarantine management tools
- Access to email logs and user mailbox activity data
- Contact information for the email security team and help desk
- Knowledge of organizational policies for spam thresholds and email filtering
- Defined escalation paths to impacted business units, Legal, and Incident Response (IR) teams

## Roles and Responsibilities

| Role                        | Responsibility                                                                                                                                                                                                                                                                                              |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                 | Identify and investigate suspected mail bomb activity.<br>Coordinate with email security team to implement temporary filtering measures.<br>Notify stakeholders of the threat and any associated suspicious activity (e.g., attempted fraud).<br>Monitor for indicators of secondary or associated attacks. |
| SOC Manager                 | Collect metrics on mail bomb attack response<br>Provide oversight for response and resolution                                                                                                                                                                                                               |
| Email Security Team         | Adjust spam thresholds and filtering rules for targeted users.<br>Create or update rules to help suppress or quarantine high-volume, repetitive emails.<br>Coordinate recovery actions, such as mailbox cleanup or redirecting email delivery.                                                              |
| Help Desk                   | Support impacted users with mailbox access, cleanup, and temporary redirection.                                                                                                                                                                                                                             |
| Incident Response (IR) Team | Assess the potential for concurrent or obfuscated attacks.<br>Investigate broader campaign activity.                                                                                                                                                                                                        |
| Legal & Compliance          | Provide guidance on regulatory implications if sensitive data is involved or systems are significantly disrupted.                                                                                                                                                                                           |

## Procedure Steps
### 1. Detection & Validation
- Alert may originate from:
	- User reports of overwhelming email volume.
	- Monitoring tools detecting anomalous spikes in inbox activity.
	- Security alerts linked to known indicators of mail bomb campaigns.
- Validate that the emails are:
	- High in volume (hundreds or thousands received in a short window).
	- Legitimate in structure but unsolicited (e.g., newsletter signups).
	- Originating from various sources (mailing lists, subscription services).
### 2. Immediate Containment Actions
- Notify the email security team to:
	- Lower the spam filtering threshold for the targeted inbox.
	- Quarantine high-volume or repetitive emails.
	- Enable aggressive greylisting or throttling for the user temporarily.
- If mailbox is inaccessible, redirect email to a secure mailbox for analysis.
- Advise the Help Desk to assist the user with:
	- Mailbox cleanup
	- Message rule creation for sorting or deletion
### 3. Threat Investigation
- Investigate whether the attack is linked to a larger operation:
	- Check for simultaneous alerts involving the targeted user (e.g., login anomalies, financial transactions).
	- Review email logs for phishing, fraud, or internal compromise indicators.
	- Examine the target’s role or access rights (executive, finance, IT admin, etc.).
- Involve the IR team if the mail bomb appears to be covering for an active threat.
### 4. Defensive Measures
- In coordination with email security:
	- Create keyword or sender-pattern rules to pre-filter future flood content.
	- Adjust SPF/DKIM/DMARC configurations to reduce spoofed message delivery.  
	- Temporarily disable auto-forwarding or rules that may expose the user to more spam.
	- Use adaptive threat detection to suppress future flooding behavior.
- For critical users (executives, finance, IT):
	- Enable mail flow monitoring for rapid detection of similar attacks in the future.
	- Consider an alternate protected inbox for business-critical alerts.
### 5. Recovery & Restoration
- Coordinate with the Help Desk to:
	- Restore normal spam filtering thresholds once the attack subsides.
	- Ensure any legitimate quarantined messages are recovered.
	- Educate the user on identifying suspicious activity and phishing attempts.
- Update the case with full incident details and actions taken.
### 6. Post-Incident Actions & Best Practices
- Document the incident for metrics and threat intelligence tracking.
- Review and update detection thresholds to improve sensitivity to sudden mailbox anomalies.
- Notify Legal and Compliance if the user missed a time-sensitive or regulated alert due to the attack.
- Share IOCs (domains, sender patterns, tactics) with the Threat Intelligence Team and any trusted sharing partners.
- Evaluate need for additional mitigations, such as:
	- Subscription sign-up protections using CAPTCHA for organizational domains
	- User training for reporting suspicious signup confirmations or newsletters
	- API integrations with third-party abuse reporting services

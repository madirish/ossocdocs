## Purpose
The purpose of this SOP is to provide a structured approach for the Security Operations Center (SOC) to identify, investigate, and remediate compromised credentials effectively. This process aims to minimize risk, limit exposure, and ensure business continuity while preventing unauthorized access to corporate systems and data.
## Scope
This SOP applies to all SOC analysts, Incident Response (IR) teams, and Identity and Access Management (IAM) personnel responsible for detecting, investigating, and responding to compromised credentials across corporate systems and applications.

## Prerequisites
- Access to security monitoring tools (SIEM, identity protection solutions, threat intelligence platforms)
- Understanding of authentication activity logs and user behavior analytics
- Knowledge of corporate password policies and multi-factor authentication (MFA) configurations
- Established communication channels with the IAM team, IR team, and Data Privacy team

## Roles and Responsibilities

| Role                         | Responsibility                                                                                                                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                  | Monitor for compromised credential alerts, investigate authentication anomalies, and coordinate remediation actions.<br>Perform business impact assessments.<br>Enumerate any unauthorized data access. |
| SOC Manager                  | Track cases of account compromise for metrics and reporting.                                                                                                                                            |
| IR Team                      | Handle escalations related to VIP and critical business function accounts, assess broader security incidents, and coordinate containment efforts.                                                       |
| IAM Team                     | Assist in resetting credentials, disabling accounts, and enforcing policy compliance for affected users.                                                                                                |
| Data Privacy Team            | Investigate unauthorized data access and support regulatory compliance efforts.                                                                                                                         |
| Cybersecurity Awareness Team | Track trends in compromised credentials and implement user training programs to mitigate risk.                                                                                                          |

## Procedure Steps

### 1. **Detection & Triage**
- Review alerts related to compromised credentials, including:
    - Impossible travel
    - Unusual sign-in activity
    - End-user reports of unauthorized access
    - Investigations from phishing or social engineering alerts
- Validate the alert by reviewing authentication logs and correlating them with threat intelligence sources.

### 2. **Containment & Business Impact Assessment**
- Determine the potential business impact of the compromised account.
	- Follow [[PRO - Business Impact Assessment]]
- If the account belongs to a VIP or is tied to a critical business function, escalate to the IR team.
- If impact is minimal, proceed with credential resets and token expiration.

### 3. **Credential Reset & Security Enforcement**
- Work with the IAM team to reset compromised credentials.    
- Expire any active authentication tokens.
- Verify compliance with password policy minimums.
- Confirm MFA is enabled for the affected account.

### 4. **Threat Actor Investigation**
- Review authentication activity to identify unauthorized access attempts.    
- Investigate whether data has been accessed or exfiltrated and notify the IR and Data Privacy teams if confirmed.    
- Check for persistence mechanisms such as:
    - Email forwarding rules    
    - Changes to authentication devices or methods    
    - Presence of credential-harvesting malware on endpoints

### 5. **Elevated Monitoring & Documentation**
- Place the compromised account under elevated monitoring for 48 hours.
- Document all findings and remediation actions in the SOC ticketing system.
- Communicate the status of compromised accounts during Shift Handoff.

### 6. **User Awareness & Risk Tracking**
- Maintain records of compromised credentials to identify high-risk users.
- Coordinate with the cybersecurity awareness training team to improve user education on credential security.
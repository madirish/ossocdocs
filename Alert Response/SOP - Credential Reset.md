## Purpose
The purpose of this SOP is to provide a structured approach for the Security Operations Center (SOC) to investigate and respond to suspected credential compromises. The goal is to limit unauthorized access, minimize business disruption, and ensure a swift and effective response that balances security with operational needs.

## Scope
This SOP applies to SOC analysts, Identity and Access Management (IAM) personnel, Help Desk teams, and SOC leadership responsible for identifying, assessing, and responding to credential compromises within the organization’s IT environment.

## Prerequisites
- Access to authentication logs and security monitoring tools (SIEM, identity protection platforms, endpoint security solutions)
- Knowledge of organizational credential reset procedures and policies
- Communication channels with the IAM team, Help Desk, and business units
- Access to Business Impact Assessment (BIA) templates and risk assessment tools
- Established credential tracking and reporting mechanisms

## Roles and Responsibilities

| Role                                 | Responsibility                                                                                                                                                                                                                                                                                                   |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                          | Detect and investigate suspected credential compromises.<br>Conduct Business Impact Assessments (BIA) before initiating credential resets.<br>Work with IAM and Help Desk to ensure smooth credential resets with minimal disruption.<br>Document instances of credential compromise for tracking and reporting. |
| SOC Manager                          | Track instances of credential compromises to generate threat metrics.<br>Assess trends in credential threats and recommend improvements to security controls.                                                                                                                                                    |
| Identity and Access Management (IAM) | Facilitate secure and rapid credential resets, including expiring authentication tokens.<br>Implement access controls and monitor accounts for anomalous activity post-reset.                                                                                                                                    |
| Help Desk Team                       | Assist affected users with credential reset procedures.<br>Provide user education on secure credential management post-reset.                                                                                                                                                                                    |
| Business Unit Representatve          | Provide context on potential business impact before executing credential resets.                                                                                                                                                                                                                                 |

## Workflow Diagram
[Insert visual diagram of the SOP workflow]

## Procedure Steps
### 1. Detection & Triage ###
- Identify potential credential compromises through:
    - Security alerts (e.g., unusual login patterns, impossible travel, brute force attempts)
    - Incident investigations (e.g., phishing, malware infections, third-party breaches)
    - User-reported suspicious activity
- Verify the compromise by reviewing:
    - Authentication logs for unauthorized access
    - Endpoint security logs for credential-stealing malware
    - Dark web monitoring for leaked credentials
            
### 2. Business Impact Assessment (BIA) ###
- Perform a [[PRO - Business Impact Assessment]] to valuate the impact of resetting the credential:
    - Is the account a service account or used for non-human authentication?
    - Is the affected user a VIP or involved in critical business functions?
    - Would a reset disrupt an ongoing process (e.g., manufacturing process, logistics fulfillment, board meetings, financial filings, etc.)?
    - If business impact is high, consult relevant stakeholders before proceeding.
	    - Escalate to SOC Leadership as necessary
        
### 3. Containment & Credential Reset ###
- Work with IAM to reset the compromised credential
- Ensure all credential types are reset, including:
    - Passwords and PINs
    - API keys and service account credentials
    - Multi-factor authentication (MFA) methods
    - Expiry of active authentication tokens
- Apply temporary account restrictions if necessary to prevent further unauthorized use.
        
### 4. Threat Investigation & Remediation###
- Investigate how the credential was compromised:
    - Social engineering (e.g., phishing attack, impersonation attempts)
    - Malware-based credential theft
    - Password reuse from third-party breaches
    - Brute force or credential stuffing attacks
- Take additional remediation actions as needed:
    - Remove malware from affected endpoints
    - Block malicious IP addresses or domains used in credential attacks    
    - Strengthen authentication policies (e.g., enforcing MFA, updating password policies)
            
### 5. Monitoring & Follow-Up Actions###
- Place affected accounts under elevated monitoring for anomalous activity.
- Verify no persistence mechanisms were left by attackers, such as:
    - Unauthorized email forwarding rules
    - Changes to authentication devices or MFA settings
    - Unauthorized application permissions
    - Communicate updates and findings to relevant stakeholders.
        
### 6. Tracking & Reporting###
- Document the incident, including:
    - Initial detection method
    - Investigation findings
    - Business impact assessment results
    - Actions taken to reset credentials and secure accounts
- SOC Leadership should:
    - Aggregate data on credential compromise incidents
    - Identify trends and risk areas
    - Recommend improvements to security policies and authentication controls
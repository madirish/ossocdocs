## Purpose
The purpose of this SOP is to provide guidance for the Security Operations Center (SOC) team in identifying, investigating, and responding to password spray attacks. These attacks are designed to evade brute-force detection and account lockout policies by testing a small number of common passwords against a large number of accounts. Timely and thorough investigation is essential to prevent account compromise and lateral movement within the organization.

## Scope
This SOP applies to all SOC analysts and supporting teams involved in monitoring, detecting, and responding to authentication anomalies within enterprise environments. It specifically addresses password spray attacks targeting user accounts through internet-facing authentication portals or internal systems.The relative scope for the procedure.

## Prerequisites
- Access to authentication logs and identity providers (e.g., Azure AD, Okta, LDAP)
- Access to SIEM for querying login behavior and correlation rules
- Tools to examine IP geolocation, VPN indicators, and IPv6 usage
- Integration with Multi-Factor Authentication (MFA) monitoring
- Communication channels with Identity and Access Management (IAM) and Incident Response (IR) teams
- Understanding of baseline user login behavior

## Roles and Responsibilities

| Role                                    | Responsibility                                                                                                                                                                                                                                                                       |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| SOC Analyst                             | - Monitor and investigate password spray attack alerts<br>- Validate alerts and determine legitimacy of source IP behavior<br>- Coordinate with IAM and IR teams for containment and user protections<br>- Document the investigation and outcomes for reporting and lessons learned |
| SOC Manager                             | - Track metrics related to Password Spray attacks                                                                                                                                                                                                                                    |
| IR Team                                 | - Assist in investigating confirmed compromises<br>- Lead containment and remediation activities for affected accounts                                                                                                                                                               |
| IAM Team                                | - Enforce credential resets, MFA enforcement, and account lockout protections<br>- Support visibility into login and authentication activity                                                                                                                                         |
| Firewall and Security Engineering Teams | - Implement blocks on suspicious IP addresses<br>- Improve detection rules and anomaly thresholds based on attack patterns                                                                                                                                                           |
| Threat Intelligence (TI) Team           | - Track adversary TTPs related to password spray attacks.                                                                                                                                                                                                                            |

## Procedure Steps
### 1. Alert Triage and Initial Validation

- Review the password spray detection alert from the SIEM or identity provider
- Validate the alert by:
    - Checking the number of unique usernames targeted
    - Verifying whether the login attempts used a small set of common passwords
    - Identifying the source IP address associated with the logins

### 2. Confirm Suspicious Source Behavior

- Analyze the login history for a sample of targeted users to determine:
    - If the source IP address is previously unseen or located in an unusual region
    - If the activity pattern could be associated with known VPN or proxy services
    - If login attempts are spread out over time to avoid detection
    - Reverse DNS and WHOIS lookup on source IP addresses
- Evaluate whether the source IP is an IPv6 address targeting multiple accounts, a strong indicator of malicious intent
- Use of threat intelligence feeds to identify known malicious infrastructure
- GeoIP correlation to detect unusual login locations
- Timeline reconstruction of login attempts across affected accounts
- Behavioral analysis of affected accounts post-login (e.g., privilege escalation, file access)

### 3. Investigate IP-Based Activity

- Query all login activity from the suspicious source IP address:
    - Identify the number of user accounts targeted
    - Determine the timeframe and frequency of attempts
    - Note whether login attempts are focused on internet-facing portals
- Review any related alerts for the IP (e.g., threat intelligence, known IOC correlation)

### 4. Examine MFA Failures and Account Status

- Identify any failed MFA attempts tied to successful password authentication
- Check for accounts with password success but MFA denial
- Review lockout status of affected accounts and user behavior following suspicious logins
- Cross-reference alerts with behavioral anomalies (e.g., access to sensitive systems, unusual file access)

### 5. Containment and Mitigation

- Block suspicious IP addresses at the perimeter firewall or proxy service
- If successful compromise is suspected:
    - Reset affected account passwords following [[SOP - Credential Reset]]
    - Expire existing authentication tokens
    - Re-enroll or revalidate MFA devices
- Temporarily restrict access to high-risk accounts pending further investigation
- Notify affected users and provide phishing awareness reminders

### 6. Communication and Coordination

- Notify the IR team of any confirmed account compromises
- Escalate to IAM and IT support to assist users with remediation
- Communicate with Legal and HR teams if sensitive accounts were targeted
- Collect any observables and submit them to the Cyber Threat Intelligence (CTI) Team

### 7. Documentation and Follow-Up

- Document the alert details, investigation steps, and findings in the SOC case management system
- Note all IP addresses, user accounts, and indicators observed during the incident
- Recommend tuning detection rules to account for the techniques used
- Contribute findings to the threat intelligence platform for future enrichment

### 8. Post-Incident Review and Best Practices

- Assess the effectiveness of detection and response measures
- Implement rule improvements for identifying low-and-slow credential attacks
- Ensure high-value accounts (e.g., executives, finance) have strong MFA policies enforce    
- Consider user segmentation for at-risk groups (e.g., with additional logging or alerting thresholds)
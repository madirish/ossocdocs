## Purpose
The purpose of this document is to outline a standardized process for investigating security alerts and incidents within the Security Operations Center (SOC). This runbook ensures efficient triage, identification, escalation, and resolution of security alerts while maintaining comprehensive documentation throughout the incident response lifecycle. This process document is for an agnostic runbook that provides the template for other, more specific, runbooks that can be customized for various types of alerts.

## Scope
This process applies to all SOC analysts responsible for investigating security alerts, determining true positives or false positives, and escalating incidents when necessary. It covers the full incident response lifecycle, with a focus on quick triage and identification of active threats that require immediate escalation to the Incident Response (IR) team.

## Roles and Responsibilities

| Role               | Responsibility                                                                                                                                                                                                                                                                                                                                                          |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst        | Monitor, triage, and investigate security alerts.<br>Determine the validity and severity of alerts (true positive or false positive).<br>Document all investigative steps and findings.<br>Escalate confirmed incidents to the Incident Response (IR) team.<br>Escalate complex or unclear cases to L3 support.<br>Provide remediation recommendations when applicable. |
| Senior SOC Analyst | Provide deeper technical analysis for complex or unclear alerts.<br>Assist in determining appropriate escalation paths.<br>Collaborate with the Incident Response (IR) team as needed.<br>Perform retrospective quality checks on investigation tickets and outcomes to ensure correctness and conformity with documented process.                                      |
| SOC Manager        | Collecting metrics and presenting analysis on true positives, false positives, and escalations.<br>Presenting metrics and analysis on a weekly basis to senior leadership.                                                                                                                                                                                              |
| IR Team            | Respond to escalated incidents involving active attacks (e.g., hands-on-keyboard attackers, ransomware, spreading malware, phishing campaigns, etc.).<br>Perform containment, eradication, and recovery actions.<br>Coordinate with relevant teams for mitigation and incident resolution.                                                                              |
## Process Steps
### Step 1 - Create a Ticket
- SOC analysts should assign security alerts in the queue based on priority and availability.
- Analysts must acknowledge ownership of an alert in the ticketing platform. If a ticket doesn’t exist the SOC Analyst should create one and assign it to themselves.

### Step 2 - Initial Triage and Investigation
- Gather alert details, including:
    - Alert type and severity.
    - Affected users, hosts, or systems.
        - Determine if alert contains priority indicators including, but not limited to:
            - Manufacturing or lab environment
            - VIP user
            - Known hacking tools such as Cobalt Strike, Mimikatz, Bloodhound, etc.
            - Indication of active attack such as spreading malware, ransomware, or active attackers
        - If priority indicators are observed escalate immediately
    - Detection source (SIEM, EDR, IDS/IPS, etc.)
    - Correlation with other security events.
- Check for false positive indicators by analyzing historical context, threat intelligence sources, and environmental factors.
- If an alert is confirmed as a false positive, document findings
- If the alert is inconclusive, proceed with deeper investigation or escalate to Senior Analyst support.

### Step 3 - Scoping the Incident
- If the alert appears legitimate, determine the scope by identifying:
    - Affected assets and users.
    - Potential attack vectors and entry points.
    - Associated indicators of compromise (IOCs) such as IP addresses, hashes, or domain names.
    - Lateral movement or persistence mechanisms.

### Step 4 - Identifying True Positive Alerts
- If the alert is confirmed as a security incident, escalate it appropriately:
    - If there is evidence of an active attack (e.g., hands-on-keyboard attacker, ransomware execution, spreading malware, ongoing phishing campaign), immediately escalate to the IR team.
    - If the incident is severe but not an immediate active attack, escalate it through the appropriate internal workflow.
- Document all findings in the case management system.

### Step 5 - Handling False Positive Alerts
- If the alert is determined to be a false positive:
    - Gather relevant details
    - Submit a tuning request to the appropriate vendor flagging the false positive

### Step 6 - Escalation and Remediation
- If unsure about any aspect of the alert, escalate ton Senior Analyst support for guidance.
- Work with relevant teams (e.g., IT, IR, vulnerability management) via ticketing requests for containment and remediation actions as appropriate, such as:
    - Isolating compromised hosts.
    - Resetting credentials.
    - Blocking malicious domains or IPs.
    - Removing malware or malicious files.
- Document all related remediation request ticket numbers and outcomes.

### Step 6 - Documentation and Close Out
- Comprehensive documentation is required for every alert investigation, regardless of the outcome.
- Include:
    - All investigative steps and reasoning.
    - Any evidence collected.
    - Mitigation or remediation actions taken.
    - Escalation paths and responses.
    - Conclusion (true positive, false positive, or inconclusive).
- Ensure proper case closure with detailed summary notes for future reference and audits.
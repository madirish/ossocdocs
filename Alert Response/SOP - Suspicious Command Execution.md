## Purpose
This Standard Operating Procedure (SOP) outlines the investigation process for suspicious command execution alerts within the Security Operations Center (SOC). Living Off the Land (LOTL) techniques, frequently used by Advanced Persistent Threat (APT) actors, exploit built-in administrative tools such as PowerShell, WMIC, command prompt, Visual Basic, and other native utilities to carry out attacks while evading detection.

Due to the dual-use nature of these tools, false positives from legitimate IT administration activities are common. This SOP provides structured guidance to help SOC Analysts differentiate between legitimate activity and malicious activity by analyzing command execution characteristics, user context, and environmental prevalence.
## Scope
This SOP applies to all SOC Analysts responsible for monitoring, investigating, and responding to suspicious command execution alerts within the organization’s security infrastructure, including:

- SIEM-generated alerts
- Endpoint Detection and Response (EDR) telemetry
- Threat intelligence reports on LOTL techniques
- Suspicious activity reported by IT and security teams

This SOP covers:

- Identifying indicators of malicious LOTL techniques
- Evaluating command execution in the context of user roles and system activity
- Determining whether activity is benign, suspicious, or malicious
- Escalating cases where a determination cannot be made

## Prerequisites
Before beginning an investigation, SOC Analysts must:

- Have access to relevant security tools, including SIEM, EDR, log aggregators, and threat intelligence platforms.
- Be trained on common LOTL techniques, including obfuscation, anti-forensic methods, and security bypass techniques.
- Understand baseline IT administrative activities within the organization.
- Be familiar with incident response escalation protocols and OPSEC considerations for investigating potential account compromises.

## Roles and Responsibilities

| Role                        | Responsibility                                                                                                       |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst                 | Investigates suspicious command execution alerts, determines legitimacy, and escalates where necessary.              |
| Threat Intelligence Analyst | Provides context on emerging LOTL techniques and threat actor tactics.                                               |
| IT Administrator            | Assists with validating legitimate administrative actions when necessary.                                            |
| Incident Response (IR) Team | Takes ownership of escalated cases, conducts deeper forensic analysis, and responds to confirmed security incidents. |

## Procedure Steps

### **Step 1: Create a Ticket in the Tracking Platform**

- Create a ticket for tracking if one does not already exist.
- Log all investigative activities in the ticketing system.
- Include:
    - The email address or domain under investigation.
    - The alert or incident source.
    - Date and time of detection.
    - Initial assessment details.
### **Step 2: Review the Detection Alert**

- Gather alert details from SIEM, EDR, or other monitoring tools, including:
    - Command executed (e.g., `powershell.exe -exec bypass -encodedCommand...`)
    - User account that executed the command
    - Source system (hostname, IP address, asset classification)
    - Process lineage (parent process and child processes)
    - Execution timestamp

### **Step 3: Assess the Context of the Executing User**

- Is the command indicative of a known hacking tool?
	- [[SOP - Known Hacking Tools]]
- Identify the user account that executed the command:
    - Is the account a known IT administrator?
    - Is the account service-related, or is it tied to an end user?
    - Has the account been recently created, modified, or accessed from unusual locations?
- **Review recent account activity**:
    - Check authentication logs for anomalous logins.
    - Review whether the account has engaged in similar command executions previously.

### **Step 4: Analyze the Nature of the Command Execution**

- Check for obfuscation techniques:
    - Encoded commands (e.g., `-encodedCommand`, `Base64 encoding`)
    - String concatenation or escaping (e.g., `^p^o^w^e^r^s^h^e^l^l`)
    - Use of alternate character sets (e.g., ASCII/Unicode tricks)
- Identify anti-forensic techniques:
    - Attempts to disable logging (`wevtutil cl Security`, `auditpol /set`)
    - Clearing event logs (`Clear-EventLog`, `Remove-Item -Path C:\Windows\System32\winevt\Logs`)
    - Modifying or deleting security tools (`taskkill /IM defender.exe`, `net stop securityservice`)
- Check for security bypass techniques:
    - Execution with `-ExecutionPolicy Bypass` (PowerShell)
    - Running scripts from hidden locations (`C:\Windows\Temp\`, `C:\Users\Public\`)
    - Use of Living Off the Land Binaries (LOLBins) (e.g., `rundll32.exe`, `certutil.exe`, `mshta.exe`, `wmic.exe`)

### **Step 5: Compare Against Normal Environmental Behavior**

- Query SIEM/EDR logs to determine:
    - How frequently this command has been executed in the environment.
    - Whether this behavior has been seen from the same user, host, or department before.
    - If there are correlated alerts or anomalies from the same source system.

### **Step 6: Determine Legitimacy**

- If the command aligns with known IT administrative tasks, no further action is required, but documentation should be maintained.
- If the command is highly unusual for the executing user/system, proceed with out-of-band verification:
    - Do not contact the user directly via their compromised account or workstation.
    - Use alternative communication channels (e.g., secure email, phone, ticketing system) to validate activity.

### **Step 7: Escalate to Incident Response (if needed)**

- If malicious activity is confirmed or uncertainty remains, escalate to the Incident Response Team (IRT) with:
    - Summary of findings (command details, user behavior, risk factors).
    - Indicators of compromise (IoCs) (if applicable).
    - Recommendations for containment (e.g., account lockout, host isolation).

### **Step 8: Document the Investigation**

- Log findings in the case management system, including:
    - The command and its context
    - Determination (benign, suspicious, malicious)
    - Actions taken (investigation, escalation, remediation, no further action)
    - Lessons learned for refining detection logic

### **Step 9: Improve Detection Engineering and Response**

- If the alert was a false positive, recommend tuning the detection to reduce noise while maintaining security coverage.
- If the alert was valid, coordinate with Detection Engineering to:
    - Enhance detection logic (e.g., detecting command obfuscation).
    - Develop **new alerting rules** to cover related activity patterns.

## Conclusion

Investigating suspicious command execution requires context-aware analysis to differentiate between legitimate IT administration and potential attacker activity. Given the high rate of false positives with LOTL techniques, SOC Analysts must carefully assess the user, execution context, and intent behind suspicious commands. In cases of uncertainty, escalation to Incident Response is critical. Additionally, OPSEC considerations must be maintained to prevent tipping off potential adversaries.

By following this SOP, SOC Analysts ensure a methodical, efficient, and effective response to suspicious command execution alerts, strengthening the organization’s cybersecurity posture.
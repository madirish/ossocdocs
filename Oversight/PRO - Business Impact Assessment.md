## Purpose

The purpose of this document is to outline the process for the Security Operations Center (SOC) to conduct a Business Impact Assessment (BIA) when evaluating the potential impact of an operational change in the environment. This assessment ensures that any modifications do not cause unnecessary interruptions or delays to business operations.

## Scope

This process applies to all SOC personnel involved in evaluating operational changes that may affect business functions. Examples of such changes include:

- Blocking a web domain.
- Blocking an email sender.
- Adding software to an allow or block list.
- Creating a network exception.
- Isolating a host.
## Roles and Responsibilities

| Role         | Responsibility                                                                                       |
| ------------ | ---------------------------------------------------------------------------------------------------- |
| SOC Analyst  | Gather and analyze relevant data sources to determine potential business impact.                     |
| SOC Manager  | Review assessments, provide additional insights, and oversee escalation if necessary.                |
| SOC Director | Provide final approval on changes with significant impact and coordinate with relevant stakeholders. |
## Process Steps
### Step 1 - Identify the Operational Change
- Clearly define the proposed operational change.
- Determine the reason for the change (e.g., security risk mitigation, compliance, policy enforcement).
### Step 2 - Gather Impact Data
- Investigate relevant data sources to assess potential impact, including:
    - **Web Proxy Logs**: Identify users accessing the domain or service.
    - **Email Traffic Volumes**: Determine email flow affected by blocking a sender.
    - **Tickets**: Check for previous incidents or business requests related to the change.
    - **SIEM**: Analyze security logs for patterns and affected assets.
    - **Other Data Sources**: Utilize additional security or IT infrastructure logs where applicable.
### Step 3 - Determine Affected Users and Business Functions
- Identify the volume and type of users impacted by the proposed change.
- Assess if critical business units or key personnel would be affected.
- Determine whether business operations or revenue-generating activities might be disrupted.

### Step 4 - Risk vs. Benefit Analysis
- Weigh the security benefits of implementing the change against the potential business impact.
- Consider alternatives or mitigations to reduce impact while maintaining security objectives.

### Step 5 - Develop a Recommendation
- Document findings, including:
    - Summary of the proposed change.
    - Data supporting the impact assessment.
    - Identified risks and affected users.
    - Suggested mitigations (if applicable).
    - Final recommendation (approve, deny, modify the change).

### Step 6 - Submit for Approval
- All requests for approval must include an email summary and documentation trail for later review
- Present the assessment and recommendation to the SOC Director.
- If the impact is deemed significant, escalate to the SOC Director or further review.
- Include all relevant evidence and context to assist in the approval decision.

### Step 7 - Implement Change
- If the change is approved create the appropriate change tracking in the ticketing system
    - Include relevant communications and approval
- Implement the change
- Close the change ticket in ticketing system
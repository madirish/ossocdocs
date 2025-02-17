## Purpose

The purpose of this policy is to establish clear guidelines for managing the alert queue within the Security Operations Center (SOC) to ensure efficient prioritization and resolution of security alerts. By following structured queue management procedures, the SOC can ensure that the highest priority alerts are investigated and addressed first, while lower priority alerts are handled in descending order of urgency. This approach aligns with the organization's Service Level Objectives (SLOs) and ensures that resources are optimally allocated to meet security demands. Proper alert queue management contributes to effective incident response, improves operational efficiency, and helps maintain the security posture of the organization.

## Scope

This policy applies to all Security Operations Center (SOC) analysts, Shift Leads, and SOC leadership, as well as any associated teams involved in managing or responding to alerts. It covers all alerts received by the SOC, from high to low priority, and establishes procedures for triaging, prioritizing, assigning, and investigating those alerts. This policy is applicable 24/7 and across all SOC shifts, ensuring that alerts are handled in accordance with defined priority levels and available resources.

## Related Content
* [[POL - Shift Handoff]]

## Roles and Responsibilities

| Role           | Responsibility                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst    | Acknowledge and investigate assigned alerts in priority order (High, Medium, Low).<br>Document investigation steps and findings, ensuring tickets are created and properly updated.<br>Escalate unresolved or complex issues to Senior Analysts as necessary.<br>Report any gaps or challenges in alert triage or investigation processes to the Shift Lead or SOC leadership.                                                                                                                                                                                                                                                                                                                             |
| Shift Lead     | Continuously monitor the alert queue to ensure that all incoming alerts are triaged and assigned based on priority.<br>Ensure that tickets are created for each alert investigation and group related alerts together as needed.<br>Assign alerts to SOC analysts according to their availability and expertise, ensuring that higher priority alerts are investigated first.<br>Track and ensure that Service Level Objectives (SLOs) are being met and alert the IR team if the SOC workload becomes overwhelming.<br>Provide clear handoffs between shifts, ensuring that alert priorities are communicated and maintained.<br>Maintain oversight of alert investigations and ensure timely resolution. |
| SOC Leadership | Monitor the overall alert volume and ensure sufficient resources are allocated to meet the demands of the alert queue.<br>Track metrics related to alert volume, priority, response time, and resolution time, and report findings at least weekly.<br>Ensure the SOC team adheres to documented procedures for alert prioritization and assignment.<br>Provide continuous training and process improvements based on alert management metrics and feedback.                                                                                                                                                                                                                                               |
## Policy Statement

Effective management of the alert queue is critical to maintaining an efficient and responsive Security Operations Center (SOC). The SOC must ensure that all alerts are triaged, prioritized, and assigned to analysts for investigation in a timely and structured manner. Alerts should be addressed in order of priority, with High priority alerts receiving immediate attention and Medium and Low priority alerts being handled only after the higher-priority items are resolved. SOC leadership is responsible for overseeing the alert queue, ensuring sufficient resources are in place, and tracking key performance metrics related to alert volume, response times, and the resolution process. This policy ensures that alert investigation aligns with Service Level Objectives (SLOs) and that resources are utilized effectively, with the goal of addressing critical security incidents before less urgent issues.

### Policy Elements

#### 1. Alert Aggregation and Standardization

- Alerts may be produced from a number of data sources including, but not limited to:
    - Endpoint Detection and Response (EDR)
    - Email defense platforms
    - Firewalls
    - Data Loss Prevention (DLP) platforms
    - DNS security platforms
    - Identity defense tools
    - Web gateways and proxies
- Alerts should be aggregated in a Security Information and Event Management (SIEM) or Security Automation and ORchestration (SOAR) tool.
- SIEM or SOAR should standardize priority across tools and platforms to enforce a uniform, mutually agreed, priority
- SOC will action standardized priority alerts out of the SIEM or SOAR platform
- Tickets must reflect priority from the SIEM or SOAR
    - Ticket priority may be adjusted to reflect priority refinement and change through the course of investigations

#### 2. . Alert Priority and Triage

- Alerts will be grouped into three priority levels: High, Medium, and Low.
- **High Priority Alerts:**
    - These alerts must be addressed immediately and investigated first, as they represent the most urgent security concerns or potential threats.
    - High priority alerts should be assigned to analysts as soon as they become available to begin investigation.
- **Medium Priority Alerts:**
    - These alerts will only be addressed after all High priority alerts have been resolved.
    - Medium priority alerts may involve less critical issues but should still be investigated promptly to ensure no escalation or breach occurs.
- **Low Priority Alerts:**
    - These alerts are to be addressed after all High and Medium priority alerts have been handled.
    - Low priority alerts often represent less time-sensitive issues but must still be logged and investigated within reasonable timeframes.

#### 3. Queue Monitoring and Assignment

- The Shift Lead is responsible for continuously monitoring the alert queue to ensure timely triage and assignment based on priority.
- Tickets in the ticketing system must be created for each alert investigation. Related alerts should be grouped together into a single investigation ticket when appropriate.
- As SOC analysts become available, alerts should be assigned in priority order. If an analyst is unavailable, alerts should be reassigned to the next available analyst.    

#### 4. Service Level Objectives (SLOs)

- The SOC must ensure that alert response and resolution times meet the organization's established SLOs.
- SOC leadership will monitor performance against SLOs to ensure that alerts are investigated within the designated time frames and escalate to Incident Response (IR) as necessary if SLOs are at risk of being missed.

#### 5. Alert Handoff

- Alert priorities must be clearly communicated during shift handoffs to ensure that incoming analysts are aware of which alerts require immediate attention and which can be addressed later.
- The Shift Lead is responsible for ensuring that alert priorities are tracked across shifts and that handoff notes clearly outline the status of ongoing investigations.

#### 6. Workload Management and Escalation

- SOC leadership should continuously monitor alert volume and adjust resources as necessary to ensure proper alignment with alert priorities.
- In the event of overwhelming alert volume, SOC leadership must immediately alert SOC Leadership team for additional support.

#### 7. Metrics and Reporting

- SOC leadership will track key metrics related to alert queue management, including:
    - Total volume of alerts by priority level (High, Medium, Low).
    - Average response time for acknowledging and assigning alerts.
    - Time to resolution for each alert.
    - Metrics related to workload distribution across shifts.
- A weekly report will be created and reviewed by SOC leadership, highlighting areas for improvement, adherence to SLOs, and any trends that require attention.

#### 8. Audit and Continuous Improvement

- SOC leadership will regularly review alert management processes and performance metrics to identify opportunities for improvement.
- Process audits will be conducted periodically to ensure that the alert queue is being effectively managed and that SOC analysts are adhering to documented procedures.
- Feedback from SOC analysts and leadership will be used to continuously refine and improve the alert management process.

## Non-compliance

By adhering to this policy, the SOC will ensure that alerts are triaged and resolved efficiently, with a focus on addressing the highest priority issues first. This approach promotes the effective use of resources, supports timely incident response, and ensures that the SOC operates in alignment with the organization's security objectives. SOC Leadership is responsible for ensuring compliance with this policy.
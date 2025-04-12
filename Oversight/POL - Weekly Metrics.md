## Purpose
The purpose of this policy is to establish a standardized approach for defining, collecting, and reporting SOC metrics that clearly demonstrate operational value, identify areas for improvement, and support strategic security goals. Metrics are not merely numbers but tools for storytelling that align SOC activities with business outcomes and process maturity. This policy ensures that metrics are meaningful, actionable, and resistant to manipulation or misinterpretation.
## Scope
This policy applies to all SOC analysts, engineers, and managers responsible for monitoring, investigating, or reporting security events. It also applies to client engagement teams responsible for delivering regular reporting and insights, including the weekly client-facing metrics deck. The policy covers the development, maintenance, and use of SOC metrics across all customer environments.
## Roles and Responsibilities

| Role                   | Responsibility                                                                                                                                                                                                                                                                                                                                           |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Manager            | - Defines success criteria and desired outcomes for SOC metrics.<br>- Reviews and approves metrics to ensure alignment with strategic objectives.<br>- Oversees delivery of weekly metric reports to clients and internal stakeholders.<br>- Ensures metric data is stored in compliance with organizational documentation standards (e.g., SharePoint). |
| SOC Analyst            | - Accurately document investigative actions and outcomes in accordance with runbooks.<br>    <br>- Identify and report any gaps in data collection or metric tracking.<br>    <br>- Contribute to runbook updates and access request tracking.                                                                                                           |
| Detection Engineer     | - Support metrics that evaluate alert quality (e.g., signal-to-noise ratio).<br>    <br>- Collaborate with SOC to tune rules and reduce alert fatigue.                                                                                                                                                                                                   |
| Client Engagement Lead | - Present weekly metrics to clients in an understandable format.<br>    <br>- Work with client stakeholders to contextualize metrics and encourage improvements.<br>    <br>- Track client-side blockers (e.g., unresolved access requests, pending responses).                                                                                          |

## Policy Statement
The Security Operations Center (SOC) is committed to providing measurable, transparent, and actionable insights into its performance and effectiveness through a structured metrics program. This policy establishes the standards and practices for defining, collecting, analyzing, and reporting metrics that align with operational objectives, support client engagement, and drive continuous improvement.

SOC metrics shall be developed with a focus on outcomes, behavioral impacts, and process maturity, rather than on arbitrary or easily gamed data points. These metrics will enable the SOC to demonstrate value, identify inefficiencies, and communicate security posture in a meaningful way to internal and external stakeholders.

By adhering to this policy, the SOC ensures that metrics are used as a tool for operational accountability, client trust, and the advancement of a mature cybersecurity program.
### Policy Elements

### **A. Principles of Effective SOC Metrics**
1. **Outcome-Driven**: Metrics must be tied to specific operational or strategic outcomes, such as improved detection fidelity or investigation throughput.
2. **Behaviorally Aware**: Metrics should be designed to avoid perverse incentives, such as rewarding premature case closure or superficial alert acknowledgments.
3. **Story-Oriented**: Each metric should support a “success story” or highlight an area of concern, such as:
    - SOC responsiveness and alert monitoring efficiency.
    - Adherence to standardized investigative procedures.
    - Integration with threat intelligence and incident management workflows.
    - Evidence of partnership and responsiveness with internal customer teams.
### **B. Initial Metrics Baseline**
SOC teams should maintain a baseline set of metrics that can be proposed to clients when establishing a reporting program:

- **Alert Volume**
    - Total number of alerts per week.
    - Week-over-week trends.
    - Breakdown by severity (High, Medium, Low) with historical trends.
- **Alert Source Quality**
    - Alert-to-detection rule ratio (volume per detection).
    - Identification of high-volume or high-severity rules.
- **Investigative Activity**
    - Number of investigations initiated and closed during the week.
    - List of high-severity alerts with investigation and resolution notes.
    - Investigations that remain open beyond defined thresholds (e.g., 7 days)
- **Operational Blockers**
    - Investigations blocked due to client dependencies (e.g., unresolved access requests).
    - Aged access requests including system name and request age.
    - Tickets or case numbers to facilitate client-side follow-up.
- **Runbook and Process Maturity**
    - Number of runbooks created or updated during the week.
    - Cases aligned to documented investigative workflows.
### **C. Metrics Reporting**

- Metrics will be compiled and delivered via a **Weekly Client Metrics Deck**.
- The deck must be:
    - Presented in a format easily understandable to non-technical stakeholders.
    - Delivered on a recurring cadence agreed upon with the client.
    - Stored in a secure location such as the designated SharePoint repository.
### **D. Continuous Improvement**
- Metrics will be periodically reviewed to ensure relevance and accuracy.
- Feedback from client engagements and operational retrospectives will inform metric evolution.
- Metrics may be expanded to highlight anti-patterns and inefficiencies, such as:
    - Excessive alert noise due to untuned detections.
    - Investigation delays stemming from insufficient system access.
## Enforcement and Compliance
compliance statement

## Policy Review
This policy will be reviewed annually by all employees to ensure its continued relevance and effectiveness. Feedback and suggestions for improvement are welcome and should be directed to the SOC Leadership.

Effective Date:

|Last Reviewed By     | Date    |
| --- | --- |
|     |     |

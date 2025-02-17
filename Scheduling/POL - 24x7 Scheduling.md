## Purpose

The purpose of this policy is to ensure continuous, around-the-clock (24x7) monitoring, investigation, and escalation of cybersecurity threats by the Security Operations Center (SOC). Maintaining full coverage is essential for cybersecurity posture, requiring adequate staffing, contingency planning, and coordination with cybersecurity leadership and other teams.

## Scope

This policy applies to all SOC personnel, including SOC analysts, Shift Leads, and SOC leadership. It governs shift scheduling, alert queue monitoring, workload management, coordination with cybersecurity teams, and compliance with service-level agreements (SLAs) for security-related requests.

## Roles and Responsibilities

| Role                     | Responsibility                                                                                                                                                |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SOC Analyst              | - Responsible for maintaining access to required tools, managing alert queues, completing mandatory training, and escalating incidents as needed.             |
| Shift Lead               | - Monitor queue volumes, notify cybersecurity leadership of untenable workloads (queue flooding)<br>- Ensure proper staffing for each shift.                  |
| SOC Leadership           | - Ensure proper scheduling, workload monitoring, contingency planning, and communication with Cybersecurity Leadership regarding staffing and coverage risks. |
| Cybersecurity Leadership | - Receive and respond to SOC notifications about coverage risks, staffing changes, and incident escalations.                                                  |
### Policy Statement

The SOC must maintain 24x7 coverage to ensure the security of the organization’s digital environment. Leadership must ensure proper staffing, contingency planning, and communication of any risks or gaps in coverage. SOC Shift Leads and analysts must adhere to this policy to guarantee seamless monitoring, investigation, and response to security incidents.Policy Elements

#### 1. Full Coverage Requirements

- The SOC must maintain 24x7 coverage for alert queue monitoring, investigations, and escalations.
- SOC Shift Leads must ensure alert queues are actively monitored at all times.
- SOC must ensure adequate coverage despite scheduled meetings or other business-related activities.
- At minimum, 2 persons must be staffed on shift every shift
    - Either 2 SOC analysts and one Senior Analyst on-call capable of responding within 30 minutes
    - or 1 SOC analyst and 1 Senior Analyst actively on shift to respond

#### 2. Scheduling and Contingency Planning

- SOC leadership must ensure scheduling adequately supports full coverage.
- Workloads must be monitored over time to determine appropriate staffing levels.
- Contingency plans must be developed for SOC analyst unavailability and communicated to cybersecurity leadership.
- Any risk to coverage must be reported to cybersecurity leadership immediately.

#### 3. Incident Response and Coordination

- SOC Shift Leads must monitor queue volumes and notify cybersecurity leadership of untenable workloads (queue flooding).
- SOC should maintain "burst coverage" capabilities for handling sudden increases in workload.

#### 4. Staffing Management and Onboarding

- SOC must notify cybersecurity leadership of staffing changes to onboard or offboard resources as necessary.
    - Cybersecurity leadership must notify IT and HR within **24 hours** of any departing SOC member, especially in cases of non-regretable termination, in order to promptly disable credentials and access.
    - IT must be notified at least **2 weeks** in advance of any new SOC hire in order to ensure adequate time to secure credentials and access for shift coverage.
- SOC leadership must develop and communicate holiday coverage plans and contingencies.
- New SOC analysts must be onboarded and trained to provide adequate coverage.  
	- Senior analysts must support new analysts on shift until they can operate independently.

#### 5. Access and Credential Maintenance

- SOC analysts must maintain access to required security tools and systems.  
    Analysts must ensure credential maintenance and completion of mandatory training to retain system access.
- Upon request, the SOC must provide a list of current staff on shift, including designated Shift Leads and any Senior Analyst resources on duty.
- The SOC must maintain access to necessary engineering resources to meet SLAs for email, web, and network-related security requests.

#### 6. Alert Queue Management and Downtime Activities

- During shifts, SOC analysts must manage alert queues in accordance with [[POL - Alert Queue Management]]
- If no active alerts require attention, SOC analysts must utilize downtime for ticket review, training, threat hunting, or professional development.

## Non-compliance

This policy ensures that the SOC operates efficiently and effectively, maintaining a robust cybersecurity posture through continuous monitoring and rapid incident response. Non-compliance could result in serious risk. Violation of this policy could lead to disciplinary action.
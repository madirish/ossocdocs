## Purpose
The purpose of this policy is to ensure consistency and accuracy in the reporting of cybersecurity incidents by mandating the use of Coordinated Universal Time (UTC) for all timestamps. By adopting UTC as the standard time reference, this policy facilitates the correlation of events across different time zones, enhances the accuracy of event timelines, and improves the effectiveness of incident response efforts.
## Scope
This policy applies to all members of the Security Operations Center (SOC) and Incident Response (IR) teams, as well as any personnel involved in the investigation and reporting of cybersecurity incidents within the organization.
## Roles and Responsibilities

| Role          | Responsibility                                                                                             |
| ------------- | ---------------------------------------------------------------------------------------------------------- |
| SOC Analyst   | Ensuring that all timestamps in investigation reports are converted to UTC in accordance with this policy. |
| SOC Engineers | Responsible for configuring systems and tools to generate logs and timestamps in UTC format.               |

## Policy Statement
All investigation reports, documentation, and communication related to cybersecurity incidents must utilize Coordinated Universal Time (UTC) for timestamping purposes. Local time zones should not be used, except where specifically required for contextual purposes, and must be clearly indicated alongside the UTC timestamp.
### Policy Elements
#### 1. Conversion to UTC

All timestamps must be converted from local time to UTC before inclusion in investigation reports.

#### 2. Standard Format

UTC timestamps should be presented in a standard format (e.g., YYYY-MM-DD HH:MM:SS UTC). 

#### 3. Day Format

Dates should be recorded using DD Month YYYY format (e.g. 23 February 2024) to disambiguate the date and recognize the difference between month and day precedence across the world.

#### 4. Consistency

Ensure consistency in the use of UTC throughout all stages of the investigation process, from data collection to reporting.

#### 5. Documentation

Document the methodology used for converting timestamps to UTC and any deviations from standard procedures.

#### 6. Tool Setup

All standard SOC tools should be configured with UTC as the default timezone for ease of standardization and correlation across tool sets.

## Enforcement and Compliance
Failure to adhere to this policy may result in:

- Compromised accuracy and reliability of investigation reports.
- Difficulty in correlating events and timelines accurately.
- Delayed incident response and resolution.
- Disciplinary action in accordance with organizational policies and procedures.

## Policy Review
This policy will be reviewed annually by all employees to ensure its continued relevance and effectiveness. Feedback and suggestions for improvement are welcome and should be directed to the SOC Leadership.

Effective Date:

|Last Reviewed By     | Date    |
| --- | --- |
|     |     |

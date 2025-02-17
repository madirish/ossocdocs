## Purpose
The purpose of this document is to establish a structured process for communicating changes within the Security Operations Center (SOC) in a consistent and effective manner. This process ensures that all SOC analysts are aware of relevant changes, understand their implications, and have access to necessary training and documentation. The principle of "at least three times, in at least three ways" is used to reinforce awareness and ensure no critical updates are missed.
## Scope
This process applies to all changes affecting SOC operations, including but not limited to:

- Updates to security tools and technologies
- Changes in incident response procedures
- Modifications to monitoring and alerting rules
- Adjustments in shift schedules or team structures
- Introduction of new policies and compliance requirements

All SOC analysts, engineers, and relevant stakeholders must adhere to this process to maintain consistency in change communication.
## Related Content
* [[POL - Change Notifications]]
## Prerequisites
* Access to dedicate email
* Access to instant messaging
* Invitation to Shift Handoffs and Team Meetings
## Roles and Responsibilities

| Role             | Responsibility                                                                                                                                                                                                                                                                       |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Change Initiator | Document the change details including purpose, rationale, and impact assessment.<br>Prepare any necessary training materials.<br>Develop test harnesses as applicable.<br>Create a rollback plan in case of unintended impacts.<br>Coordinate with SOC leadership for communication. |
| SOC Leadership   | Review and approve changes.<br>Ensure communications plan for changes is followed.<br>Tracks acknowledgment from SOC analysts.<br>Review SOC analyst behavior to ensure compliance with the change.                                                                                  |
| SOC Analyst      | Monitor communications for change announcements.<br>Acknowledge all changes.<br>Participate in required training and review associated documentation.                                                                                                                                |
## **Process Steps**

### **Step 1: Document the Change**

- The Change Initiator drafts a formal change description, including:
    - Nature of the change
    - Justification and expected impact
    - Effective date
    - Required actions for SOC analysts
    - References to supporting documentation and training materials

### **Step 2: Internal Approval and Preparation**

- The Change Initiator submits the change document to the SOC Leadership Team.
- Leadership reviews the change for clarity and completeness.
- Necessary training materials are finalized.

### **Step 3: Communicate the Change (Three Times, Three Ways)**

1. **Verbal Announcement:**
    - Communicate during SOC shift handoff meetings.
    - Announce at the next team meeting or stand-up.
2. **Chat Notification:**
    - Post the change details in a dedicated chat channel (e.g., "#SOC-Change-Alerts").
    - Tag relevant team members to ensure visibility.
3. **Email Notification:**
    - Send an email to the SOC distribution list with the subject line formatted as:
        - **[SOC CHANGE NOTICE] [Brief Change Summary] [Effective Date]**
    - The body should include:
        - Summary of the change
        - Links to documentation, training materials, or videos
        - Actions required by SOC analysts
        - Contact details for questions

### **Step 4: Acknowledgment and Tracking**

- Analysts must acknowledge receipt via one of the following methods:
    
    - Reply to the email with "Acknowledged."
    - Mark acknowledgment in a tracking document (e.g., SharePoint, Confluence, or ticketing system).
    - Confirm in the chat channel dedicated to SOC change communications.
- SOC Leadership monitors acknowledgments and follows up with those who have not responded.

### **Step 5: Training and Support**

- Analysts review and complete any required training materials.
- A follow-up Q&A session is held if necessary.
- Any feedback or issues related to the change are logged for continuous improvement.

### **Step 6: Continuous Monitoring and Adjustments**

- SOC Leadership ensures proper adoption of the change.
- Any unforeseen issues or challenges are addressed and, if necessary, additional communications and training are provided.
- Lessons learned are documented for future process improvements.
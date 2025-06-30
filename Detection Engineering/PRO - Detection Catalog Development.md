## Purpose
The purpose of this document is to define a structured, iterative process for developing a comprehensive detection catalog to support Security Operations Center (SOC) monitoring and incident response. This process prioritizes early-stage threat detection aligned with the cyber kill chain, ensuring effective visibility into reconnaissance and initial access tactics before extending coverage to subsequent attack stages. The detection catalog serves as a foundational reference for detection coverage, detection fidelity, and strategic improvement.

## Scope
This process applies to the Detection Engineering team and related stakeholders contributing to the creation, validation, and enhancement of detection capabilities. It includes detection rule inventorying, gap analysis, rule development, validation via adversary simulation, and catalog maintenance across all supported security platforms and telemetry sources. The process is designed to start from zero coverage and expand iteratively.

## Roles and Responsibilities

| Role                       | Responsibility                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Detection Engineering Team | Owns and maintains the detection catalog<br>Maps out-of-the-box (OOTB) and custom detection rules to the MITRE ATT&CK framework<br>Prioritizes detection rule development according to cyber kill chain order: reconnaissance, initial access, execution, persistence, etc.<br>Develops high-fidelity, low-noise detection logic<br>Coordinates validation efforts with Red, Purple, and Threat Hunt teams |
| Adversary Emulation Teams  | Provides insight into real-world adversary techniques and TTPs<br><br>Designs and executes controlled simulations to test and validate detections<br><br>Shares adversary tradecraft trends for incorporation into detection planning                                                                                                                                                                      |
| Threat Hunt Teams          | Informs the detection roadmap with insights from proactive hunting activities<br><br>Aligns threat hunting efforts with early kill chain detection priorities<br><br>Validates and improves detection rules based on observed threat behaviors                                                                                                                                                             |
## Process Steps


#### 1.  Initialize the Detection Catalog Structure
- Define catalog schema including fields such as: rule ID, ATT&CK tactic/technique, detection logic summary, platform, telemetry source, validation status, and false positive rate.
- Establish version control and documentation standards for catalog entries.
- Create a centralized, access-controlled location for catalog storage (e.g., internal wiki, SIEM content repository).

#### 2.  Baseline with Out-of-the-Box Detection
- Inventory all OOTB detection rules provided by security technologies (EDR, SIEM, WAF, NIDS, etc.).
- Map OOTB rules to MITRE ATT&CK techniques and assign initial heat map values.
- Document coverage gaps, redundancy, and limitations of vendor-provided rules.

#### 3.  Prioritize by Kill Chain Phase
- Focus detection development first on reconnaissance and initial access tactics, per cyber kill chain guidance.
- Use threat intelligence and recent incident trends to support priority setting.
- Define clear entry and exit criteria for each kill chain phase (e.g., 80% ATT&CK sub-technique coverage before advancing).

#### 4.  Iterative Rule Development
- Select high-priority gaps and draft detection logic with available telemetry.
- Implement detections in test environments where possible before production deployment.
- Ensure rules are tuned for fidelity (low false positives, high signal) and include detection rationale, context enrichment, and response recommendations.

#### 5.  Simulated Adversary Validation
- Partner with Red and Purple Teams to emulate relevant TTPs in controlled environments.
- Evaluate detection triggers and alert quality.
- Iterate on logic to improve detection precision and reliability.
- Update catalog entries with validation results, detection fidelity ratings, and adversary simulation artifacts.

#### 6.  Feedback from Threat Hunting
- Review threat hunt findings for missed detection opportunities.
- Integrate learned behaviors or anomalous patterns into new or refined detection rules.
- Adjust prioritization if repeated hunt patterns indicate early kill chain activity not yet covered.

#### 7.  Periodic Heat Map Reassessment
- Re-map catalog entries to MITRE ATT&CK monthly or quarterly.
- Generate and review updated coverage heat maps with Detection Engineering leadership.
- Use findings to adjust development roadmap and resource allocation.

#### 8.  Catalog Maintenance and Quality Assurance
- Periodically retire obsolete rules and refactor detection logic as telemetry or platforms evolve.
- Track detection rule performance, including false positives and alert volume over time.
- Maintain alignment with organizational threat model and risk landscape.

#### 9.  Reporting and Communication
- Regularly brief SOC leadership and stakeholders on detection coverage progress.
- Share roadmap, recent additions, simulation results, and outstanding gaps.
- Maintain transparency and alignment with organizational cybersecurity priorities.

#### Best Practices

- Anchor detection priorities in threat intelligence and real adversary behavior.
- Avoid overfitting rules to simulations—maintain general applicability.
- Encourage collaboration across detection, hunt, and adversary emulation teams to accelerate validation cycles.
- Document everything for repeatability, audit readiness, and team continuity.

This process ensures a deliberate, prioritized, and high-fidelity approach to detection catalog development, enabling SOC analysts to detect and respond to threats early and with confidence.
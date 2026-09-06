# GDPR + Cybersecurity — Data Protection Impact Assessment

## Overview
This project demonstrates how privacy requirements can be integrated into cybersecurity risk management through a Data Protection Impact Assessment (DPIA).

**Scenario:** A fictional cloud-based healthcare application processes personal and health-related data for patients in the European Economic Area.

**Frameworks/concepts:** GDPR principles, privacy by design, DPIA, data minimization, access control, encryption, retention, incident response, vendor risk, and security of processing.

> **Disclaimer:** This is an educational case study and not legal advice. No real personal data is used.

## 1. Processing Activity
**Application:** CareCloud Connect (fictional)

The application allows patients to:
- Create an account.
- View health-related information.
- Communicate with providers.
- Upload documents.
- Receive notifications.

### Categories of data
- Identity/contact information
- Account credentials
- Health-related information
- Appointment information
- Technical and usage data

## 2. Privacy Risks

| ID | Privacy risk | Likelihood | Impact | Risk |
|---|---|---:|---:|---|
| P01 | Unauthorized access to sensitive data | Medium | Very High | High |
| P02 | Excessive data collection | Medium | High | High |
| P03 | Excessive retention | Medium | High | High |
| P04 | Third-party processor breach | Medium | Very High | High |
| P05 | Inaccurate or outdated information | Low/Medium | High | Medium/High |
| P06 | Insufficient transparency | Medium | Medium | Medium |

## 3. GDPR Principles Applied

### Data minimization
Collect only data necessary for defined purposes.

### Purpose limitation
Use information only for specified and legitimate purposes.

### Accuracy
Provide mechanisms for correcting inaccurate personal information.

### Storage limitation
Define retention periods and secure deletion procedures.

### Integrity and confidentiality
Protect data against unauthorized access, loss, alteration, or disclosure.

### Accountability
Maintain evidence demonstrating that privacy and security requirements are being implemented.

## 4. Privacy by Design Security Controls

### Identity and Access
- MFA.
- RBAC.
- Least privilege.
- Privileged-access controls.
- Periodic access reviews.

### Data Protection
- Encryption in transit.
- Encryption at rest.
- Secure key management.
- Data classification.

### Application Security
- Secure development lifecycle.
- Vulnerability scanning.
- Dependency management.
- Security testing.
- Secure API authentication.

### Monitoring
- Centralized security logs.
- Access monitoring.
- Detection of anomalous activity.
- Incident escalation procedures.

## 5. Retention and Deletion
The organization should define retention periods based on documented legal, operational, and business requirements.

Controls should include:
- Retention schedules.
- Automated deletion where appropriate.
- Secure deletion procedures.
- Periodic review of stored data.
- Documentation of exceptions.

## 6. Third-Party Processor Risk
Before engaging a cloud or technology provider:
- Identify what personal data the processor will access.
- Evaluate security controls.
- Review contractual requirements.
- Assess international data-transfer implications when applicable.
- Establish breach-notification procedures.
- Monitor material providers.

## 7. Incident Scenario
**Scenario:** A cloud storage configuration exposes a database containing personal and health-related information.

### Response
1. Contain the exposure.
2. Preserve evidence and logs.
3. Identify affected data and individuals.
4. Determine the scope and duration.
5. Assess risk to individuals.
6. Escalate to privacy and security teams.
7. Determine applicable notification obligations.
8. Remediate the configuration.
9. Document the incident and lessons learned.

## 8. DPIA Conclusion
The highest risks are unauthorized access, third-party compromise, and excessive collection/retention of sensitive data.

The recommended risk-reduction strategy combines:
- privacy by design;
- strong identity controls;
- encryption;
- data minimization;
- retention management;
- vendor risk management;
- continuous monitoring;
- incident response.

## 9. Professional Relevance
This project demonstrates the intersection of:

**Law + Privacy + Cybersecurity + Risk Management + Governance**

That intersection is the area in which I intend to develop professionally.

My legal background and experience working with sensitive healthcare and regulated information provide a foundation for translating privacy and regulatory requirements into practical information-security controls.

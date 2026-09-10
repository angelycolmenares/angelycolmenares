# Cyber Risk Assessment — Insurance Company

## Overview
This project demonstrates a structured cybersecurity risk assessment for a fictional U.S. insurance company. The assessment applies risk-management concepts to a regulated environment and focuses on identifying information-security risks, evaluating their potential impact, and recommending appropriate controls.

**Frameworks and concepts:** NIST Cybersecurity Framework (CSF), risk assessment, security controls, least privilege, MFA, data protection, incident response, and third-party risk.

> **Disclaimer:** This is an educational case study based on a fictional organization. No confidential or proprietary employer information is used.

## 1. Organization Profile
**Organization:** SecureShield Insurance (fictional)  
**Industry:** Health and property insurance  
**Employees:** 500  
**Environment:** Cloud-based applications, employee laptops, CRM, claims platform, email, and third-party service providers.

### Critical assets
- Customer personally identifiable information (PII)
- Health information handled by the organization or its partners
- Claims and policy records
- Employee credentials
- Financial and payment information
- Customer-facing applications
- Backups and security logs

## 2. Risk Assessment Method
Risk is evaluated using:

**Risk = Likelihood × Impact**

| Rating | Likelihood | Impact |
|---|---|---|
| 1 | Rare | Minimal |
| 2 | Unlikely | Low |
| 3 | Possible | Moderate |
| 4 | Likely | High |
| 5 | Almost certain | Critical |

Risk score:
- 1–4: Low
- 5–9: Moderate
- 10–16: High
- 17–25: Critical

## 3. Risk Register

| ID | Risk | Likelihood | Impact | Score | Priority |
|---|---|---:|---:|---:|---|
| R01 | Phishing leading to credential compromise | 4 | 5 | 20 | Critical |
| R02 | Excessive user privileges | 4 | 4 | 16 | High |
| R03 | Ransomware affecting claims systems | 3 | 5 | 15 | High |
| R04 | Third-party vendor data breach | 3 | 5 | 15 | High |
| R05 | Unpatched endpoint vulnerability | 3 | 4 | 12 | High |
| R06 | Lost or stolen employee device | 3 | 4 | 12 | High |

## 4. Recommended Controls

### R01 — Phishing / credential compromise
- Enforce MFA for all workforce accounts.
- Implement phishing-resistant authentication where feasible.
- Conduct security-awareness training.
- Deploy email filtering and anti-phishing controls.
- Monitor authentication anomalies.

### R02 — Excessive privileges
- Apply least privilege.
- Implement role-based access control (RBAC).
- Conduct quarterly access reviews.
- Remove dormant accounts promptly.
- Separate privileged administration from standard user accounts.

### R03 — Ransomware
- Maintain offline or immutable backups.
- Segment critical systems.
- Establish tested incident-response procedures.
- Deploy endpoint detection and response.
- Regularly test restoration procedures.

### R04 — Third-party risk
- Perform vendor security due diligence.
- Include security and breach-notification requirements in contracts.
- Review SOC 2/ISO 27001 evidence when appropriate.
- Classify vendors according to data sensitivity and business impact.
- Monitor high-risk vendors continuously.

### R05 — Vulnerability management
- Maintain an accurate asset inventory.
- Prioritize remediation according to severity and business impact.
- Establish patching SLAs.
- Validate remediation through rescanning.

### R06 — Lost or stolen devices
- Encrypt endpoints.
- Require strong authentication.
- Enable remote lock/wipe.
- Maintain an asset-management process.

## 5. NIST CSF Alignment

| Function | Example activity |
|---|---|
| Govern | Define security responsibilities, policies, and risk appetite |
| Identify | Maintain asset inventory and risk register |
| Protect | MFA, least privilege, encryption, training |
| Detect | Logging, monitoring, alerting |
| Respond | Incident-response plan and communications |
| Recover | Backups, restoration testing, lessons learned |

## 6. Risk Treatment Priorities
1. Reduce phishing and account-compromise risk.
2. Strengthen identity and access management.
3. Improve ransomware resilience.
4. Formalize third-party risk management.
5. Strengthen vulnerability-management processes.
6. Improve endpoint protection.

## 7. Key Takeaways
This assessment demonstrates that cybersecurity risk is not purely technical. Effective risk management requires governance, documented controls, regulatory awareness, business context, and continuous monitoring.

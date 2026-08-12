# Controls and Compliance Checklist — Botium Toys Security Audit

## Overview
As part of an internal IT security audit for **Botium Toys**, a small U.S.-based toy company with growing international online sales, I conducted a controls and compliance assessment using the NIST Cybersecurity Framework (NIST CSF). The goal was to evaluate the company's current security posture and identify risks related to compliance with PCI DSS, GDPR, and SOC standards.

## Controls Assessment Checklist

| Control | In Place? | Explanation |
|---|---|---|
| Least Privilege | ❌ No | All employees currently have access to customer data; access needs to be limited to reduce breach risk. |
| Disaster Recovery Plans | ❌ No | No disaster recovery plan exists; needed to ensure business continuity. |
| Password Policies | ❌ No | Password requirements are minimal, increasing risk of unauthorized access. |
| Separation of Duties | ❌ No | The CEO currently manages both daily operations and payroll, increasing fraud risk. |
| Firewall | ✅ Yes | Existing firewall blocks traffic based on defined security rules. |
| Intrusion Detection System (IDS) | ❌ No | No IDS in place to identify potential intrusions. |
| Backups | ❌ No | No backups of critical data exist to ensure continuity after a breach. |
| Antivirus Software | ✅ Yes | Installed and monitored regularly by the IT department. |
| Legacy System Monitoring | ⚠️ Partial | Legacy systems are monitored, but no regular schedule or clear intervention policy exists. |
| Encryption | ❌ No | Not currently used; needed to protect sensitive information. |
| Password Management System | ❌ No | No system in place to support password management. |
| Physical Locks (office/store/warehouse) | ✅ Yes | Sufficient locks are in place at the physical location. |
| CCTV Surveillance | ✅ Yes | Installed and functioning at the physical location. |
| Fire Detection/Prevention | ✅ Yes | Functioning fire alarm and sprinkler systems in place. |

## Compliance Checklist

### PCI DSS (Payment Card Industry Data Security Standard)

| Best Practice | Compliant? | Explanation |
|---|---|---|
| Only authorized users access credit card data | ❌ No | All employees currently have access to internal data. |
| Credit card data securely stored/processed | ❌ No | Data is not encrypted; all employees have access. |
| Data encryption implemented | ❌ No | No encryption used to secure transaction touchpoints. |
| Secure password management adopted | ❌ No | Password policies are minimal; no management system exists. |

### GDPR (General Data Protection Regulation)

| Best Practice | Compliant? | Explanation |
|---|---|---|
| E.U. customer data kept private/secured | ❌ No | No encryption used to protect financial information. |
| 72-hour breach notification plan in place | ✅ Yes | Plan exists to notify E.U. customers within 72 hours. |
| Data properly classified and inventoried | ⚠️ Partial | Assets are inventoried but not classified. |
| Privacy policies enforced | ✅ Yes | Policies and processes are developed and enforced among staff. |

### SOC (System and Organization Controls)

| Best Practice | Compliant? | Explanation |
|---|---|---|
| User access policies established | ❌ No | Least Privilege and separation of duties are not in place. |
| Sensitive data (PII/SPII) kept confidential | ❌ No | No encryption used to protect PII/SPII. |
| Data integrity maintained | ✅ Yes | Data is consistent, complete, accurate, and validated. |
| Data available to authorized individuals | ⚠️ Partial | Data is accessible to all employees, not limited to those who need it. |

## Recommendations

Botium Toys should prioritize implementing the following controls to strengthen its security posture:

- **Least Privilege** access controls
- **Disaster recovery plan**
- **Stronger password policies** and a password management system
- **Separation of duties**, especially between operational and financial responsibilities
- **Intrusion Detection System (IDS)**
- **Regular legacy system monitoring schedule**
- **Data encryption** for sensitive and financial information

To close compliance gaps with **PCI DSS**, **GDPR**, and **SOC** standards, the company should also classify its data assets and restrict access based on job function, in addition to encrypting sensitive information across all systems.

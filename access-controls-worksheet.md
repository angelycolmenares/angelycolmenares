# Access Controls Worksheet

## Purpose
This worksheet documents an authorization/authentication issue identified during a security review, following the Identity and Access Management (IAM) principles of least privilege and separation of duties.

## Access Controls Analysis

| Category | Note(s) | Issue(s) | Recommendation(s) |
|---|---|---|---|
| **Authorization / Authentication** | - The event was identified on 11/14/23.<br>- The user account belongs to a former contractor in the Finance department.<br>- The login originated from IP address 203.0.113.42, outside the company's usual network range. | - The contractor's account was never deprovisioned after their contract ended in early 2023.<br>- The account still had access to financial reporting systems, despite no longer being an active employee. | - Implement automatic account deprovisioning tied to HR contract end dates.<br>- Enforce periodic (e.g., quarterly) access reviews for all contractor and vendor accounts.<br>- Require multi-factor authentication (MFA) for any access to financial systems. |

## Key IAM Concepts Applied
- **Least Privilege:** Users should only have the minimum access needed to perform their role — this incident shows what happens when that principle isn't maintained after a role changes.
- **Separation of Duties:** Access to sensitive systems (like financial reporting) should require distinct, monitored authorization paths.
- **User Deprovisioning:** A critical but often overlooked IAM practice — removing access as soon as it's no longer needed, not after an incident reveals the gap.

## Reflections/Notes
This exercise reinforced that access control isn't a "set it and forget it" process. Even well-designed authorization frameworks (MAC, DAC, RBAC) fail if provisioning and deprovisioning aren't actively maintained as employment or contract status changes.

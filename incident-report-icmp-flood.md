# Incident Report Analysis — ICMP Flood DoS Attack

## Overview
As a cybersecurity analyst, I applied the NIST Cybersecurity Framework (CSF) to analyze a denial of service (DoS) incident affecting a multimedia company offering web design, graphic design, and social media marketing services. This report summarizes the event and outlines an improved security strategy across the five NIST CSF functions: Identify, Protect, Detect, Respond, and Recover.

## Summary
The company experienced a security event in which network services suddenly stopped responding. The cybersecurity team identified the cause as a denial of service (DoS) attack carried out through a flood of incoming ICMP packets, sent through an unconfigured firewall. The incident disrupted the internal network for two hours. The incident management team responded by blocking incoming ICMP packets, taking non-critical network services offline, and restoring critical network services.

## Identify
A malicious actor exploited an unconfigured firewall to launch an ICMP flood, a type of DoS attack, against the organization's network. The attack overwhelmed network resources, preventing normal internal traffic from accessing critical assets. The entire internal network was affected for the duration of the incident, and the firewall misconfiguration was identified as the root vulnerability that allowed the attack to succeed.

## Protect
To better protect the network going forward, the team implemented a new firewall rule to limit the rate of incoming ICMP packets, closing the configuration gap that was exploited. An IDS/IPS system was also deployed to filter ICMP traffic based on suspicious characteristics. Going forward, the organization should also conduct regular firewall configuration audits and enforce least privilege access on network devices to reduce the chance of similar misconfigurations going unnoticed.

## Detect
The team configured source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets, since spoofing is often used to disguise the origin of flood-based attacks. Network monitoring software was also implemented to detect abnormal traffic patterns, such as unusually high volumes of ICMP requests, in real time. Ongoing monitoring of authorized versus unauthorized traffic and regular review of firewall/IDS logs will help the team catch similar activity earlier in future incidents.

## Respond
For future incidents, the team will immediately isolate affected systems and block malicious traffic at the firewall to contain the attack. Non-critical services will be taken offline first to preserve resources for critical systems, which will be prioritized for restoration. The team will analyze network and firewall logs to determine the attack's source, scope, and method. All incidents will be documented and reported to upper management, and to appropriate legal or regulatory authorities if customer data or business operations were materially affected.

## Recover
To recover from an ICMP flood DoS attack, access to network services must be restored to normal functioning. External ICMP flood traffic should continue to be blocked at the firewall using the rate-limiting rule already in place. Non-critical services should remain offline temporarily to reduce internal load, while critical services are restored first. Once malicious traffic has subsided and systems are confirmed stable, non-critical services can be brought back online. A post-incident review should also be conducted to confirm the firewall configuration gap has been fully closed.

## Reflections/Notes
This incident highlights how a single misconfigured firewall rule created an exploitable gap, even though other controls (like the firewall itself) were technically in place. It reinforces that hardening isn't a one-time setup — regular configuration reviews and monitoring are what actually catch these gaps before attackers do.

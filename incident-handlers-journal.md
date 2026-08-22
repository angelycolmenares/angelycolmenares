# Incident Handler's Journal

## Instructions
This journal is used to document findings after completing cybersecurity activities, and to record key takeaways about tools and concepts encountered throughout the course.

---

## Entry #1

**Date:** August 18, 2026

**Description**
Documenting a ransomware incident that disrupted operations at a healthcare clinic. This incident spans two phases of the NIST Incident Response Lifecycle: **Detection and Analysis**, when the organization first identified the encrypted files and ransom note, and **Containment, Eradication, and Recovery**, when the clinic shut down affected systems and reached out to external organizations for assistance.

**Tool(s) used**
None — this entry documents the incident narrative rather than a specific tool.

**The 5 W's**
- **Who:** An organized cybercriminal group known for targeting healthcare and transportation organizations.
- **What:** A ransomware attack that encrypted critical patient files and displayed a ransom demand.
- **Where:** Internal systems of a small U.S. primary-care healthcare clinic.
- **When:** Tuesday, approximately 9:00 a.m.
- **Why:** Attackers gained access through a phishing email with a malicious attachment. Once opened, malware was installed and ransomware was later deployed. The ransom demand suggests financial motivation.

**Additional notes**
1. What email filtering controls were in place before this incident, and were they sufficient?
2. Would restoring from backups be faster and safer than engaging with the attackers at all?

---

## Entry #2

**Date:** August 19, 2026

**Description**
Analyzing network traffic using a packet capture tool to understand normal versus suspicious communication patterns. This falls under the **Detection and Analysis** phase, since packet analysis is a core method for identifying anomalous network behavior.

**Tool(s) used**
For this activity, I used **Wireshark** to inspect a packet capture (.pcap) file. Wireshark is a graphical network protocol analyzer that lets analysts drill into individual packets, filter traffic by protocol or IP, and reconstruct communication sessions. It's especially useful for spotting unusual traffic patterns, such as unexpected outbound connections or unencrypted transmission of sensitive data.

**The 5 W's**
N/A — this entry focuses on tool usage rather than a specific incident.

**Additional notes**
The sheer volume of packets in a live capture was overwhelming at first. Learning to apply display filters (like isolating traffic by IP or port) made the tool far more manageable and showed me how much noise exists in normal network traffic.

---

## Entry #3

**Date:** August 20, 2026

**Description**
Capturing live network traffic directly from the command line to practice a lower-level approach to traffic analysis. This also falls under **Detection and Analysis**, as capturing traffic is often the first step before deeper investigation.

**Tool(s) used**
For this activity, I used **tcpdump**, a command-line packet analyzer. Unlike Wireshark's graphical interface, tcpdump requires writing specific syntax to capture and filter traffic directly from the terminal. It's lightweight and commonly used on servers without a graphical interface, making it valuable for analysts working in remote or headless environments.

**The 5 W's**
N/A — this entry focuses on tool usage rather than a specific incident.

**Additional notes**
Working entirely from the command line was a bigger adjustment than I expected. I made a few syntax errors early on, but troubleshooting them helped me understand tcpdump's filtering logic much better than if it had worked correctly on the first try.

---

## Entry #4

**Date:** August 21, 2026

**Description**
Investigating a suspicious file hash flagged by an intrusion detection system at a financial services company. This incident falls under the **Detection and Analysis** phase — the IDS alert triggered the investigation, and further analysis was needed to confirm whether the file was genuinely malicious.

**Tool(s) used**
For this activity, I used **VirusTotal**, an online tool that scans files, URLs, and hashes against multiple antivirus engines and security vendor databases. It allows analysts to quickly check whether a file hash has already been identified as malicious by the security community, and to uncover related indicators of compromise like associated IP addresses, domains, and behavioral data from sandbox reports.

**The 5 W's**
- **Who:** An unidentified threat actor.
- **What:** A password-protected spreadsheet attachment containing a malicious payload, identified by SHA256 hash `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`.
- **Where:** An employee's workstation at a financial services company.
- **When:** IDS alert triggered at 1:20 p.m., following file download and execution at 1:13 p.m.
- **Why:** The attacker used social engineering (providing the password in the email itself) to convince the employee to open the file, bypassing suspicion that a password-protected file might raise.

**Additional notes**
Why did the employee trust an unsolicited password-protected file? This makes me think phishing awareness training should specifically cover this tactic, since a "protected" file can feel more legitimate to an unsuspecting user rather than less.

---

## Reflections/Notes

**1. Were there any specific activities that were challenging for you? Why or why not?**
The tcpdump activity was the most challenging for me. Working purely from the command line, without the visual structure Wireshark provides, meant I had to be much more precise with syntax. A few failed attempts taught me to slow down and verify each flag before running a capture.

**2. Has your understanding of incident detection and response changed since taking this course?**
Yes, significantly. Before this course, I saw incident response as a single reactive event. Now I understand it as a structured lifecycle — preparation, detection, containment, and recovery — where the tools and decisions at each phase directly shape how quickly and effectively an organization can recover.

**3. Was there a specific tool or concept that you enjoyed the most? Why?**
I most enjoyed working with VirusTotal. Coming from a legal and compliance background, I found it fascinating how a single indicator, like a file hash, can unlock a whole web of related evidence — IPs, domains, and attacker behavior — that supports both technical response and, potentially, later legal or regulatory reporting.

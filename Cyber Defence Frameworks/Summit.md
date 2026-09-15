# Summit

## Overview

Summit is a practical defensive security room focused on applying the **Pyramid of Pain** in a realistic SOC environment.

The goal is to detect and block malicious activity by creating defensive controls against different Indicators of Compromise (IoCs), starting with simple hashes and progressing toward attacker behavior.

The room demonstrates how defenders can make attacks increasingly difficult by targeting indicators higher in the Pyramid of Pain.

---

## Scenario

In this room, a malicious Windows executable is analyzed and different security controls are implemented to prevent the malware from operating successfully.

The investigation focuses on:

- File hashes
- Malicious IP addresses
- Domains
- Network connections
- File artifacts
- Attacker behavior

---

## Hash-Based Detection

The first defensive layer focuses on identifying malicious files using hashes.

A known malicious file can be added to a blocklist using its hash.

Common hash types include:

- MD5
- SHA-1
- SHA-256

Hash-based detection is useful, but attackers can easily modify a file to generate a new hash.

This represents one of the lower levels of the **Pyramid of Pain**.

---

## Firewall Rules

Firewall rules can be used to block malicious network communication.

Important information when creating a rule includes:

- Source IP
- Destination IP
- Destination port
- Protocol
- Action

For example, suspicious outbound connections to attacker-controlled infrastructure can be blocked to prevent Command and Control (C2) communication.

---

## DNS Filtering

Attackers often use malicious domains to communicate with their infrastructure.

DNS filtering can prevent systems from resolving or connecting to known malicious domains.

Defenders can block:

- Malicious domains
- Suspicious subdomains
- Known malicious IP addresses

This can disrupt malware communication and prevent access to attacker infrastructure.

---

## Network Artifacts

Instead of detecting only IP addresses or domains, defenders can analyze patterns in network communication.

Examples include:

- Remote IP addresses
- Remote ports
- Connection frequency
- Communication patterns

Network artifacts are more difficult for attackers to change than simple file hashes.

---

## File Artifacts

Malware may create or modify files after execution.

Useful indicators include:

- File name
- File path
- File creation activity
- Suspicious directories

Detecting these artifacts allows defenders to identify malicious behavior even if the malware's hash changes.

---

## Sigma Rules

The room introduces **Sigma rules** for creating behavioral detections.

Sigma is a generic detection rule format that can describe suspicious activity across different logging platforms.

Rules can monitor areas such as:

- Process activity
- File activity
- Network connections
- Registry activity

A Sigma rule may use conditions such as:

- File path
- File name
- Remote IP
- Remote port
- Frequency
- Time window

---

## MITRE ATT&CK Mapping

Detection rules can be mapped to **MITRE ATT&CK** techniques and tactics.

For example, suspicious network communication may be associated with:

**Command and Control (C2)**

Mapping detections to ATT&CK helps analysts understand the attacker's behavior rather than focusing only on individual IoCs.

---

## Applying the Pyramid of Pain

The room demonstrates how defensive controls can move higher through the Pyramid of Pain:

**Hashes → IP Addresses → Domains → Network/Host Artifacts → Tools → TTPs**

The higher the detection is in the pyramid, the more difficult it becomes for the attacker to bypass it.

Blocking a hash may force the attacker to modify a file.

Detecting their behavior may force them to change their entire attack technique.

---

## Skills Learned

After completing this room, I learned how to:

- Apply the Pyramid of Pain in a practical scenario
- Block malicious file hashes
- Create firewall rules
- Block malicious domains and IP addresses
- Analyze network and file artifacts
- Create behavioral detection rules
- Work with Sigma rules
- Map detections to MITRE ATT&CK
- Detect Command and Control activity
- Understand how different defensive controls impact attackers

---

## Key Takeaway

Summit demonstrates how defenders can move beyond simple IoC blocking and focus on attacker behavior.

The main objective is to create detections that are increasingly difficult for attackers to evade.

**The higher the detection is on the Pyramid of Pain, the more effort the attacker must make to bypass the defense.**

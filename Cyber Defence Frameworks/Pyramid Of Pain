# Pyramid of Pain

## Overview

The Pyramid of Pain is a cybersecurity model created by David J. Bianco that explains how different types of Indicators of Compromise (IoCs) affect an attacker when defenders detect and block them.

The main idea is simple: the higher an indicator is in the pyramid, the more difficult and costly it is for an attacker to change it.

For example, changing a file hash is very easy for an attacker, while changing their entire Tactics, Techniques, and Procedures (TTPs) can require significant effort.

This room introduces the different levels of the Pyramid of Pain and explains how defenders can use them for threat detection and response.

---

## Pyramid of Pain Levels

The Pyramid of Pain contains six main levels:

1. Hash Values
2. IP Addresses
3. Domain Names
4. Network / Host Artifacts
5. Tools
6. Tactics, Techniques, and Procedures (TTPs)

As we move higher in the pyramid, the amount of "pain" caused to the attacker increases.

---

## 1. Hash Values

Hash values are unique values generated from files using hashing algorithms.

Common hashing algorithms include:

- MD5
- SHA-1
- SHA-256

Security teams can use malicious file hashes as Indicators of Compromise.

For example, if a known malware sample has a specific SHA-256 hash, security tools can detect or block files with that hash.

### Limitation

Hashes are relatively easy for attackers to change.

Even a small modification to a malicious file can generate a completely different hash.

Because of this, blocking hashes causes relatively little pain to attackers.

---

## 2. IP Addresses

Attackers often use IP addresses for activities such as:

- Command and Control (C2)
- Malware downloads
- Data exfiltration
- Remote access

Security teams can block known malicious IP addresses using:

- Firewalls
- IDS/IPS
- SIEM rules
- Threat intelligence feeds

### Limitation

Attackers can change their IP addresses by moving their infrastructure or using:

- VPNs
- Proxies
- Compromised servers
- Cloud infrastructure

Changing an IP address requires more effort than changing a hash, but it is still relatively easy.

---

## 3. Domain Names

Attackers often use domain names instead of directly connecting to IP addresses.

Domains can be used for:

- Phishing websites
- Malware delivery
- Command and Control (C2)
- Credential harvesting
- Redirecting victims

Defenders can block malicious domains using DNS filtering and other security controls.

Attackers may also use techniques such as:

- Domain generation
- Look-alike domains
- Punycode attacks
- Subdomains

Changing domains requires additional infrastructure and therefore causes more pain than changing an IP address or file hash.

---

## 4. Network Artifacts

Network artifacts are characteristics that can be observed in network traffic.

Examples include:

- User-Agent strings
- URI patterns
- HTTP requests
- C2 communication patterns
- Unusual ports
- Network protocol behavior

For example, malware may communicate with its C2 server using a specific User-Agent or URI structure.

Defenders can create detection rules based on these patterns.

Changing network behavior usually requires attackers to modify their malware or infrastructure, which requires additional effort.

---

## 5. Host Artifacts

Host artifacts are indicators left behind on compromised systems.

Examples include:

- Registry keys
- File paths
- File names
- Scheduled tasks
- Services
- Processes
- Persistence mechanisms

These artifacts can help security analysts understand what an attacker did after compromising a system.

EDR and SIEM solutions can monitor these artifacts and generate alerts when suspicious behavior is detected.

Attackers must modify how their malware operates to avoid these detections, making host artifacts more painful to change than simple indicators such as hashes.

---

## 6. Tools

Attackers use various tools during cyber attacks.

Examples may include:

- Remote Access Tools (RATs)
- Credential dumping tools
- Network scanners
- Exploitation frameworks
- Custom malware

If defenders can reliably detect the tools used by attackers, the attackers may need to:

- Modify their tools
- Develop new malware
- Find alternative tools
- Change their attack infrastructure

This requires significantly more time and effort.

---

## 7. Tactics, Techniques, and Procedures (TTPs)

TTPs represent how attackers operate.

### Tactics

The attacker's overall objective.

Examples:

- Initial Access
- Persistence
- Privilege Escalation
- Credential Access
- Discovery
- Collection
- Exfiltration

### Techniques

The methods attackers use to achieve their objectives.

Examples:

- Phishing
- PowerShell
- Credential Dumping
- Scheduled Tasks
- Remote Services

### Procedures

The specific way an attacker implements a technique.

TTPs are at the top of the Pyramid of Pain because they describe the attacker's behavior rather than a simple technical indicator.

Detecting TTPs forces attackers to change how they operate, which can require significant time, resources, and knowledge.

This makes TTP-based detection extremely valuable for defenders.

---

## Fuzzy Hashing

Traditional hashes require files to be identical to produce the same hash.

Fuzzy hashing works differently.

It attempts to determine the similarity between files instead of checking whether they are exactly identical.

This can help analysts identify modified versions of malware.

Fuzzy hashes are also known as:

**Context Triggered Piecewise Hashes (CTPH)**

A commonly used fuzzy hashing tool is:

**ssdeep**

---

## Indicators of Compromise (IoCs)

Indicators of Compromise are pieces of evidence that may indicate malicious activity.

Examples include:

- Malicious hashes
- Suspicious IP addresses
- Malicious domains
- Unusual network traffic
- Suspicious registry modifications
- Malicious processes

IoCs are useful for detecting known threats, but attackers can often modify lower-level indicators.

This is why behavioral detection and TTP-based detection are important.

---

## Defensive Perspective

The goal of the Pyramid of Pain is not simply to collect as many IoCs as possible.

Instead, defenders should try to detect indicators that are increasingly difficult for attackers to change.

Blocking a hash may stop one malware sample.

Blocking an IP may stop one server.

Detecting an attacker's behavior can potentially stop multiple versions of their attack.

Therefore, detection strategies should ideally move higher in the Pyramid of Pain.

---

## Key Concept

The higher you move in the Pyramid of Pain, the more difficult it becomes for an attacker to adapt.

| Indicator | Difficulty for Attacker |
|---|---|
| Hash Values | Trivial |
| IP Addresses | Easy |
| Domain Names | Simple |
| Network / Host Artifacts | Annoying |
| Tools | Challenging |
| TTPs | Tough |

---

## Skills Learned

After completing this room, I learned how to:

- Understand the Pyramid of Pain model
- Identify different types of Indicators of Compromise
- Analyze malicious hashes
- Understand IP and domain-based indicators
- Identify network and host artifacts
- Understand attacker tools
- Recognize Tactics, Techniques, and Procedures
- Understand the difference between IoC-based and behavioral detection
- Use fuzzy hashing to identify similar files
- Understand why TTP-based detection creates more difficulty for attackers

---

## Key Takeaway

The Pyramid of Pain demonstrates that not all indicators are equally valuable.

Lower-level indicators such as hashes and IP addresses are useful but relatively easy for attackers to replace.

Higher-level indicators such as tools and TTPs are much harder to change.

For SOC analysts and defenders, focusing on attacker behavior and TTPs can provide stronger and more resilient detection capabilities.

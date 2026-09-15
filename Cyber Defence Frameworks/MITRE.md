# MITRE

## Overview

MITRE provides cybersecurity frameworks and resources that help defenders understand attacker behavior.

The most well-known framework is **MITRE ATT&CK**, a knowledge base that documents real-world attacker **Tactics, Techniques, and Procedures (TTPs)**.

It is widely used by SOC analysts, threat hunters, penetration testers, and incident responders.

---

## MITRE ATT&CK

ATT&CK stands for:

**Adversarial Tactics, Techniques, and Common Knowledge**

Instead of describing an attack as a simple sequence of stages, ATT&CK focuses on **what attackers do and how they do it**.

---

## Tactics, Techniques, and Procedures (TTPs)

### Tactics

A tactic represents **what the attacker wants to achieve**.

Examples:

- Reconnaissance
- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Credential Access
- Discovery
- Lateral Movement
- Collection
- Command and Control
- Exfiltration
- Impact

### Techniques

Techniques describe **how the attacker achieves a tactic**.

Examples:

- Phishing
- Create Account
- PowerShell
- Remote Services
- Credential Dumping

Each technique has a unique ID, such as:

`T1136 – Create Account`

### Sub-Techniques

Some techniques contain more specific **sub-techniques**.

These provide additional detail about exactly how an attacker performs an action.

---

## MITRE ATT&CK Navigator

ATT&CK Navigator is a tool used to visualize and analyze ATT&CK techniques.

It can be used to:

- Map attacker behavior
- Highlight techniques used by threat groups
- Compare different threats
- Identify detection gaps
- Create ATT&CK layers

For example, analysts can create a Navigator layer showing all techniques associated with a specific APT group.

---

## Threat Groups and Software

MITRE ATT&CK contains information about known threat groups and the software they use.

A group profile can include:

- Techniques used
- Targeted industries
- Associated campaigns
- Malware and tools
- Known procedures

This helps analysts understand how real attackers operate.

---

## Cyber Analytics Repository (CAR)

The **Cyber Analytics Repository (CAR)** contains analytics that defenders can use to detect attacker behavior.

CAR analytics can be mapped to MITRE ATT&CK techniques.

Detection examples may include:

- Suspicious process execution
- Scheduled task activity
- File access
- Authentication behavior

Analytics can include queries for technologies such as:

- Splunk
- EQL

Example:

`CAR-2020-09-001 – Scheduled Task - File Access`

---

## Adversary Emulation

MITRE resources can also help security teams simulate the behavior of real attackers.

An **Adversary Emulation Plan** describes how a threat actor's known behavior can be reproduced in a controlled environment.

This can help organizations:

- Test security controls
- Evaluate detections
- Identify defensive gaps
- Improve incident response

---

## Other MITRE Frameworks

MITRE also provides frameworks for specialized areas.

### ATLAS

**Adversarial Threat Landscape for AI Systems**

ATLAS focuses on attacks against AI and machine learning systems.

### AADAPT

AADAPT focuses on adversarial behavior involving decentralized and blockchain-related technologies.

---

## ATT&CK for SOC Analysts

SOC analysts can use MITRE ATT&CK to understand alerts and map suspicious activity to attacker behavior.

For example:

If an attacker uses PowerShell, the analyst can identify the corresponding ATT&CK technique and investigate what tactic the attacker may be trying to achieve.

This provides more context than simply identifying a malicious command.

---

## Skills Learned

After completing this room, I learned how to:

- Understand the MITRE ATT&CK framework
- Identify Tactics, Techniques, and Procedures (TTPs)
- Find ATT&CK technique IDs
- Understand sub-techniques
- Use ATT&CK Navigator
- Research threat groups and their software
- Understand the Cyber Analytics Repository (CAR)
- Understand adversary emulation
- Explore MITRE projects such as ATLAS and AADAPT

---

## Key Takeaway

MITRE ATT&CK provides a common language for describing attacker behavior.

Instead of focusing only on individual Indicators of Compromise, defenders can focus on **how attackers operate**.

**Tactic = Why**

**Technique = How**

**Procedure = The specific implementation**

This makes MITRE ATT&CK an important framework for threat detection, threat hunting, and SOC operations.

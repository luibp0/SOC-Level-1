# Unified Kill Chain

## Overview

The Unified Kill Chain (UKC) is a cybersecurity framework that combines ideas from multiple attack models to provide a more complete view of how cyber attacks happen.

Unlike the traditional Cyber Kill Chain, the UKC also focuses on what attackers do after gaining access, such as privilege escalation, discovery, lateral movement, collection, and exfiltration.

The framework contains **18 phases**, organized into three main sections:

- In
- Through
- Out

---

## 1. In – Initial Foothold

This section describes how an attacker prepares for an attack and gains initial access to the target.

Common activities include:

- Reconnaissance
- Weaponization
- Delivery
- Social Engineering
- Exploitation
- Persistence
- Command and Control (C2)

### Reconnaissance

Attackers gather information about the target using techniques such as OSINT, scanning, and enumeration.

### Weaponization

The attacker prepares malicious tools, payloads, or infrastructure for the attack.

### Delivery & Social Engineering

Phishing emails, malicious links, attachments, and impersonation may be used to reach and manipulate the victim.

### Exploitation

The attacker exploits a vulnerability or user action to gain access.

### Persistence

Techniques such as registry modifications, scheduled tasks, or malicious accounts can be used to maintain access.

---

## 2. Through – Network Propagation

After gaining access, the attacker attempts to expand their control inside the environment.

Important activities include:

- Discovery
- Privilege Escalation
- Credential Access
- Lateral Movement
- Execution

### Discovery

Attackers gather information about:

- Users
- Computers
- Networks
- Services
- Security controls

### Privilege Escalation

The attacker attempts to gain higher privileges, such as Administrator or SYSTEM access.

### Credential Access

Tools such as **Mimikatz** may be used to obtain passwords, hashes, or other credentials.

### Lateral Movement

The attacker moves from one compromised system to another.

This process is also known as **Network Propagation**.

---

## 3. Out – Actions on Objectives

The final section describes how attackers achieve their objectives after establishing control.

Activities can include:

- Collection
- Exfiltration
- Impact
- Objectives

### Collection

Attackers gather valuable information from compromised systems or information repositories.

### Exfiltration

Collected data is transferred outside the victim's environment.

Attackers may use C2 channels, proxies, or other methods to hide the transfer.

### Impact

Attackers may:

- Delete data
- Encrypt systems
- Disrupt services
- Manipulate information

### Objectives

The attacker achieves their final goal, such as:

- Data theft
- Espionage
- Financial gain
- Intellectual property theft
- Service disruption

---

## Threat Modeling

Threat modeling helps organizations identify potential threats before they become successful attacks.

Common models include:

### STRIDE

Used to identify different categories of threats.

### DREAD

Used to evaluate and prioritize security risks.

### CVSS

The Common Vulnerability Scoring System is used to measure the severity of vulnerabilities.

---

## Unified Kill Chain vs Cyber Kill Chain

The **Cyber Kill Chain** mainly focuses on how an attacker gains access and reaches their objective.

The **Unified Kill Chain** provides a broader view, especially of what happens inside the network after the initial compromise.

This makes it useful for understanding:

- Privilege Escalation
- Discovery
- Credential Access
- Lateral Movement
- Collection
- Exfiltration

---

## Relationship with MITRE ATT&CK

Many Unified Kill Chain activities can be mapped to MITRE ATT&CK tactics.

Examples:

- Reconnaissance → TA0043
- Privilege Escalation → TA0004
- Discovery → TA0007
- Lateral Movement → TA0008
- Collection → TA0009
- Exfiltration → TA0010
- Impact → TA0040

This helps defenders connect attack stages with specific attacker techniques.

---

## Skills Learned

After completing this room, I learned how to:

- Understand the Unified Kill Chain
- Identify the In, Through, and Out stages
- Understand network propagation
- Recognize privilege escalation and lateral movement
- Understand collection and exfiltration
- Apply basic threat modeling concepts
- Connect the UKC with MITRE ATT&CK
- Analyze an attack from initial access to final objectives

---

## Key Takeaway

The Unified Kill Chain provides a detailed view of the complete attacker lifecycle.

**In → Through → Out**

It helps SOC analysts understand not only how attackers gain access, but also how they move through a network and eventually achieve their objectives.

# Eviction

## Overview

Eviction is a practical cyber defence room focused on analyzing the behavior of an **Advanced Persistent Threat (APT)** using the **MITRE ATT&CK framework**.

The room uses an ATT&CK Navigator layer to investigate the techniques used by the threat group **Y-28** and understand how the attacker progresses through different stages of an attack.

The objective is to identify attacker Tactics, Techniques, and Procedures (TTPs) and understand how defenders can detect and respond to them.

---

## MITRE ATT&CK Navigator

The investigation uses **MITRE ATT&CK Navigator** to visualize the techniques associated with the threat actor.

Navigator helps analysts:

- Identify attacker techniques
- Map techniques to ATT&CK tactics
- Analyze attack progression
- Understand attacker behavior
- Build a complete picture of an intrusion

---

## Reconnaissance and Initial Access

Before compromising the organization, the attacker gathers information about the target.

The attacker then attempts to gain initial access using techniques such as:

- Phishing
- Spearphishing
- Malicious links
- Social engineering

### Spearphishing Link

A targeted phishing message can contain a malicious link designed to trick a victim into visiting attacker-controlled infrastructure.

This can provide the attacker with their initial foothold.

---

## Resource Development

Attackers may prepare resources before performing the attack.

This can include:

- Creating accounts
- Preparing infrastructure
- Registering domains
- Developing malicious payloads

These resources support later stages of the attack.

---

## Execution

After gaining access, attackers need to execute commands or malicious code.

Common techniques include:

- PowerShell
- Command Shell
- Scripts
- User Execution

### User Execution

Attackers may rely on the victim to perform an action such as:

- Opening a malicious file
- Clicking a malicious link
- Executing a payload

---

## Persistence

Persistence allows attackers to maintain access to compromised systems.

One technique is modifying Windows Registry keys such as:

- Run
- RunOnce

Programs stored in these locations can automatically execute when the user logs in.

---

## Defense Evasion

Attackers use defense evasion techniques to avoid detection by security tools.

One method is abusing legitimate system binaries to execute malicious code.

This is sometimes known as:

**System Binary Proxy Execution**

Because legitimate Windows programs are being used, malicious activity may be more difficult to identify.

---

## Credential Access

Attackers may attempt to obtain credentials from compromised systems.

Tools such as **Mimikatz** can be used to extract:

- Passwords
- Password hashes
- Authentication credentials

Stolen credentials can help attackers escalate privileges or move to additional systems.

---

## Discovery

After compromising a system, attackers gather information about the environment.

They may investigate:

- Network configuration
- Users
- Systems
- Services
- Active connections

Network utilities such as `tcpdump` can also be abused to capture and analyze network traffic.

---

## Lateral Movement

Lateral Movement occurs when an attacker moves from one compromised system to another.

Attackers may use:

- Remote Services
- Stolen credentials
- Administrative protocols
- Remote access tools

This allows the attacker to expand their access throughout the organization.

---

## Collection

Once valuable systems are discovered, attackers begin collecting information.

Possible targets include:

- File servers
- Databases
- Email systems
- Information repositories
- Intellectual property

For organizations holding valuable research or proprietary information, these repositories can be a major target.

---

## Command and Control

Attackers establish Command and Control (C2) communication to remotely control compromised systems.

C2 can be used to:

- Send commands
- Download additional tools
- Control malware
- Prepare data for exfiltration

Attackers may also use proxy techniques to hide their communication.

---

## Exfiltration

Exfiltration is the process of transferring stolen information outside the victim's environment.

Attackers may use proxies and C2 infrastructure to hide the true destination of the stolen data.

This makes malicious network traffic more difficult to detect.

---

## Using ATT&CK for Investigation

MITRE ATT&CK allows SOC analysts to connect individual events to a larger attack.

Instead of seeing phishing, PowerShell execution, credential theft, and lateral movement as unrelated alerts, ATT&CK helps connect them as parts of the same intrusion.

This provides analysts with better context about the attacker's objectives.

---

## Skills Learned

After completing this room, I learned how to:

- Use MITRE ATT&CK Navigator
- Investigate an APT's behavior
- Identify attacker TTPs
- Analyze spearphishing and initial access
- Understand User Execution
- Identify persistence using Registry keys
- Understand System Binary Proxy Execution
- Analyze credential access techniques
- Identify discovery activity
- Understand lateral movement
- Analyze collection and exfiltration
- Map an attack using MITRE ATT&CK

---

## Key Takeaway

Eviction demonstrates how **MITRE ATT&CK can be used to investigate a real attack scenario from initial access to data exfiltration**.

By mapping attacker behavior to ATT&CK techniques, SOC analysts can better understand what has happened, what the attacker may do next, and where defensive controls should be applied.

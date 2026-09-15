# Cyber Kill Chain

## Overview

The Cyber Kill Chain is a cybersecurity framework developed by Lockheed Martin to describe the different stages of a cyber attack.

The framework helps security teams understand how attackers move from initial reconnaissance to achieving their final objective.

By identifying which stage an attacker is currently in, defenders can detect, disrupt, or stop the attack before the attacker reaches their goal.

The Cyber Kill Chain consists of seven main phases:

1. Reconnaissance
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command and Control (C2)
7. Actions on Objectives

---

## Why the Cyber Kill Chain is Important

Cyber attacks usually involve multiple steps rather than a single action.

The Cyber Kill Chain allows defenders to break an attack into stages and understand:

- What the attacker is trying to achieve
- What techniques are being used
- Where the attack can be detected
- Where security controls can stop the attack
- How the attacker progresses through the environment

Stopping the attacker at any stage can prevent them from completing the attack.

---

## 1. Reconnaissance

Reconnaissance is the information-gathering stage.

Before launching an attack, attackers collect information about their target.

This information can help them identify potential vulnerabilities and attack vectors.

Attackers may collect information such as:

- Employee names
- Email addresses
- Company information
- Technologies used by the organization
- Public IP addresses
- Domains and subdomains
- Social media accounts
- Exposed services

### Passive Reconnaissance

The attacker gathers information without directly interacting with the target.

Examples:

- Search engines
- Social media
- Public websites
- WHOIS information
- Job advertisements
- OSINT tools

### Active Reconnaissance

The attacker directly interacts with the target's infrastructure.

Examples:

- Port scanning
- Network scanning
- Service enumeration
- Vulnerability scanning

### Defender's Goal

Reduce publicly available sensitive information and detect suspicious reconnaissance activity.

---

## 2. Weaponization

During Weaponization, the attacker prepares the tools or malicious payload required for the attack.

The attacker may combine an exploit with malware to create a weaponized payload.

Examples include:

- Malicious Microsoft Office documents
- Malicious macros
- Exploit payloads
- Trojanized files
- Malicious scripts
- Custom malware

For example, an attacker could create a Word document containing a malicious macro.

When the victim opens the document and enables the macro, malicious code may execute.

### Zero-Day Exploits

Attackers may also use vulnerabilities that are unknown to the software vendor or do not yet have a patch.

These are commonly called **zero-day vulnerabilities**.

---

## 3. Delivery

Delivery is the stage where the attacker sends the malicious payload to the victim.

Common delivery methods include:

- Phishing emails
- Spearphishing attachments
- Spearphishing links
- Malicious websites
- USB devices
- Social engineering
- Drive-by downloads

### Example

An attacker creates a malicious Word document during Weaponization.

They then send that document to an employee through a phishing email.

Sending the document is the **Delivery** stage.

### Defender's Goal

Security controls such as email filtering, web filtering, and security awareness training can help stop malicious payloads before they reach users.

---

## 4. Exploitation

Exploitation occurs when the attacker takes advantage of a vulnerability to execute malicious code or gain access.

The vulnerability could exist in:

- Software
- Operating systems
- Web applications
- Browsers
- Plugins
- Human behavior

Examples include:

- Exploiting a public-facing application
- Exploiting an unpatched vulnerability
- Executing malicious macros
- Exploiting browser vulnerabilities
- Using malicious scripts

Successful exploitation allows the attacker to move further into the target environment.

---

## 5. Installation

After successful exploitation, the attacker may install malware or establish persistence on the compromised system.

The goal is to maintain access even after the initial compromise.

Examples include:

- Installing a Remote Access Trojan (RAT)
- Creating malicious services
- Creating scheduled tasks
- Modifying registry keys
- Installing backdoors
- DLL hijacking
- Dynamic linker hijacking
- Adding startup programs

### Persistence

Persistence allows an attacker to regain access after:

- System restarts
- User logouts
- Network interruptions

This makes persistence an important part of many cyber attacks.

---

## 6. Command and Control (C2)

Once the attacker has compromised a system, the infected machine may establish communication with attacker-controlled infrastructure.

This communication is known as:

**Command and Control (C2)**

The attacker can use the C2 channel to remotely control the compromised machine.

C2 communication may use protocols such as:

- HTTP
- HTTPS
- DNS
- TCP
- Other network protocols

Through the C2 channel, attackers may:

- Execute commands
- Download additional malware
- Upload tools
- Control compromised machines
- Move further through the network
- Prepare data for exfiltration

### Defender's Goal

Security teams can monitor unusual outbound network connections, suspicious domains, malicious IP addresses, and abnormal traffic patterns to detect C2 activity.

---

## 7. Actions on Objectives

This is the final stage of the Cyber Kill Chain.

At this point, the attacker attempts to accomplish their primary objective.

The objective depends on the attack.

Examples include:

- Stealing sensitive information
- Data exfiltration
- Credential theft
- Intellectual property theft
- Destroying data
- Encrypting files with ransomware
- Disrupting services
- Financial theft
- Espionage

### Data Collection

Before exfiltration, attackers may collect information from compromised systems.

For example:

**Data from Local System**

An attacker may search the compromised computer for sensitive files and information.

### Exfiltration

The collected information can then be transferred outside the victim's network to attacker-controlled infrastructure.

---

## Example Attack Scenario

A simplified attack using the Cyber Kill Chain could look like this:

### Reconnaissance

The attacker searches LinkedIn and the company's website to identify employees and email addresses.

### Weaponization

The attacker creates a malicious Word document containing malware.

### Delivery

The document is sent to an employee using a spearphishing email.

### Exploitation

The victim opens the document, allowing malicious code to execute.

### Installation

Malware establishes persistence on the victim's computer.

### Command and Control

The compromised computer connects to an attacker-controlled C2 server.

### Actions on Objectives

The attacker collects sensitive company files and exfiltrates them.

---

## Important Concepts

### Spearphishing Attachment

A targeted phishing email containing a malicious attachment.

The attacker usually attempts to convince a specific victim to open the attachment.

This is commonly associated with the **Delivery** stage.

---

### Exploit Public-Facing Application

Attackers may exploit vulnerabilities in internet-facing applications to gain initial access.

Examples include:

- Web servers
- VPN gateways
- Email servers
- Public web applications

This involves exploiting a vulnerability exposed to the internet.

---

### PowerShell

PowerShell is a legitimate Windows command-line and scripting environment.

Attackers can abuse PowerShell to:

- Execute commands
- Download payloads
- Run scripts
- Perform reconnaissance
- Execute malware

Because PowerShell is a legitimate administrative tool, attackers may abuse it as a **Living off the Land** technique.

---

### Dynamic Linker Hijacking

Dynamic linker hijacking is a technique where attackers manipulate how an application loads shared libraries.

The attacker attempts to make a legitimate application load a malicious library instead of the expected legitimate one.

This can be used for:

- Code execution
- Persistence
- Privilege escalation
- Defense evasion

---

### Shadow Copies

Windows can create copies of files or system data known as **Volume Shadow Copies**.

These copies can be useful for:

- Backups
- File recovery
- System restoration

Attackers, especially ransomware operators, may delete shadow copies to prevent victims from recovering their files.

---

### Zero-Day

A zero-day vulnerability is a vulnerability that is unknown to the vendor or does not yet have an available fix when attackers begin exploiting it.

Zero-day vulnerabilities can be especially dangerous because organizations may have limited defenses against them.

---

## Cyber Kill Chain and Defenders

The Cyber Kill Chain is useful because defenders do not necessarily need to wait until the attacker reaches the final stage.

Security controls can interrupt the attack throughout the chain.

| Stage | Possible Defensive Action |
|---|---|
| Reconnaissance | Monitor scanning and reduce exposed information |
| Weaponization | Threat intelligence and malware research |
| Delivery | Email and web filtering |
| Exploitation | Patch management and endpoint protection |
| Installation | EDR, antivirus, and persistence detection |
| Command & Control | Network monitoring and C2 blocking |
| Actions on Objectives | DLP, incident response, and access controls |

---

## Breaking the Kill Chain

The main defensive idea behind the Cyber Kill Chain is to interrupt the attack as early as possible.

For example:

If a phishing email is blocked during **Delivery**, the attacker cannot reach Exploitation.

If malware is detected during **Installation**, the attacker may not establish C2 communication.

If C2 traffic is blocked, the attacker may lose remote control of the compromised system.

Therefore, defenders can stop the attack by breaking any link in the chain.

---

## Limitations of the Cyber Kill Chain

Although the Cyber Kill Chain is useful, it has some limitations.

It was primarily designed around traditional external attacks and may not fully represent every modern attack.

For example, modern attackers may:

- Skip certain stages
- Perform stages in a different order
- Repeat stages multiple times
- Use legitimate tools
- Already have access through compromised credentials
- Move laterally between systems

Frameworks such as **MITRE ATT&CK** provide a more detailed view of attacker behavior and techniques.

---

## Skills Learned

After completing this room, I learned how to:

- Understand the seven stages of the Cyber Kill Chain
- Identify reconnaissance activities
- Understand how attackers weaponize malicious payloads
- Recognize different malware delivery techniques
- Understand exploitation and vulnerability abuse
- Identify installation and persistence techniques
- Understand Command and Control (C2)
- Recognize attacker objectives and data exfiltration
- Map attacker activities to different Kill Chain stages
- Understand how defenders can interrupt an attack
- Analyze cyber attacks from a defensive perspective

---

## Key Takeaway

The Cyber Kill Chain provides a structured way to understand how a cyber attack progresses from initial reconnaissance to the attacker's final objective.

The seven stages are:

**Reconnaissance → Weaponization → Delivery → Exploitation → Installation → Command & Control → Actions on Objectives**

For defenders and SOC analysts, the goal is to detect and disrupt the attacker as early as possible.

Breaking any stage of the chain can prevent the attacker from successfully reaching their objective.

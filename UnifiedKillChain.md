# TryHackMe - Unified Kill Chain Room

This repository is part of my TryHackMe journey to becoming a cybersecurity expert. Below is a brief overview of the **Unified Kill Chain** room I completed.

---

## 🧠 Room Summary

The **Unified Kill Chain (UKC)** is a comprehensive cybersecurity framework that outlines the full lifecycle of a cyberattack. It aims to improve understanding and defense by categorizing the tactics and techniques used by adversaries throughout all stages of an attack.

### 📌 Learning Objectives:
- Understand the purpose and importance of kill chain frameworks.
- Analyze attacker behavior, methodology, and objectives.
- Explore all 18 phases of the Unified Kill Chain.
- See how the UKC complements other frameworks like MITRE ATT&CK and Lockheed Martin's Cyber Kill Chain.

---

## 🛠️ Key Concepts Covered

### 🔗 What is a Kill Chain?
- Origin: **The Military**
- Describes various phases of an attack such as reconnaissance, exploitation, and privilege escalation.

### ⚙️ Threat Modelling
- Involves identifying assets, assessing vulnerabilities, and creating mitigation plans.
- Utilizes models like **STRIDE**, **DREAD**, and **CVSS**.

### 🔍 Unified Kill Chain (2017)
- Contains **18 detailed attack phases** across 3 major categories:
  1. **In (Initial Foothold)**
     - Reconnaissance, Weaponization, Social Engineering, Exploitation, Persistence, Defense Evasion, Command & Control, Pivoting.
  2. **Through (Network Propagation)**
     - Discovery, Privilege Escalation, Execution, Credential Access, Lateral Movement.
  3. **Out (Actions on Objectives)**
     - Collection, Exfiltration, Impact, Objectives.

---

## 📋 Practical Scenarios

Matched attack actions to UKC phases:
1. **Information gathering** → Reconnaissance  
2. **Remote access setup** → Persistence  
3. **Controlling victim's machine** → Command & Control  
4. **Network lateral movement** → Lateral Movement  
5. **Data theft and sale** → Objectives  

**✅ Flag:** `THM{UKC_SCENARIO}`

---

## 🧩 Additional Resources

- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [Lockheed Martin Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)
- [STRIDE Threat Model](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats)

---

## 🏁 Conclusion

The Unified Kill Chain is a powerful and modern framework for understanding the full spectrum of cyberattacks. It enables more effective detection, response, and mitigation strategies by mapping out the attack lifecycle in detail.

Stay tuned as I explore more rooms and continue my path in cybersecurity!

---

### 📅 Room Completed: July 2025  
### 🚩 Platform: [TryHackMe](https://tryhackme.com/room/unifiedkillchain)

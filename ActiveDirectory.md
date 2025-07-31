# TryHackMe - Active Directory Basics Room

This repository is part of my TryHackMe journey to becoming a cybersecurity expert. Below is a structured overview of the **Active Directory Basics** room I completed.

---

## 🧠 Room Summary

**Active Directory (AD)** is a core component of Windows network environments that enables centralized domain management, including user authentication, resource access, and group policies. Understanding AD is essential for both defensive and offensive security practices.

### 📌 Learning Objectives:
- Understand the basic architecture and function of Active Directory.
- Learn key concepts like domains, forests, OUs, and Group Policy.
- Explore how authentication and permissions are handled within AD.
- Practice enumeration techniques and understand attack surfaces in AD environments.

---

## 🛠️ Key Concepts Covered

### 🏛️ What is Active Directory?
- A directory service developed by Microsoft for Windows domain networks.
- Provides centralized control over users, computers, permissions, and other resources.

### 🧱 AD Structure Components:
- **Domain**: A logical group of network objects.
- **Tree**: A collection of domains in a contiguous namespace.
- **Forest**: A collection of trees with a shared global catalog and trust relationships.
- **Organizational Unit (OU)**: Used to group users and computers for easier management.
- **Group Policy Objects (GPO)**: Policies applied to users/computers within domains or OUs.

### 🔐 Authentication in AD:
- Uses **Kerberos** as the primary authentication protocol.
- Relies on **LDAP** (Lightweight Directory Access Protocol) for directory queries.
- **NTLM** is still used in legacy support or fallback scenarios.

---

## 🔍 Practical Enumeration Techniques

### 🧰 Tools Covered:
- **PowerView**: A PowerShell tool used for AD enumeration.
- **BloodHound**: A tool to analyze AD relationships and attack paths.
- **ldapsearch**: A Linux tool for LDAP enumeration.

### ⚙️ Key Enumeration Targets:
- User & group listings
- Computer objects
- ACLs and permission structures
- Trust relationships between domains

---

## 🚨 Security Implications & Common Attacks

- **Password Spraying & Brute Force**: Exploiting weak credentials.
- **Privilege Escalation**: Abusing misconfigured ACLs or unconstrained delegation.
- **Kerberoasting**: Extracting service tickets to crack hashes offline.
- **Lateral Movement**: Using credentials or sessions to pivot inside the network.

---

## 🧪 Hands-on Activities

The room includes simulated labs for:
- Basic enumeration of AD environment.
- Using PowerView and built-in tools to extract AD data.
- Identifying potential attack vectors.

---

## 📋 Key Takeaways

- Active Directory is foundational for managing enterprise Windows environments.
- Enumeration is critical for both attackers and defenders to understand the AD structure.
- Common misconfigurations can lead to severe privilege escalation paths.
- Understanding AD security is crucial for real-world pentesting and red teaming.

---

## 🧩 Additional Resources

- [Microsoft AD Docs](https://docs.microsoft.com/en-us/windows-server/identity/active-directory-domain-services)
- [TryHackMe - Windows Fundamentals](https://tryhackme.com/room/windowsfundamentals1)
- [BloodHound GitHub](https://github.com/BloodHoundAD/BloodHound)
- [ADSecurity.org](https://adsecurity.org/)

---

## 🏁 Conclusion

This room provided foundational knowledge of Active Directory and its role in enterprise environments. It also introduced enumeration techniques and how misconfigurations can be exploited. Understanding these basics is essential before progressing into more advanced AD attack labs.

---

### 📅 Room Completed: July 2025  
### 🚩 Platform: [TryHackMe - Active Directory Basics](https://tryhackme.com/room/activedirectorybasics)

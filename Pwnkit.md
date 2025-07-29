
# 🚨 CVE-2021-4034 — PwnKit Exploitation Lab

> A TryHackMe-based hands-on walkthrough of the **PwnKit** vulnerability (CVE-2021-4034), a critical Local Privilege Escalation flaw affecting Polkit on nearly all major Linux distributions.

## 🧠 Overview

**CVE-2021-4034**, dubbed **PwnKit**, is a high-impact Local Privilege Escalation (LPE) vulnerability discovered by Qualys in January 2022. The flaw exists in the `pkexec` binary of the Polkit package, which is installed by default on most Linux distributions.

This repository documents my learning and exploitation process as part of the **[TryHackMe PwnKit room](https://tryhackme.com/room/pwnkit)**.

---

## 📌 Key Concepts

- **Vulnerability Type**: Local Privilege Escalation (LPE)
- **Affected Component**: `pkexec` (in `polkit`)
- **CVE**: [CVE-2021-4034](https://nvd.nist.gov/vuln/detail/CVE-2021-4034)
- **Impact**: Any unprivileged local user can gain **root access**
- **Exploitability**: Trivially easy, no authentication required

---

## ⚙️ Exploitation Summary

1. Connected to the vulnerable VM provided by TryHackMe
2. Navigated to the preloaded `pwnkit/` directory
3. Compiled the C-based PoC exploit:
   ```bash
   gcc cve-2021-4034-poc.c -o exploit
   ```
4. Executed the exploit:
   ```bash
   ./exploit
   ```
5. Gained a root shell and read the flag:
   ```bash
   cat /root/flag.txt
   # THM{CONGRATULATIONS-YOU-EXPLOITED-PWNKIT}
   ```

---

## 🔧 Remediation

### ✅ Patch (Recommended)
Update the `polkit` package to a secure version:
```bash
sudo apt update && sudo apt upgrade
```

### 🛠️ Temporary Mitigation
Remove the setuid bit from `pkexec`:
```bash
sudo chmod 0755 $(which pkexec)
```

---

## 🔍 Detection & Verification

To check if the system is still vulnerable, run the PoC:
- If you see a help message instead of a root shell, the system is **patched**:
  ```bash
  pkexec --version
  ```

---

## 📚 References

- [Qualys Security Advisory](https://blog.qualys.com/vulnerabilities-research/2022/01/25/cve-2021-4034-pkexec-local-privilege-escalation)
- [Official CVE Page](https://nvd.nist.gov/vuln/detail/CVE-2021-4034)
- [TryHackMe - PwnKit Room](https://tryhackme.com/room/pwnkit)
- [Exploit Repo (arthepsy)](https://github.com/Arthepsy/CVE-2021-4034)

---

## ✍️ Author

**Harry**  
_Aspiring Security Researcher | Penetration Tester | Cybersecurity Enthusiast_

---

## 🚀 Next Steps

- [ ] TryHackMe CVE-2021-3560 Room (Polkit Timing Attack)
- [ ] Create and test a custom PwnKit exploit
- [ ] Explore other Linux LPE techniques

---

> 💡 _This project is for educational purposes only. Never test vulnerabilities on systems you do not own or have explicit permission to test._

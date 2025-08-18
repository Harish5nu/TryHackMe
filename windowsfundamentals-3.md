# 🖥️ Windows Fundamentals 3 - TryHackMe Notes

**Room link:** [Windows Fundamentals 3](https://tryhackme.com/room/windowsfundamentals3xzx)  

---

## 🔹 Topics Covered  
1. Windows Updates  
2. Windows Security  
3. BitLocker  
4. Volume Shadow Copy Service (VSS)  

---

## 1️⃣ Windows Updates  
- Service provided by Microsoft for:  
  - Security updates  
  - Feature enhancements  
  - Bug patches for Windows OS & Microsoft products (e.g., Defender)  
- Windows 10+ → Updates can’t be ignored completely, only postponed. Eventually, the system will update and reboot.  
- Purpose: Keep systems safe & secure.  

---

## 2️⃣ Windows Security  
“Your home to manage the tools that protect your device and data.”  

### Status Icons  
- **Green** → Device sufficiently protected.  
- **Yellow** → Safety recommendation to review.  
- **Red** → Immediate action required.  

### Virus & Threat Protection  
- Scan options: Quick, Full, Custom.  
- Threat history: Last scan, quarantined threats, allowed threats.  

**Settings available:**  
- Real-time protection → Stops malware from running.  
- Cloud-delivered protection → Faster detection using cloud.  
- Automatic sample submission → Sends samples to Microsoft.  
- Controlled folder access → Protects folders from ransomware.  
- Exclusions → Files/folders excluded from scans.  
- Notifications → Alerts for system health/security.  

### Firewall & Network Protection  
Firewall controls access to/from the network.  

Profiles:  
- **Domain** → For domain-authenticated networks.  
- **Private** → For home/private networks.  
- **Public** → For untrusted/public Wi-Fi (coffee shops, airports).  

Command to open firewall: **WF.msc**  

### App & Browser Control  
- SmartScreen → Protects against phishing, malware, and malicious downloads.  
- Exploit protection → Built into Windows.  

### Device Security  
- **Core Isolation** → Virtualization-based protection of core processes.  
- **Memory Integrity** → Prevents malicious code injections.  
- **Security Processor Details** → Information about TPM (Trusted Platform Module).  

TPM: Secure crypto-processor chip for encryption, tamper resistance, and hardware security.  

---

## 3️⃣ BitLocker  
- Drive encryption feature integrated into Windows OS.  
- Protects data from theft, loss, or unauthorized access.  
- Works with TPM (if available) → Ensures data integrity when system is offline.  
- If no TPM v1.2+ available → Requires **USB startup key**.  

---

## 4️⃣ Volume Shadow Copy Service (VSS)  
- Coordinates creation of consistent shadow copies for backup.  
- If enabled, allows:  
  - Create restore point.  
  - Perform system restore.  
  - Configure restore settings.  
  - Delete restore points.  

---

## 📝 Room Answers  

**Task 2**  
- Date definition updates installed → **5/3/2021**  

**Task 3**  
- Area needing immediate attention → **Virus & threat protection**  

**Task 4**  
- Feature turned off → **Real-time protection**  

**Task 5**  
- Firewall profile active on airport Wi-Fi → **Public network**  

**Task 7**  
- TPM stands for → **Trusted Platform Module**  

**Task 8**  
- What to insert if no TPM 1.2+ → **USB startup key**  

**Task 9**  
- VSS → **Volume Shadow Copy Service**  

# 🖥️ Windows Fundamentals 1 - TryHackMe Notes

**Room link:** [Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1)  

---

## 🔹 Topics Covered  
1. Windows Editions  
2. The File System  
3. Windows & System32 Folders  
4. Users  
5. UAC (User Account Control)  
6. Control Panel  
7. Task Manager  

---

## 1️⃣ Windows Editions  
- Different versions of Windows include:  
  - Windows XP, Vista, 7, 10, 11.  
- **Windows 11 Pro** includes **BitLocker encryption**, which **Windows 11 Home** does not support.  

---

## 2️⃣ The File System  
- **Modern Windows systems use NTFS (New Technology File System).**  
- Earlier file systems: **FAT16 / FAT32**, **HPFS**.  
- **FAT** is still common on USB drives, MicroSD cards, etc.  

### ✅ Features of NTFS  
- Supports **files > 4GB**.  
- Set **file & folder permissions**.  
- **Compression** of files/folders.  
- **EFS (Encrypting File System)** for encryption.  
- **ADS (Alternate Data Streams)** → allows files to hold multiple streams of data.  

---

## 3️⃣ Windows / System32 Folders  
- **C:\Windows** → Main Windows system folder.  
- Can exist on another drive, not just C:\.  
- **%windir%** → System environment variable pointing to Windows directory.  
- **System32 folder** → Contains critical system files needed for Windows to function.  

---

## 4️⃣ Users  
- Two types of accounts:  
  - **Administrator** → Full control, can install programs, manage users, and change system settings.  
  - **Standard User** → Limited permissions, can only change their own files.  
- Tool: `lusrmgr.msc` → Opens **Local Users & Groups Management**.  

---

## 5️⃣ UAC (User Account Control)  
- Introduced to reduce risk from malware.  
- By default, admin accounts don’t run with **full elevated privileges**.  
- When elevated actions are needed → UAC prompts the user to **allow or deny**.  
- Protects system from malware running with admin privileges.  

---

## 6️⃣ Control Panel  
- **Settings App** introduced in Windows 8 (touch-focused).  
- **Control Panel** still used for advanced configurations.  
- Some options may redirect between **Settings ↔ Control Panel**.  

---

## 7️⃣ Task Manager  
- Provides details about:  
  - Running apps & processes.  
  - **Performance**: CPU, RAM, disk, network usage.  
  - Startup programs & services.  
- Shortcut: **Ctrl + Shift + Esc**.  

---

## 📝 Room Answers  

**Task 2**  
- Encryption available on Pro but not Home → **BitLocker**  

**Task 3**  
- Hide/disable Search box → **Hidden**  
- Hide/disable Task View button → **Show task view button**  
- Icon besides Clock & Network in Notification Area → **Action Center**  

**Task 4**  
- Meaning of NTFS → **New Technology File System**  

**Task 5**  
- System variable for Windows folder → **%windir%**  

**Task 6**  
- Other user account → **tryhackmebilly**  
- Groups this user is in → **Remote Desktop Users, Users**  
- Built-in guest account → **Guest**  
- Account description → **window$Fun1!**  

**Task 7**  
- UAC stands for → **User Account Control**  

**Task 8**  
- Last setting in Control Panel (small icons view) → **Windows Defender Firewall**  

**Task 9**  
- Keyboard shortcut for Task Manager → **Ctrl + Shift + Esc**  

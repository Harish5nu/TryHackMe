# 🖥️ Windows Fundamentals 2 - TryHackMe Notes

**Room link:** [Windows Fundamentals 2](https://tryhackme.com/room/windowsfundamentals2x0x)  

---

## 🔹 Topics Covered  
1. System Configuration  
2. Change UAC Settings  
3. Computer Management  
4. System Information  
5. Resource Monitor  
6. Command Prompt  
7. Registry Editor  

---

## Task 1: Introduction  
- Launch the attached VM.  
- **Answer:** No answer needed.  

---

## Task 2: System Configuration  
System Configuration (`msconfig`) is used for advanced troubleshooting and diagnosing startup issues.  

- **2.1** Service with Systems Internals as manufacturer → **PsShutdown**  
- **2.2** Windows license registered to → **Windows User**  
- **2.3** Command for Windows Troubleshooting →  
  `C:\Windows\System32\control.exe /name Microsoft.Troubleshooting`  
- **2.4** Command to open Control Panel (exe only) → **control.exe**  

---

## Task 3: Change UAC Settings  
- **3.1** Command to open User Account Control Settings → **UserAccountControlSettings.exe**  

---

## Task 4: Computer Management  
Computer Management provides a centralized view of system settings and performance information.  

- **4.1** Command to open Computer Management → **compmgmt.msc**  
- **4.2** Time GoogleUpdateTaskMachineUA task is configured to run → **6:15 AM**  
- **4.3** Name of the hidden shared folder → **sh4r3dF0ld3r**  

---

## Task 5: System Information  
- **5.1** Command to open System Information → **msinfo32.exe**  
- **5.2** System Name → **THM-WINFUN2**  
- **5.3** Environment variable value for ComSpec → **%SystemRoot%\system32\cmd.exe**  

---

## Task 6: Resource Monitor  
- **6.1** Command to open Resource Monitor → **resmon.exe**  

---

## Task 7: Command Prompt  
- **7.1** Full command for Internet Protocol Configuration →  
  `C:\Windows\System32\cmd.exe /k %windir%\system32\ipconfig.exe`  
- **7.2** Command to show detailed ipconfig info → **ipconfig /all**  

---

## Task 8: Registry Editor  
- **8.1** Command to open Registry Editor → **regedt32.exe**  

---

## Task 9: Conclusion  
- End of room.  

# 🖥️ TryHackMe: Windows Command Line (Cyber Security 101)

This note covers the key tasks and answers for the **Windows Command Line** room from the **Cyber Security 101 Pathway**.

---

## 🔹 Task 1: Basics
**Q:** What is the default command line interpreter in Windows?  
**A:** `cmd.exe`

---

## 🔹 Task 2: System Information
- **OS Version**
  ```cmd
  systeminfo
  ver
  ```
  **Answer:** `10.0.20348`  

- **Hostname**
  ```cmd
  hostname
  ```
  **Answer:** `WINSRV2022-CORE`  

---

## 🔹 Task 3: Networking
- **Find MAC Address**
  ```cmd
  ipconfig /all
  ```
  **Answer:** `ipconfig /all`  

- **Process on Port 3389**
  ```powershell
  Get-Service | Where-Object {$_.DisplayName -like "*Remote Desktop Services*"}
  ```
  **Answer:** `TermService`  

- **Gateway IP**
  ```cmd
  ipconfig /all
  ```
  **Answer:** `10.10.0.1`

---

## 🔹 Task 4: File Search
- **Contents of C:\Treasure\Hunt**
  ```cmd
  type C:\Treasure\Hunt\flag.txt
  ```
  **Answer:** `THM{CLI_POWER}`  

---

## 🔹 Task 5: Processes
- **Find Notepad processes**
  ```cmd
  tasklist /FI "imagename eq Notepad.exe"
  ```
  **Answer:** `tasklist /FI imagename eq Notepad.exe`  

- **Kill process with PID 1516**
  ```cmd
  taskkill /PID 1516
  ```
  **Answer:** `taskkill /PID 1516`

---

## 🔹 Task 6: Shutdown Commands
- **Restart System**
  ```cmd
  shutdown /r
  ```
- **Abort Shutdown**
  ```cmd
  shutdown /a
  ```

---

## 📌 Summary
- Windows **default CLI**: `cmd.exe` (though Windows Terminal is now the modern default shell host).  
- Useful commands covered: `systeminfo`, `hostname`, `ipconfig`, `tasklist`, `taskkill`, `shutdown`.  
- Flag found: **THM{CLI_POWER}**

---

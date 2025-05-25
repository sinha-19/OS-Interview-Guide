# 8. Security, Protection & Access Control

---

## Security vs. Protection

- **Security:** Defending against external threats (unauthorized access, malware, attacks).
- **Protection:** Internal mechanisms to control access by processes/users to resources within the system.

---

## Security Goals

- **Confidentiality:** Prevent unauthorized data access.
- **Integrity:** Prevent unauthorized modification of data.
- **Availability:** Ensure services/data are accessible to authorized users.

---

## Authentication

- Verifying identity of users/processes.
- **Methods:** Passwords, biometrics, tokens, multi-factor authentication.

---

## Authorization

- Determining what an authenticated user/process is allowed to do.
- **Access Control Matrix:** Table specifying access rights of subjects (users/processes) over objects (files, devices).
- **Access Control List (ACL):** Per-object list of allowed (user, rights) pairs.
- **Role-Based Access Control (RBAC):** Rights assigned according to roles.

---

## Protection Mechanisms

- **User Accounts/Groups:** Segregate rights.
- **File Permissions:** Read, write, execute (UNIX: rwxr-xr--).
- **Capabilities:** Tokens or keys that grant access.
- **Protection Rings:** Hardware-enforced privilege levels (e.g., kernel/user mode).

---

## Common Attacks & Threats

| Attack Type           | Description                                      |
|-----------------------|--------------------------------------------------|
| Malware               | Viruses, worms, trojans                          |
| Phishing/Social Eng.  | Tricking users for credentials                   |
| Buffer Overflow       | Overwriting memory to execute arbitrary code     |
| Denial-of-Service     | Exhausting system resources                      |
| Privilege Escalation  | Gaining higher-level permissions                 |
| Spoofing              | Masquerading as trusted entity                   |

---

## Encryption

- **Purpose:** Protect data at rest and in transit.
- **Symmetric Encryption:** Same key for encryption/decryption (e.g., AES).
- **Asymmetric Encryption:** Different keys (public/private, e.g., RSA).

---

## Auditing & Logging

- Monitoring user/process activities to detect and investigate security breaches.

---

## Interview Tips

- Know difference between authentication and authorization.
- Understand UNIX/Windows file permissions and access control models.
- Be able to describe common attacks and defenses.
- Explain how encryption helps in OS security.

---

## Possible Follow-Up Questions

- What is the purpose of access control lists?
- How does RBAC differ from DAC (Discretionary Access Control)?
- Give an example of a privilege escalation attack.
- How do operating systems defend against malware?

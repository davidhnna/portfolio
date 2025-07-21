---
layout: default
title: Projects
---

# Cybersecurity Projects

Explore hands-on cybersecurity projects demonstrating real-world exploitation and defense techniques.

---

## 🔓 Metasploit SMB Compromise

> **Platforms and Tools**: TryHackMe, Metasploit, John the Ripper

**Objective**  
Simulated an attack on a vulnerable SMB service using Metasploit to gain unauthorized access and escalate privileges.

**Key Steps**  
1. Exploited SMB vulnerability using `ms08_067_netapi` module.
2. Gained remote shell with Meterpreter.
3. Performed privilege escalation and extracted SAM database.
4. Used `hashdump` and cracked hashes with rainbow tables.

```bash
use exploit/windows/smb/ms08_067_netapi
set RHOST <target-ip>
exploit
```

**Outcome**  
Successfully compromised a machine, extracted credentials, and simulated post-exploitation steps.

---

## 🩻 SQL Injection with SQLMap

> **Platforms and Tools**: TryHackMe, SQLMap, Burp Suite, Linux Terminal

**Objective**  
Performed automated SQL injection on a vulnerable web application to extract sensitive data.

**Key Steps**  
1. Identified vulnerable endpoints using browser dev tools and Burp Suite.
2. Ran SQLMap with custom flags to enumerate databases.
3. Extracted user tables and dumped credentials.
4. Learned common SQLi vectors and how to mitigate them.

```bash
sqlmap -u "http://vulnerable.site/page.php?id=1" --dbs
sqlmap -u "http://vulnerable.site/page.php?id=1" -D users -T creds --dump
```

**Outcome**  
Gained a clear understanding of how SQL injection attacks are carried out and the importance of input sanitization.

---


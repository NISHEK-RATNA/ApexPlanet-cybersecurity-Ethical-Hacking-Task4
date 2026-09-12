# ApexPlanet Cybersecurity and Ethical Hacking – Task 4

## Exploitation & System Security

This repository contains the work completed for **Task 4** of the ApexPlanet Cybersecurity and Ethical Hacking Internship.

The task was performed in an **isolated and authorized virtual laboratory environment** using Kali Linux and Metasploitable2.

## Lab Environment

- Attacker: Kali Linux
- Target: Metasploitable2
- Kali IP: `192.168.56.101`
- Target IP: `192.168.56.102`
- Network: Isolated Host-Only Network

## Objectives

- Understand the basic penetration-testing methodology.
- Perform reconnaissance and service enumeration.
- Demonstrate exploitation using Metasploit.
- Perform controlled password testing using Hydra.
- Demonstrate password-hash cracking using John the Ripper.
- Conduct a safe social-engineering awareness simulation.
- Perform basic malware/file analysis.
- Apply a firewall hardening rule.

## Activities Completed

### 1. Penetration Testing Methodology
Followed a basic workflow:

1. Reconnaissance
2. Scanning and enumeration
3. Exploitation
4. Post-exploitation verification
5. Password testing
6. Analysis and documentation
7. System hardening

### 2. Metasploit Exploitation

The vulnerable **VSFTPD 2.3.4** FTP service on Metasploitable2 was tested using the Metasploit Framework.

The module used was:

`exploit/unix/ftp/vsftpd_234_backdoor`

A Meterpreter session was obtained and root-level access was verified in the authorized lab.

### 3. Password Attacks

#### Hydra

A controlled wordlist was used to demonstrate weak/default FTP credentials.

The lab account:

`msfadmin / msfadmin`

was successfully identified through the FTP password test.

The SSH test also demonstrated a compatibility limitation caused by the legacy SSH cryptographic algorithms.

#### John the Ripper

John the Ripper was used with a **locally generated harmless MD5 test hash** to demonstrate password recovery.

No third-party or real user credentials were used.

### 4. Social Engineering Awareness

A harmless phishing-awareness simulation was created.

The simulation focused on recognizing:

- Urgent or threatening language
- Requests for sensitive information
- Suspicious links or attachments
- Unusual sender addresses
- Pressure to act immediately

No real messages were sent and no credentials were collected.

### 5. Malware Basics and File Analysis

A harmless text file was created for basic static analysis.

The file was examined using:

- `file`
- `ls -lh`
- `sha256sum`

No malware was created, deployed, or executed.

### 6. System Hardening

The firewall configuration was examined and a defensive rule was applied to block incoming traffic from the isolated Metasploitable2 lab IP.

The resulting nftables configuration was verified.

## Tools Used

- Nmap
- Metasploit Framework
- Meterpreter
- Hydra
- John the Ripper
- iptables / nftables
- Kali Linux
- Metasploitable2

## Evidence

Screenshots demonstrating the practical activities are included in this repository.

The screenshots cover:

- Network configuration
- Nmap reconnaissance
- Metasploit exploitation
- Meterpreter verification
- Root privilege verification
- Hydra password testing
- John the Ripper
- Social-engineering awareness
- File analysis
- Firewall configuration and hardening

## Key Security Findings

- Vulnerable and outdated services can allow system compromise.
- Default credentials create significant security risks.
- Weak password hashes can be recovered quickly.
- Legacy cryptographic algorithms create compatibility and security problems.
- User awareness is important for reducing phishing risk.
- Proper firewall rules can reduce unnecessary network exposure.

## Recommendations

- Remove or update vulnerable services.
- Disable unnecessary network services.
- Change all default credentials.
- Use strong, unique passwords.
- Use modern password-hashing algorithms such as Argon2id, scrypt, or bcrypt.
- Upgrade legacy SSH implementations.
- Apply least-privilege firewall rules.
- Train users to recognize phishing attempts.
- Regularly patch systems and perform security assessments.

## Ethical and Safety Statement

All exploitation and password-testing activities were performed only against the intentionally vulnerable **Metasploitable2 virtual machine** in an isolated host-only laboratory.

No real-world systems, public services, or third-party accounts were targeted.

The social-engineering activity was an awareness simulation, and the malware-analysis activity used only a harmless text file.

## Conclusion

Task 4 provided practical experience with both offensive and defensive cybersecurity techniques. The exercises demonstrated the risks associated with vulnerable services, weak credentials, outdated cryptography, social engineering, and insufficient security controls.

This project was completed in a controlled and authorized cybersecurity laboratory environment.

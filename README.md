# Linux & Windows Security Basics

![GitHub Actions Status](https://img.shields.io/github/actions/workflow/status/martinzambonino/linux-windows-security-basics/ci.yml?branch=main)
![License](https://img.shields.io/github/license/martinzambonino/linux-windows-security-basics)

## What It Does

A practical guide and script collection for operating system security hardening and auditing:

- **Linux Hardening:** Bash scripts implementing CIS Benchmark recommendations (SSH configuration, firewall rules, user management, file permissions).
- **Windows Hardening:** PowerShell scripts for security policy auditing, Windows Defender configuration, and event log analysis.
- **Auditing & Monitoring:** Scripts that check system configurations against baseline security standards and generate compliance reports.
- **Documentation:** Step-by-step guides for securing fresh OS installations in lab environments.

## Skills Demonstrated

| Skill | Details |
|---|---|
| Linux Administration | Bash scripting, systemd, iptables/nftables, SELinux/AppArmor |
| Windows Administration | PowerShell, Group Policy, Windows Event Logs |
| Hardening | CIS Benchmarks, DISA STIGs, least privilege |
| Monitoring | Auditd, syslog, Windows Event Forwarding |

## How to Run

```bash
# Clone the repository
git clone https://github.com/martinzambonino/linux-windows-security-basics.git
cd linux-windows-security-basics

# Linux hardening scripts (run in a lab VM — NEVER on production)
chmod +x src/linux/*.sh
./src/linux/audit_ssh_config.sh

# Windows auditing scripts (run in PowerShell as Administrator in a lab VM)
# Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
# .\src\windows\audit_security_policy.ps1
```

## Methodology

- **CIS Benchmarks:** Center for Internet Security configuration guidelines for Linux and Windows.
- **DISA STIGs:** Defense Information Systems Agency Security Technical Implementation Guides.
- **NIST SP 800-123:** Guide to General Server Security.

## Limitations

- Scripts are designed for **lab/VM environments only** — never execute on production systems.
- Hardening scripts make configuration changes — always test in isolated virtual machines.
- Coverage focuses on Ubuntu/Debian (Linux) and Windows 10/11 (Windows).
- Scripts implement a subset of CIS Benchmarks for educational purposes, not full compliance.

## ⚖️ Ethical & Legal Disclaimer

> [!WARNING]
> **This repository is strictly for academic and educational purposes.**
> Hardening scripts modify system configurations and must **only** be executed on systems you own or have explicit, written authorization to configure.
> The author assumes no liability for system damage or misconfiguration resulting from the use of these scripts.

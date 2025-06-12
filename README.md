# 🧠 5-Day L1 Linux System Admin Lab (RHEL + Hyper-V + Ansible)

This repository contains a complete hands-on simulation designed to replicate the real-world experience of a **Level 1 Linux System Administrator** over a **5-day period**.

### 🎯 Goal  
Simulate 20–24 months of real-world L1 Linux System Administration in just **5 days** using **RHEL servers + Hyper-V + Ansible + Shell scripts**, replicating hybrid cloud tasks in a local lab.

---

## 🛠️ Lab Environment Overview

| Role        | OS        | Purpose                                       |
|-------------|-----------|-----------------------------------------------|
| Server01    | RHEL 8    | NFS server, internal DNS, basic monitoring    |
| Server02    | RHEL 8    | Apache, SSH, Ansible control node             |
| Client01    | RHEL 8    | Sysadmin workstation (SSH, scripts)           |
| Client02    | RHEL 8    | Developer workstation (support simulation)    |

---

## 🗓️ 5-Day Lab Simulation Plan

### ✅ Day 1 – Lab Setup + Core System Configuration
- Create and configure 4 VMs in Hyper-V
- Set static IPs, hostnames, `/etc/hosts`
- Install updates, SSH, firewalld
- Add admin user and test connectivity

### ✅ Day 2 – User Support + Monitoring + Services
- Mount NFS, restart Apache, fix SSH
- Monitor system usage (`top`, `journalctl`, etc.)
- Script disk usage alerts

### ✅ Day 3 – Shell Scripting + Cron + Backup
- Write 3 Bash scripts: cleanup, backup, user log
- Automate with cron
- Simulate data deletion + restore

### ✅ Day 4 – Ansible Basics
- Install Ansible and set up inventory
- Create 3 playbooks:
  - Install packages
  - Restart services
  - Push MOTD file

### ✅ Day 5 – Simulated L1 Ops + Documentation
- Run through simulated tickets: SSH issues, restore files, enforce locks
- Write SOP and Support Guide
- Document scripts and playbooks

---

## 📁 Suggested GitHub Structure

```bash
L1-Linux-Sys-Admin-Tasks/
├── scripts/
│   ├── cleanup_tmp.sh
│   ├── home_backup.sh
│   └── session_logger.sh
├── playbooks/
│   ├── install_tools.yml
│   ├── restart_httpd.yml
│   └── motd_update.yml
├── docs/
│   ├── L1_SOP.md
│   ├── User_Support_Guide.md
│   └── Lab_Report.md
├── ansible/
│   └── hosts
├── 5-day-lab.Rmd
└── README.md

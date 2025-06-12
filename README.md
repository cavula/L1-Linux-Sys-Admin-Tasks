# 🧠 5-Day L1 Linux System Admin Lab (RHEL + Hyper-V + Ansible)

This repository contains a complete hands-on simulation designed to replicate the real-world experience of a **Level 1 Linux System Administrator** over a **5-day period**.

The goal is to simulate 20 months of day-to-day operations, scripting, automation, user support, and documentation tasks — using a **locally hosted lab on Microsoft Hyper-V** with **RHEL servers**, **Linux clients**, **Ansible**, and **Bash** scripting.

---

## 🔧 What You'll Build

- A 4-VM lab setup using **RHEL 8**:
  - 2x Servers (NFS, Web, Ansible)
  - 2x Clients (SysAdmin + Developer role-play)
- Full system lifecycle tasks: provisioning, monitoring, patching, user management, backups
- Ansible playbooks and shell scripts to automate common admin functions
- A documented SOP, ticket response simulation, and backup/restoration procedures

---

## 🗓️ 5-Day Lab Simulation Plan Overview

### ✅ Day 1 – Lab Setup + System Configuration
- Create and configure VMs on Hyper-V
- Set static IPs, install SSH, configure DNS, NTP, etc.
- Add admin users and configure sudo access

### ✅ Day 2 – User Support + Monitoring + Services
- Reset passwords, fix SSH access
- Mount NFS shares, restart services
- Use `top`, `df`, `journalctl`, and monitor logs

### ✅ Day 3 – Shell Scripting + Cron + Backup
- Write Bash scripts for cleanup, backup, and user session tracking
- Set up cron jobs and test restores

### ✅ Day 4 – Ansible Basics
- Install and configure Ansible
- Create playbooks to install packages, restart services, and push files

### ✅ Day 5 – Simulated Operations & Documentation
- Simulate incidents and service desk tasks
- Create SOPs, troubleshooting guides, and documentation

---

## 🗂️ Recommended Folder Structure


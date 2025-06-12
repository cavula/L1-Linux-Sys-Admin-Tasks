---
title: "5-Day L1 Linux System Administrator Lab Plan"
author: "Your Name"
output: github_document
---

# 🧭 5-Day Lab Simulation Plan (L1 Linux System Admin – RHEL + Hyper-V)

### Goal  
Simulate 20 months of real-world L1 Linux System Administration in just **5 days** using **RHEL servers + Hyper-V + Ansible + Shell scripts**, replicating hybrid cloud tasks in a local lab.

---

## 🛠️ Lab Environment Overview

| Role        | OS        | Purpose                                       |
|-------------|-----------|-----------------------------------------------|
| Server01    | RHEL 8    | NFS server, internal DNS, basic monitoring    |
| Server02    | RHEL 8    | Apache, SSH, Ansible control node             |
| Client01    | RHEL 8    | Sysadmin workstation (SSH, scripts)           |
| Client02    | RHEL 8    | Developer workstation (support simulation)    |

---

# ✅ Day 1 – Lab Setup + Core System Configuration

### 🔧 Hyper-V Setup
- Create 4 VMs (2 servers, 2 clients)
- Configure networking with internal switch
- Install Guest Tools
- Set static IPs, hostnames, and `/etc/hosts`

### 🛠 Tasks
- Install `dnf`, update packages
- Create `admin` user and assign `sudo`
- Set up SSH, enable firewalld
- Configure time sync (`chronyd`)
- Test connectivity across all machines

### ✅ Deliverables
- VMs operational with SSH access
- Static IPs and DNS working
- Admin user created on all nodes

---

# ✅ Day 2 – User Support + Services + Monitoring

### 🧪 Support Scenarios
- Password reset for `developer`
- Mount NFS share from Server01 to Client02
- Fix SSH access issue for `developer`
- Restart `httpd` on Server02

### 🔍 Monitoring Tasks
- Use `top`, `df`, `uptime`, `vmstat`, `journalctl`
- Configure log rotation and alert scripts
- Create script to email when `/` > 80% usage

### ✅ Deliverables
- Disk space script with email alert
- Apache and SSH troubleshooting documented
- Monitoring command usage recorded

---

# ✅ Day 3 – Shell Scripting + Cron Jobs + Backup

### 🐚 Shell Scripts
- `cleanup_tmp.sh`: Delete files older than 3 days
- `home_backup.sh`: Compress and archive `/home`
- `session_logger.sh`: Log currently logged-in users

### 🕒 Cron Setup
- Daily cleanup
- Nightly backup
- Log sessions every 10 min

### 💾 Backup Tasks
- Use `rsync` or `tar`
- Simulate deletion + restore

### ✅ Deliverables
- 3 scripts tested and working
- Crontabs set
- Restore verified

---

# ✅ Day 4 – Ansible for Configuration Management

### ⚙️ Setup
- Install Ansible on Server02
- Setup SSH key auth to all nodes
- Add all hosts to `/etc/ansible/hosts`

### 🔧 Tasks
- Ping all nodes using Ansible
- Playbook 1: Install `vim`, `htop`, `httpd`
- Playbook 2: Restart `httpd`
- Playbook 3: Push `/etc/motd` file

### ✅ Deliverables
- 3 playbooks committed
- Ad-hoc commands executed
- Inventory file complete

---

# ✅ Day 5 – Simulated Real-World Operations

### 🕹️ Day-in-the-Life Simulation
- Fix SSH for developer
- Restart failed Apache service
- Run scheduled backup
- Lock inactive users (simulate security policy)
- Restore developer's deleted files

### 📄 Documentation Tasks
- Create:
  - `L1_SOP.md`
  - `User_Support_Guide.md`
  - Script library
  - Playbook library

### ✅ Deliverables
- SOPs created
- Lab run report
- Everything versioned in GitHub

---

## 🗂️ Suggested GitHub Repo Structure

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

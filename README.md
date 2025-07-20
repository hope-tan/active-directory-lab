# 🏢 Active Directory Lab

A hands-on infrastructure project deployed on **VMware vSphere**, featuring a secure Windows domain environment with domain-joined Linux clients, automated backups, and internal web hosting with SSL.

This project demonstrates my skills in **Active Directory administration**, **Group Policy configuration**, **PowerShell scripting**, and **system hardening** across Windows and Ubuntu environments.

---

## 🧩 Lab Overview

| Component              | Description                                       |
|------------------------|---------------------------------------------------|
| Windows Server 2019    | Domain Controller (DC), DNS, DHCP, File Sharing, scheduled PowerShell backups   |
| Windows Server Core 2019 | Backup Server — failover and scheduled PowerShell backups     |
| Windows 10 Workstation | Domain-joined endpoint                            |
| Ubuntu Machine        | Domain-joined Linux client  |
| Static Websites         | Internal sites hosted on Apache and IIS with SSL (HTTPS)             |

---
## 🧪 Lab Topology (Deployed in vSphere)
<img width="909" height="585" alt="ad-lab" src="https://github.com/user-attachments/assets/41259fd2-043c-487b-91c3-b4b252823024" />


---
## 🔐 Active Directory & Domain Services

- Configured **Active Directory Domain Services (AD DS)** on Windows Server 2019
- Created:
  - Organizational Units (OUs) for users, computers, and departments
  - Custom user accounts and security groups
- Enabled **DNS** and **DHCP** roles on the DC to support dynamic IP and name resolution
- Joined all Windows and Ubuntu systems to the domain

---

## 🛡️ Group Policy (GPOs)

Implemented several GPOs to enforce security and usability:

- **Security Settings**:
  - Computer lockout policy
  - Restricted Control Panel access
  - Restricted PowerShell access

- **User Experience**:
  - Drive mappings based on group membership
  - Desktop background customization
  - Logon message

---

## 📁 File Sharing

- Configured role-based access to shared folders
- Applied **NTFS** and **Share** permissions for least-privilege access

---

## 🌐 Internal Web Hosting

- Hosted 2 **static HTML** websites on the domain using IIS and Apache
- Secured with **SSL certificate**
- Created internal DNS name for access with forward and reverse lookups

---

## 💾 Backup & Recovery

- Windows Server Core 2019 configured for failover from the Windows Server 2019
- Created **PowerShell scripts** to back up key services and files
- Scheduled tasks for daily and weekly backups

---

## 🧠 Domain-Joined Ubuntu Integration

- Users can log in with domain credentials
- Configured file share access via FTP and domain resolution


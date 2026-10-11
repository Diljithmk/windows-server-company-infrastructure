# Windows Server Company Infrastructure

A hands-on IT System Administration project built using Windows Server 2025. This project simulates a small company's IT infrastructure using Active Directory, DNS, user and group management, departmental file sharing, and Group Policy.

## Project Overview

- **Operating System:** Windows Server 2025
- **Virtualization:** VMware Workstation
- **Server Name:** `DC01`
- **Domain Name:** `diljithcompany.local`
- **Project Type:** IT Support and System Administration Lab

## Objectives

- Install and configure Active Directory Domain Services (AD DS).
- Create a company domain and departmental Organizational Units.
- Manage domain users and security groups.
- Configure departmental file shares and NTFS permissions.
- Create and apply Group Policy Objects (GPOs).
- Verify domain controller and DNS functionality.

## Infrastructure Structure

```text
diljithcompany.local
|
+-- Departments
|   +-- IT
|   |   +-- it.admin
|   |   +-- IT_Team
|   |
|   +-- HR
|   |   +-- hr.executive
|   |   +-- HR_Team
|   |
|   +-- Finance
|       +-- finance.user
|       +-- Finance_Team
|
+-- Company-Security-Policy
```

## File Sharing Structure

```text
C:\CompanyShares
|
+-- IT
+-- HR
+-- Finance
```

Departmental folders are shared over the network. NTFS permissions are configured to control access, with security groups used to simplify permission management.

## Technologies Used

- Windows Server 2025
- Active Directory Domain Services
- DNS
- Organizational Units (OU)
- Active Directory Users and Computers
- Security Groups
- SMB File Sharing
- NTFS Permissions
- Group Policy Management
- PowerShell
- VMware Workstation

## Useful PowerShell Commands

Check server name:

```powershell
hostname
```

Check domain information:

```powershell
Get-ADDomain
```

Run Domain Controller diagnostics:

```powershell
dcdiag
```

Verify DNS resolution:

```powershell
nslookup diljithcompany.local
```

List Active Directory users:

```powershell
Get-ADUser -Filter *
```

List security groups:

```powershell
Get-ADGroup -Filter *
```

List shared folders:

```powershell
Get-SmbShare
```

Refresh Group Policy:

```powershell
gpupdate /force
```

## Security Practices

- Use security groups to manage permissions.
- Follow the principle of least privilege.
- Configure appropriate share and NTFS permissions.
- Apply security settings through Group Policy.
- Keep administrator credentials secure.

## Project Status

**Core configuration:** Practised in a virtual lab.

Additional exercises planned:
- DHCP server configuration
- Windows Server Backup and recovery
- File Server Resource Manager (FSRM) quotas
- Joining a Windows client to the domain
- Testing departmental access restrictions

## Learning Outcomes

This project provides practical experience with Windows Server administration, centralized identity management, domain authentication, DNS verification, file sharing, access control, and Group Policy.

It is designed for IT Support, System Administrator, and Network Administrator learning and interview preparation.

## Author

**Diljith M K**

IT Support | System Administration | Networking

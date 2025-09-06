Windows Infrastructure Lab (Azure VMs)
This repository contains a complete lab project for building a Core Windows Infrastructure in Azure. It demonstrates how to deploy a Domain Controller, join client PCs to the domain, configure GPOs, and migrate local file shares to Azure Files.
Project Overview
Goal:
Simulate a small corporate network using Azure VMs with Active Directory, DNS, Group Policies, and Azure File storage.
Skills Covered:
Azure VM & Networking setup (VNet, Subnets, NSG, DNS)
Active Directory Domain Services (AD DS) deployment
Organizational Units (OUs), users, and groups
Group Policy Objects (GPO) for password policies, desktop lockdown, wallpapers, and drive mapping
Azure Files migration using AzCopy
ITIL concepts: Service Request, Change, Incident, and Asset Management
Lab Topology
Resource Group: rg-infra-lab
VNet: vnet-infra-lab (10.0.0.0/16)
Subnet: subnet-workload (10.0.1.0/24)
Domain Controller VM: DC01 (Windows Server 2022)
Client VM: CL01 (Windows 10/11 Pro)
File Share: Azure Storage itsales
📸 Screenshots of topology setup and VMs are in the screenshots/ folder.
Folder Structure
WindowsInfraLab/
├─ docs/                # Project documentation
├─ screenshots/         # Screenshots of lab setup
└─ notes/               # Troubleshooting & notes
Step-by-Step Implementation
Azure Network & VM Setup
Created RG, VNet, Subnet
Configured DC01 (static IP 10.0.1.4) and CL01 (dynamic IP)
Configured DNS to point client to DC
Domain Controller & AD DS
Promoted DC01 to Domain Controller
Created new forest minster.local
Configured OUs: Users, Computers, Groups
Created test user Navya Sruthi and Sales Department group
Group Policies (GPOs)
Locked down Control Panel for users
Set desktop wallpaper via GPO
Mapped local drives for Sales Department
Azure File Share Migration
Created file share itsales
Uploaded files using AzCopy from D:\Shares\Sales
Mapped Azure File Share as drive S: for domain users
Testing & Verification
User login on client VM
GPO settings applied (gpupdate /force)
Drive mapping verified
ITIL Mapping
ITIL Process	Lab Example
Service Request Management	Created new user Navya & access to Sales share
Change Management	Promoted DC, created GPOs, mapped drives
Incident Management	Login or GPO issues, troubleshooting & resolving
Problem Management	Repeated mapped drive failures, root cause fix
Asset & Configuration Mgmt	VMs, IPs, GPOs recorded; GitHub docs as lightweight CMDB
Screenshots
The screenshots/ folder contains:
rg-vnet-dns.png – Resource group, VNet, DNS
dc-promo.png – DC promotion summary
aduc-ous-users-groups.png – OUs, users, and groups
cl01-domain-joined.png – Client joined to domain
gpo-lockdown.png – Control Panel lockdown
gpo-wallpaper.png – Desktop wallpaper GPO
gpo-drive-map.png – Drive mapping GPO
azure-files-share.png – Azure Files share
client-mapped-drive.png – Client mapped drive
Notes & Troubleshooting
See notes/troubleshooting.txt for issues like:
Wallpaper GPO path errors
Drive mapping using AzCopy and SAS tokens
gpupdate /force tips for client PCs
Conclusion
This project demonstrates a full Azure-based Windows infrastructure lab, showcasing skills in networking, Active Directory, Group Policies, file migration, and ITIL processes.

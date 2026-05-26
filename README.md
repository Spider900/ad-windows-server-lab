# 🖥️ Home Lab: Active Directory + Windows Server
# Overview
I designed a self-hosted home lab environment to simulate a corporate network using Active Directory Domain Services, DNS, DHCP, and Group Policy management on Windows Server. This document will showcase my deployment of these features.

![Badge](https://img.shields.io/badge/Windows_Server_2019-blue) ![Badge](https://img.shields.io/badge/Active_Directory-purple) ![Badge](https://img.shields.io/badge/DNS/DHCP-green) ![Badge](https://img.shields.io/badge/Group_Policy-brown) ![Badge](https://img.shields.io/badge/VirtualBox-grey)

# Architecture
| Component | Details |
| --------- | ------- |
| Domain Controller | Windows Server 2019 |
| Domain Name | mydomain.com |
| Client Machine  | Windows 11 (domain-joined) |
| Hypervisor | Oracle VirtualBox |
| Network Adapter | NAT + Host-Only |
| DC Static IP | 172.16.0.1 |
| DHCP Range | 172.16.0.100 - 172.16.0.200 |

# Features implemented
✅ Active Directory Domain Services (AD DS) 

✅ DNS - forward lookup zone 

✅ DHCP - scope, reservations, and exclusions

✅ Remote Access for client machine to interface with Domain Controller

✅ Organization Units (OUs) for structured user management

✅ User and security group creation

✅ Group Policy Objects (GPOs) — password policy, desktop lockdown

✅ Domain-joined Windows 11 client

✅ PowerShell automation for bulk user provisioning

# Settings and Configuration

# AD DS:

<img width="1918" height="1023" alt="AD-DS-1 " src="https://github.com/user-attachments/assets/1982176b-4fe2-45eb-ac37-4a549ff041be" />

1. root tree of my Active Directory

<img width="1918" height="1022" alt="AD-DS-2" src="https://github.com/user-attachments/assets/cc65c96a-3cda-4b03-bb69-d246daf104cf" />

2. Admin OU

<img width="1918" height="1018" alt="AD-DS-3" src="https://github.com/user-attachments/assets/41e47fc8-618b-41d4-a9f8-569ca3b13aa6" />

3. Users OU with 1,000+ users
   
# Remote Access:

<img width="1918" height="1022" alt="RA-1" src="https://github.com/user-attachments/assets/59d276f8-37dc-41c6-aa3b-7cb45e38eee1" />

1. Configured Routing and Remote Access

# DHCP:

<img width="1918" height="1022" alt="DHCP-1" src="https://github.com/user-attachments/assets/50144b02-39b4-4d84-824f-80cff187098e" />

1. DHCP Configuration and Scope


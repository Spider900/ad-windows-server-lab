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

### AD DS:

<img width="1918" height="1023" alt="AD-DS-1 " src="https://github.com/user-attachments/assets/1982176b-4fe2-45eb-ac37-4a549ff041be" />

1. root tree of my Active Directory

<img width="1918" height="1015" alt="AD-DS-4" src="https://github.com/user-attachments/assets/e94bb89b-f08a-4a99-9fea-9daaf5401ce6" />

2. Windows 11 Pro client machine connected to AD environment

<img width="1918" height="1022" alt="AD-DS-2" src="https://github.com/user-attachments/assets/cc65c96a-3cda-4b03-bb69-d246daf104cf" />

3. Admin OU

<img width="1918" height="1018" alt="AD-DS-3" src="https://github.com/user-attachments/assets/41e47fc8-618b-41d4-a9f8-569ca3b13aa6" />

4. Users OU with 1,000+ users

### GPO Settings

<img width="1918" height="1021" alt="image" src="https://github.com/user-attachments/assets/516473f9-f988-494e-aa0b-ad2039984644" />

1. Configured GPO so only Administrator Accounts can Access DC Machine

<img width="1918" height="1021" alt="GPO-2" src="https://github.com/user-attachments/assets/3f882ebf-2a0a-4e80-ac85-b96d6ae14cd2" />

2. Login attempt with user account

<img width="1918" height="1018" alt="GPO-3" src="https://github.com/user-attachments/assets/d7089b53-45c0-4282-812a-e7dfe38c8620" />

3. Failed login due to proper GPO controls

<img width="1918" height="1017" alt="GPO-4" src="https://github.com/user-attachments/assets/ebdb60c5-04d1-4b3a-9092-a457e9922da0" />

4. Login attempt with admin account

<img width="1918" height="1020" alt="GPO-5" src="https://github.com/user-attachments/assets/edfc69aa-6bdc-4427-9903-31e41f6975f8" />

5. Successful login

### Remote Access:

<img width="1918" height="1022" alt="RA-1" src="https://github.com/user-attachments/assets/59d276f8-37dc-41c6-aa3b-7cb45e38eee1" />

1. Configured Routing and Remote Access

### DHCP:

<img width="1918" height="1022" alt="DHCP-1" src="https://github.com/user-attachments/assets/50144b02-39b4-4d84-824f-80cff187098e" />

1. DHCP Configuration and Scope

### Powershell:

<img width="1918" height="1022" alt="Powershell-1" src="https://github.com/user-attachments/assets/e737ded5-cbce-4f09-a9f4-bc7abe7060a0" />

1. I used [this](https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1) powershell script to automatically generate 1,000+ users for my AD environment

### Client Machine:

<img width="1918" height="1016" alt="Client-1" src="https://github.com/user-attachments/assets/0c418df3-ca80-49e6-b5c1-d24cf667729b" />

1. I will be using account "aabrev" to demonstrate how a user can log into the Windows 11 computer

<img width="1918" height="1022" alt="Client-2" src="https://github.com/user-attachments/assets/37db751e-c909-48df-8acc-b9d1af2687c8" />

2. Login credentials used for "aabrev"

<img width="1918" height="1025" alt="Client-3" src="https://github.com/user-attachments/assets/ad84f13e-de4f-4744-8f79-80bc97939367" />

3. Successful login

# What I learned

1. How Active Directory Domain Services integrates with DNS for domain resolution
2. Kerberos authentication flow and how domain-joined clients authenticate
3. GPO inheritance
4. Diagnosing DNS misconfigurations that prevent domain join
5. Automating repetitive AD tasks with PowerShell

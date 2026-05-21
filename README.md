# 🖥️ Home Lab: Active Directory + Windows Server
# Overview
I designed a self-hosted home lab environment to simulate a corporate network using Active Directory Domain Services, DNS, DHCP, and Group Policy management on Windows Server.

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

# Enterprise Infrastructure Lab

## Overview

A hands-on home lab designed to simulate an enterprise IT environment. This project focuses on building, configuring, managing, and troubleshooting infrastructure using industry-standard technologies and system administration practices.

## Project Objectives

- Develop practical experience in enterprise IT infrastructure.
- Understand virtualization and virtual networking.
- Deploy and administer Windows Server environments.
- Implement centralized identity and access management.
- Configure and troubleshoot network services.
- Automate infrastructure administration.
- Maintain technical documentation and configuration records.

## Host System

| Component | Specification |
|---|---|
| Operating System | Windows 11 Pro |
| Processor | AMD Ryzen 7 5800X |
| CPU Cores / Threads | 8 / 16 |
| Memory | 32 GB RAM |
| Storage | 930 GB |
| Hypervisor | Microsoft Hyper-V |

## Virtual Infrastructure

| Server | Operating System | IP Address | Role |
|---|---|---|---|
| DC01 | Windows Server 2025 | 192.168.50.10 | Domain Controller, DNS |

## Network Configuration

| Setting | Value |
|---|---|
| Virtual Switch | Lab-Internal |
| Switch Type | Internal |
| Network | 192.168.50.0/24 |
| Subnet Mask | 255.255.255.0 |
| Domain | corp.example.test |
| NetBIOS Name | CORP |

## Technologies

- Microsoft Hyper-V
- Windows Server 2025
- Active Directory Domain Services (AD DS)
- Domain Name System (DNS)
- PowerShell
- IPv4 Networking
- Git and GitHub

## Project Roadmap

### Phase 1 — Virtualization and Networking

- [x] Enable Microsoft Hyper-V
- [x] Configure internal virtual networking
- [x] Deploy Windows Server 2025
- [x] Configure static IPv4 addressing

### Phase 2 — Active Directory and DNS

- [x] Install Active Directory Domain Services
- [x] Deploy an Active Directory forest
- [x] Promote DC01 to a domain controller
- [x] Configure DNS services
- [x] Verify forward DNS resolution
- [x] Verify DNS SRV records
- [ ] Configure reverse DNS resolution

### Phase 3 — Identity and Access Management

- [ ] Create organizational units
- [ ] Create domain users
- [ ] Configure security groups
- [ ] Implement Group Policy
- [ ] Join a Windows client to the domain
- [ ] Test domain authentication

### Phase 4 — Infrastructure Expansion

- [ ] Deploy DHCP services
- [ ] Configure file services and permissions
- [ ] Implement security hardening
- [ ] Configure infrastructure monitoring
- [ ] Implement backup and recovery procedures
- [ ] Automate administrative tasks with PowerShell

## Documentation

Technical documentation is organized within the `docs/` directory and will be updated throughout the project.

## Project Status

In active development. Infrastructure components are deployed, tested, and documented incrementally as part of an ongoing learning process.
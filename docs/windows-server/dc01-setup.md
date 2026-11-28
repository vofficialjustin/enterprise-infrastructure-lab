# DC01 — Windows Server Deployment

## Objective

Deploy a Windows Server virtual machine to serve as the primary domain controller and DNS server for the enterprise infrastructure lab.

## Virtual Machine Specifications

| Component | Configuration |
|---|---|
| VM Name | DC01 |
| Hypervisor | Microsoft Hyper-V |
| Generation | Generation 2 |
| Operating System | Windows Server 2025 Evaluation |
| Virtual Processors | 2 |
| Memory | 4096 MB (4 GB) |
| Dynamic Memory | Disabled |
| Virtual Disk | 80 GB |
| Disk Type | Dynamically expanding VHDX |
| Virtual Switch | Lab-Internal |
| Secure Boot | Enabled |

## Deployment Procedure

1. Opened Hyper-V Manager.
2. Created a new Generation 2 virtual machine named DC01.
3. Allocated 4 GB of memory and 2 virtual processors.
4. Created an 80 GB dynamically expanding virtual hard disk.
5. Connected the virtual network adapter to Lab-Internal.
6. Attached the Windows Server 2025 Evaluation ISO.
7. Started the virtual machine and installed Windows Server.
8. Configured the Administrator account.
9. Verified the server hostname as DC01.

## Network Configuration

| Setting | Value |
|---|---|
| Hostname | DC01 |
| IPv4 Address | 192.168.50.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | Not configured |
| Preferred DNS | 192.168.50.10 |
| IP Assignment | Static |

A static IP address was configured to ensure that other domain systems can consistently locate the server.

## Initial Troubleshooting

Before static IP configuration, the server received an Automatic Private IP Addressing (APIPA) address of `169.254.32.75`.

This occurred because the internal virtual network did not have an available DHCP server.

The issue was addressed by manually assigning a static IPv4 address.

## Verification

- Successfully booted Windows Server 2025.
- Successfully accessed Server Manager.
- Verified the server hostname.
- Confirmed static IPv4 configuration.
- Successfully pinged the server's own IP address.

## Design Decisions

- Generation 2 was selected to support modern UEFI-based virtual hardware and Secure Boot.
- Fixed memory allocation provides predictable memory availability.
- Dynamically expanding storage reduces initial physical storage consumption.
- Static IP addressing provides a consistent network identity for critical infrastructure services.
- An internal virtual switch provides a controlled lab network.

## Lessons Learned

- Virtual machines operate independently of the host operating system.
- Virtual hardware resources are allocated and managed through the hypervisor.
- Servers hosting critical network services typically require consistent IP addresses.
- APIPA addresses can indicate the absence of an available DHCP server.
- Server Manager provides centralized access to Windows Server administration tools.

## Result

DC01 was successfully deployed and configured as the foundational Windows Server instance for the enterprise infrastructure lab.

Subsequent Active Directory deployment and DNS configuration are documented separately.
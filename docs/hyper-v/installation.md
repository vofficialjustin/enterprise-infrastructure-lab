# Hyper-V Installation and Configuration

## Objective

Configure Microsoft Hyper-V on a Windows 11 Pro host to establish a virtualization environment for an enterprise infrastructure lab.

## Host Specifications

| Component | Specification |
|---|---|
| Operating System | Windows 11 Pro |
| Processor | AMD Ryzen 7 5800X |
| CPU Cores | 8 |
| Logical Processors | 16 |
| Memory | 32 GB RAM |
| Storage | 930 GB |

## Hypervisor Selection

Oracle VirtualBox was initially considered for hosting virtual machines. However, its nested AMD-V virtualization option was unavailable.

Microsoft Hyper-V was selected as the primary hypervisor because of its native Windows integration and relevance to enterprise virtualization environments.

## Installation Procedure

1. Opened the Windows Run dialog using `Win + R`.
2. Executed `optionalfeatures` to access Windows Features.
3. Located and enabled Hyper-V, including its management tools and platform components.
4. Restarted the host system to complete the installation.
5. Opened Hyper-V Manager to verify successful installation.

## Verification

- Successfully launched Hyper-V Manager.
- Confirmed that the local host was available for management.
- Accessed Virtual Switch Manager.
- Confirmed the ability to create and configure virtual machines.

## Architecture

Hyper-V operates as a Type 1 hypervisor, providing virtual machines with isolated computing environments while sharing the physical host's hardware resources.

## Lessons Learned

- Virtualization allows multiple operating systems to run on a single physical machine.
- Hypervisors manage virtual CPU, memory, storage, and networking resources.
- Hardware virtualization and hypervisor compatibility are important considerations when selecting a virtualization platform.
- Hyper-V Manager provides centralized management of virtual machines and virtual networks.

## Result

Microsoft Hyper-V was successfully installed and verified. The host is ready to support virtual machines and virtual networking for the enterprise infrastructure lab.